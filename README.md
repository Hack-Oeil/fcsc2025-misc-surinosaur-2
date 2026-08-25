# FCSC 2025 Surinausor (Winds of the past)

*Le FCSC est un CTF au format Jeopardy, mais voici une épreuve pour vous entrainer au mode Attaque-Défense.* *Les flags échangés entre les équipes simulées sont fictifs et indépendants du FCSC.* *Votre but est de filtrer le trafic réseau : une fois que vous aurez réussi, le flag pour valider l’épreuve FCSC vous sera donné.*

Vous jouez un [CTF en mode Attack/Defense](https://2023.faustctf.net/information/attackdefense-for-beginners/), mais c’est la catastrophe ! Les organisateurs n’ont fourni que des services sous forme de binaires ou dans des langages exotiques que vous ne connaissez pas, impossible de les patcher simplement. Vous décidez de changer drastiquement de stratégie : plutôt que de corriger les vulnérabilités, vous mettez en place [un système de prévention d’intrusion](https://fr.wikipedia.org/wiki/Syst%C3%A8me_de_pr%C3%A9vention_d%27intrusion) (IPS) sur la machine hébergeant vos services (la *vulnbox*).

Nous vous donnons en référence une capture réseau (fichier `winds-of-the-past.pcap`) réalisée au moment où vous avez découvert avec horreur sur le scoreboard qu’une équipe a réussi à voler vos flags. Les flags de cet attaque-défense suivent la regex `ECSC_[A-Za-z0-9\/+]{32}`. Votre but est d’écrire des règles Suricata pour **bloquer seulement le payload utilisé par la ou les attaques observées**. Il ne faut pas bloquer le trafic légitime qui permet entre autre de déposer des flags et tester la présence des flags dans le service. Une fois vos règles écrites, vous pouvez vous connectez sur `nc localhost 4000` pour les tester sur du nouveau trafic. Nous vous donnons le flag FCSC une fois le service correctement protégés (trafic illégitime bloqué, trafic légitime non modifié).

Vous pouvez télécharger des exemples de règles de blocage ici pour vous inspirer : [https://rules.emergingthreats.net/OPEN_download_instructions.html](https://rules.emergingthreats.net/OPEN_download_instructions.html). Nous vous recommandons également de lire la documentation de Suricata : [https://docs.suricata.io/en/suricata-7.0.6/rules/index.html](https://docs.suricata.io/en/suricata-7.0.6/rules/index.html).

Note : *Le service d’Attaque-Défense considéré est Winds of the past, développé initialement pour l’ECSC 2022. Il n’est pas utile d’aller lire le code source de ce service pour résoudre cette épreuve.*

Auteur : erdnaxe

Origine : [Surinausor (Winds of the past)](https://hackropole.fr/fr/challenges/misc/fcsc2025-misc-surinosaur-2/)


## Challenge
[files/winds-of-the-past.pcap.xz](files/winds-of-the-past.pcap.xz)

-----------

## Installation manuel
Vous n'utilisez pas l'application **les CTFs de Cyrhades** ? C'est dommage !
Mais voici comment installer ce CTF manuellement :

> git clone https://github.com/Hack-Oeil/fcsc2025-misc-surinosaur-2.git

> cd fcsc2025-misc-surinosaur-2

> docker compose up

-----------

## Sur le site officiel hackropole.fr
> https://hackropole.fr/fr/challenges/misc/fcsc2025-misc-surinosaur-2/

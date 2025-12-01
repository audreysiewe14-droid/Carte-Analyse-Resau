
# 🔹 Projet 1 : Carte d’analyse réseau

## 1️⃣ Modèle OSI
Le modèle **OSI (Open Systems Interconnection)** comporte **7 couches** :  

1. **Physique (couche 1)** : Transmission des bits sur le support (câble, fibre, ondes radio).  
2. **Liaison de données (couche 2)** : Transmission fiable de trames entre deux machines connectées (ex :protocole Ethernet, adresse MAC).  
3. **Réseau (couche 3)** : Acheminement des paquets entre plusieurs réseaux (ex :protocole IP, adresse ip).  
4. **Transport (couche 4)** : Gestion de la transmission de données d’un point à un autre, fiable ou non (ex : protocole TCP/UDP).  
5. **Session (couche 5)** : Gestion des sessions de communication entre applications.  
6. **Présentation (couche 6)** : Formatage et traduction des données (ex : chiffrement, compression).  
7. **Application (couche 7)** : Interface utilisateur et applications réseau (ex : navigateur web, mail).  

## 2️⃣ Modèle TCP/IP
Le modèle **TCP/IP** comporte **4 couches** :  

1. **Accès réseau (Network Interface)** : Équivalent des couches 1 et 2 du modèle OSI.  
2. **Internet** : Équivalent de la couche 3 OSI, gère le routage des paquets (ex : protocole IP).  
3. **Transport** : Équivalent de la  couche 4 du modèle OSI (TCP ou UDP).  
4. **Application** : Combine les couches 5 à 7 du modèle OSI, ex de protocoles : HTTP, FTP, SMTP, DNS.  

## 3️⃣ Comparaison TCP vs UDP

| Protocole | Fiabilité | Connexion | Vitesse | Usage typique |
|-----------|-----------|-----------|---------|---------------|
| **TCP**   | Fiable, contrôle d’erreur | Orienté connexion | Plus lent | Web (HTTP/HTTPS), mail (SMTP) |
| **UDP**   | Non fiable, pas de contrôle | Sans connexion | Rapide | Streaming, jeux en ligne, DNS |

## 4️⃣ Principaux ports

| Port | Protocole | Usage |
|------|-----------|------|
| 20   | FTP       | Transfert de fichiers (données) |
| 21   | FTP       | Commandes FTP |
| 22   | SSH       | Connexion sécurisée |
| 25   | SMTP      | Envoi de mail |
| 53   | DNS       | Résolution de noms |
| 80   | HTTP      | Web non sécurisé |
| 443  | HTTPS     | Web sécurisé |

## 5️⃣ Fonctionnement d’un routeur

1>Definition
Un **routeur** permet de connecter plusieurs réseaux et de **choisir le meilleur chemin** pour les paquets de données. 

-> Utilise des **tables de routage** (tableau représentant les routes connues par le routeur) pour savoir où envoyer chaque paquet.Es tsbles contiennent :
  -**l'adresse IP**
  - **le masque réseau**
  - **le protocole utilisé (*direct*, *statique*, "*dynamique*)
  - **l'interface de sortie**
  - **le prochain saut**(*next hop*)
  
 
->**Comment fait un routeur pour trouver les routes correspondantes à un paquet ?**
-Tout d'abord, il acquiert **l'adresse MAC destination** reçu
- puis compare chaque **masque réseau** des routes qu'il connaît en faisant un **et logique** entre l'adresse Mac de destination et ce masque
  -Lorsqu'il y'a équivalence, il renvoie les routes potentielles.
  
-> Fonctionne sur la **couche 3 (Réseau)** du modèle OSI. 

-> Peut filtrer le trafic (pare-feu) et gérer la traduction d’adresses (NAT).

### Partie 1 : Gestion des utilisateurs

- **Q2.1.1** - Création de l'utilisateur **jfsorin** en précisant dans la commande de créer le dossier home correspondant et le shell par défaut. Création ensuite du mot de passe
  
  ![Q2.1.1](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice2/Q2.1.1.png?raw=true)
  
- **Q2.1.2** - Il est préconiser de bien créer le **/home** de l'utilisateur, de bien penser à paramétrer le **shell par défaut** voulu ainsi que paramétrer un mot de passe complexe, d'une longueur correcte, comprenant de la casse ainsi que des caractères spéciaux.
### Partie 2 : Configuration de SSH

- **Q2.2.1** - Modification du fichier **/etc/ssh/sshd_config.d/local.conf** indiquant _PermitRootLogin yes_ en **no**
  
  ![Q2.2.1](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice2/Q2.2.1.png?raw=true)
  
- **Q2.2.2** - Autorisation de connexion à l'utilisateur **jfsorin** uniquement en modifiant le fichier **local.conf**
  
  ![Q2.2.2](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice2/Q2.2.2.png?raw=true)
  
- **Q2.2.3** - Mise en place d'une authentification par clé et désactivation de l'authentification par mot de passe
  
  ![Q2.2.3](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice2/Q2.2.3.png?raw=true)
  
  
  Redémarrage du service pour appliquer les changements: ```systemctl restart sshd```

### Partie 3 : Analyse du stockage

- **Q2.3.1 / Q2.3.2** - Il y a un disque **sda** monté avec des volumes logiques **LVM**  et un **RAID 1**
  
  ![Q2.3.1](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice2/Q2.3.1.png?raw=true)
  
  
  ![Q2.3.2](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice2/Q2.3.2.png?raw=true)
  
- **Q.2.3.3** - Ajout d'un disque de 8Gb et réparation du RAID
	- Création de la partition principale de type **RAID Linux auto**
	  
	  ![Q2.3.3](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice2/Q2.3.3.png?raw=true)
	  
	- Reconstruction du **RAID1** et vérification de la reconstruction
		
		![Q2.3.3_cap2](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice2/Q2.3.3_cap2.png?raw=true)
		
- **Q2.3.4** - Création d'un nouveau **LV** et montage automatique sur **/var/lib/bareos/storage**
  cp3-vg
  
  ![Q2.3.4](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice2/Q2.3.4.png?raw=true)
  
  
  ![Q2.3.4_cap2](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice2/Q2.3.4_cap2.png?raw=true)
  
- **Q2.3.5** - Il reste 1.79Gb
  
  ![Q2.3.5](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice2/Q2.3.5.png?raw=true)

### Partie 4 : Sauvegardes

- **Q2.4.1**:
	- **Bareos Director** (bareos-dir) 
		C'est le chef d'orchestre. Il est responsable de la planification, du contrôle et du lancement des tâches de sauvegardes. Il contrôle l'ensemble des autres composants. Il est installé sur le serveur en charge de la gestion des sauvegardes.
	- **Bareos Storage Daemon**  (bareos-sd)
	    Bareos permet d'effectuer des sauvegardes sur différents types de supports (bandes magnétiques, disques, stockage distant...). L'écriture sur ces supports est effectué par un **Storage Daemon**.  
	    Il peut donc y en avoir plusieurs, si on souhaite par exemple que les sauvegardes soient hébergées sur les disques de plusieurs machines.  
	    Une tâche de sauvegarde est donc lancée par le **Director** qui met en relation un **File Daemon** présent sur la machine à sauvegarder avec un **Storage Daemon** présent lui sur la machine qui enregistrent les informations de la sauvegarde sur un support de stockage.
	- **Bareos File Daemon**  (bareos-fd)
	    Ce composant est installé sur chaque machine devant être sauvegardée.  
	    Il est en charge de collecter les informations à sauvegarder et de les envoyer au **Bareos Storage Daemon**

### Partie 5 : Filtrage et analyse réseau

- **Q.2.5.1** - Le fichier de configuration utilisé (présent dans le fichier /etc/network/interfaces) est **/root/nftables/config.nft**
  
  ![Q2.5.1](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice2/Q2.5.1.png?raw=true)
  
- **Q2.5.2** - Les communications autorisées **en entrée** sont:
	- SSH
	- ICMP
	- ICMPv6
- **Q2.5.3** - Tout le reste est refusé
- **Q2.5.4** - Ajout de l'autorisation de communication de bareos (la vm étant en connexion par pont, elle est sur le réseau 172.16.0.0/16)
  
  ![Q2.5.4](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice2/Q2.5.4.png?raw=true)
  

### Partie 6 : Analyse de logs

- **Q.2.6.1** - Les 10 derniers échecs de connexion SSH
  
  ![Q2.6.1](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice2/Q2.6.1.png?raw=true)
  
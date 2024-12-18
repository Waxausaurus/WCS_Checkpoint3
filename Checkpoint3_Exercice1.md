
### Partie 1 : Gestion des utilisateurs

 - **Q.1.1.1** - Création de **Lionel Lemarchand** en calquant **Kelly Rhameur** dans la bonne OU (Direction des ressources humaines)
   
   ![Q1.1.1](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice1/Q1.1.1.png?raw=true)
   
   Définition des attributs à l'identique
   
   ![Q1.1.1_cap2](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice1/Q1.1.1_cap2.png?raw=true)
   
   
   ![Q1.1.1_cap3](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice1/Q1.1.1_cap3.png?raw=true)
   
   Ajout dans les mêmes groupes
   
   ![Q1.1.1_cap4](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice1/Q1.1.1_cap4.png?raw=true)
   
   Résultat final
   
   ![Q1.1.1_cap5](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice1/Q1.1.1_cap5.png?raw=true)
   
- **Q.1.1.2** - Création de l'OU **DeactivatedUsers**
  
  ![Q1.1.2](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice1/Q1.1.2.png?raw=true)
  
  Désactivation de **Kelly Rhameur**
  
  ![Q1.1.2_cap2](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice1/Q1.1.2_cap2.png?raw=true)
  
  
  ![Q1.1.2_cap3](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice1/Q1.1.2_cap3.png?raw=true)
  
  Déplacement du compte dans l'OU **DeactivatedUsers**
  
  ![Q1.1.2_cap4](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice1/Q1.1.2_cap4.png?raw=true)
  
  
  ![Q1.1.2_cap5](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice1/Q1.1.2_cap5.png?raw=true)
  
- **Q1.1.3** - Création du nouveau groupe d'OU **GrpDeactivatedUsers**
  
  ![Q1.1.3](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice1/Q1.1.3.png?raw=true)
  
  Ajout du compte dans le groupe
  
  ![Q1.1.3_cap2](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice1/Q1.1.3_cap2.png?raw=true)
  
  Retrait du compte de l'ancien groupe
  
  ![Q1.1.3_cap3](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice1/Q1.1.3_cap3.png?raw=true)
  
  
  ![Q1.1.3_cap4](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice1/Q1.1.3_cap4.png?raw=true)
  
- **Q1.1.4** - Création du dossier personnel de **Lionel Lemarchand** dans le disque **DossiersIndividuels** (lecteur F: sur le serveur) et archivage du dossier de **Kelly Rhameur**
  
  ![Q1.1.4](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice1/Q1.1.4.png?raw=true)

### Partie 2 : Restriction utilisateurs

- **Q1.2.1** - Limitation des horaires de **Gabriel Guhl** (Dans l'onglet **Account** dans les propriétés de l'utilisateur, bouton **logon hours**)
  
  ![Q1.2.1](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice1/Q1.2.1.png?raw=true)
  
- **Q1.2.2** - Dans le même onglet, fonction **logon to**, permission de se connecter seulement au pc **CLIENT01**
  
  ![Q1.2.2](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice1/Q1.2.2.png?raw=true)
  
- **Q1.2.3** - Ajout d'une GPO obligeant les utilisateurs à utiliser des mots de passes complexes et de minimum 12 caractères
  
  ![Q1.2.3](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice1/Q1.2.3.png?raw=true)
  
  Application du lien dans l'OU **LabUsers**
  
  ![Q1.2.3_cap2](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice1/Q1.2.3_cap2.png?raw=true)

### Partie 3 : Lecteurs réseaux

- **Q1.3.1** - Ajout d'une GPO **drive mount** pour monter automatiquement les lecteurs E: et F: sur les clients (en ayant préalablement partagé les disques)
  
  ![Q1.3.1](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice1/Q1.3.1.png?raw=true)
  
  
  ![Q1.3.1_cap2](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice1/Q1.3.1_cap2.png?raw=true)
  
  Pour **DossiersCommuns**
  
  ![Q1.3.1_cap3](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice1/Q1.3.1_cap3.png?raw=true)
  
  
  ![Q1.3.1_cap4](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice1/Q1.3.1_cap4.png?raw=true)
  
  
  ![Q1.3.1_cap5](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice1/Q1.3.1_cap5.png?raw=true)
  
  Pour **DossiersIndividuels**
  
  ![Q1.3.1_cap6](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice1/Q1.3.1_cap6.png?raw=true)
  
  
  ![Q1.3.1_cap7](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice1/Q1.3.1_cap7.png?raw=true)
  
  
  ![Q1.3.1_cap8](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice1/Q1.3.1_cap8.png?raw=true)
  
  Ajout du lien de la GPO
  
  ![Q1.3.1_cap9](https://github.com/Waxausaurus/ImgStorage/blob/main/Checkpoint3_Exercice1/Q1.3.1_cap9.png?raw=true)
  

### Partie 1 : Gestion des utilisateurs

 - **Q.1.1.1** - Création de **Lionel Lemarchand** en calquant **Kelly Rhameur** dans la bonne OU (Direction des ressources humaines)
   (INSERER Q1.1.1)
   Définition des attributs à l'identique
   (INSERER Q1.1.1_cap2)
   (INSERER Q1.1.1_cap3)
   Ajout dans les mêmes groupes
   (INSERER Q1.1.1_cap4)
   Résultat final
   (INSERER Q1.1.1_cap5)
- **Q.1.1.2** - Création de l'OU **DeactivatedUsers**
  (INSERER Q1.1.2)
  Désactivation de **Kelly Rhameur**
  (INSERER Q1.1.2_cap2)
  (INSERER Q1.1.2_cap3)
  Déplacement du compte dans l'OU **DeactivatedUsers**
  (INSERER Q1.1.2_cap4)
  (Q1.1.2_cap5)
- **Q1.1.3** - Création du nouveau groupe d'OU **GrpDeactivatedUsers**
  (INSERER Q1.1.3)
  Ajout du compte dans le groupe
  (INSERER Q1.1.3_cap2)
  Retrait du compte de l'ancien groupe
  (INSERER Q1.1.3_cap3)
  (INSERER Q1.1.3_cap4)
- **Q1.1.4** - Création du dossier personnel de **Lionel Lemarchand** dans le disque **DossiersIndividuels** (lecteur F: sur le serveur) et archivage du dossier de **Kelly Rhameur**
  (INSERER Q1.1.4)

### Partie 2 : Restriction utilisateurs

- **Q1.2.1** - Limitation des horaires de **Gabriel Guhl** (Dans l'onglet **Account** dans les propriétés de l'utilisateur, bouton **logon hours**)
  (INSERER Q1.2.1)
- **Q1.2.2** - Dans le même onglet, fonction **logon to**, permission de se connecter seulement au pc **CLIENT01**
  (INSERER Q1.2.2)
- **Q1.2.3** - Ajout d'une GPO obligeant les utilisateurs à utiliser des mots de passes complexes et de minimum 12 caractères
  (INSERER Q1.2.3)
  Application du lien dans l'OU **LabUsers**
  (INSERER Q1.2.3_cap2)

### Partie 3 : Lecteurs réseaux

- **Q1.3.1** - Ajout d'une GPO **drive mount** pour monter automatiquement les lecteurs E: et F: sur les clients (en ayant préalablement partagé les disques)
  (INSERER Q1.3.1)
  (INSERER Q1.3.1_cap2)
  Pour **DossiersCommuns**
  (INSERER Q1.3.1_cap3)
  (INSERER Q1.3.1_cap4)
  (INSERER Q1.3.1_cap5)
  Pour **DossiersIndividuels**
  (INSERER Q1.3.1_cap6)
  (INSERER Q1.3.1_cap7)
  (INSERER Q1.3.1_cap8)
  Ajout du lien de la GPO
  (INSERER Q1.3.1_cap9)
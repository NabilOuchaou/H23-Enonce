# Mise en place

## Prérequis

- [Git](https://git-scm.com/downloads)
- [Java 11](https://aws.amazon.com/corretto/)
- [IntelliJ](https://www.jetbrains.com/idea/download/)
  - Version Community ou Ultimate disponible gratuitement avec l'université :)
- [Postman](https://www.postman.com/downloads/)
- [Compte Github](https://github.com/login)

## Étapes

### 1. Création de l'organisation

Créez ⚠️ **1 SEULE ORGANISATION PAR ÉQUIPE** ⚠️ sur Github.

1. En haut à droite, cliquez sur `+` puis `New organization`
2. À gauche, cliquez sur `Create a free organization`
3. Choisissez un nom d'équipe (**DOIT contenir votre numéro d'équipe!!!**)
4. Donnez le email du responsable des plateformes de votre équipe
5. Indiquez l'appartenance à `Business or institution` et donnez le même nom que précédemment
6. Ajoutez tous les membres de votre équipe
7. ⚠️ **AJOUTEZ LES AUXILIAIRES ET CORRECTEURS** en tant **QU'ADMINISTRATEURS** ⚠️
    - `vigenere23`

### 2. Copie du projet

Copiez le template du projet vers votre nouvelle organisation.

1. [Copiez le template](https://github.com/glo2003/jersey-api-template/generate)
2. Choisissez le `Repository name`
3. ⚠️ **LE `Owner` DOIT ÊTRE VOTRE NOUVELLE ORGANISATION** ⚠️
4. ⚠️ **DOIT ÊTRE PRIVÉ/PRIVATE!!!** ⚠️

### 3. Setup IntelliJ+Java

Exécutez le projet.

1. Clonez le projet vers votre poste local
2. Ouvrez le projet cloné dans IntelliJ
3. Ajustez vos réglages d'IntelliJ
    1. Allez dans `File > Projet Structure`
    2. Dans l'onglet `Project Settings > Project`
        1. Choisissez la version **11 - Amazon Corretto** comme `Project SDK`
        2. Choisissez la version **11** de Java comme `Project langage level`
4. Démarrez le projet
    1. Cliquez sur la flèche verte en haut à droite
    2. Du texte en rouge devrait s'affiche à la console
        1. C'est normal s'il s'agit de `INFO` ou `WARNING`
        2. Ce n'est pas normal s'il s'agit de `ERROR`

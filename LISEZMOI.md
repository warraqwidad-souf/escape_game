# Le Manoir de l'Horloger : projet Android

Jeu d'escape en dix chambres. Le jeu lui-même est une page web (`app/src/main/assets/index.html`)
affichée en plein écran par une WebView. Aucune dépendance externe.

## Obtenir l'APK

### Avec Android Studio
1. Ouvrez ce dossier dans Android Studio (File > Open) et laissez la synchronisation Gradle se terminer.
2. Menu Build > Build App Bundle(s) / APK(s) > Build APK(s).
3. L'APK se trouve dans `app/build/outputs/apk/debug/app-debug.apk`.

### En ligne de commande (JDK 17 et SDK Android installés)
    ./gradlew assembleDebug

### Sans rien installer, avec GitHub
1. Créez un dépôt GitHub et poussez-y ce dossier sur la branche `main`.
2. L'onglet Actions lance « Construire l'APK ». À la fin, téléchargez `ManoirHorloger-apk`
   dans les artefacts de l'exécution.

## Installer sur un téléphone
Copiez `app-debug.apk` sur le téléphone, ouvrez-le et autorisez l'installation depuis cette source.

## Modifier le jeu
Tout le jeu est dans `app/src/main/assets/index.html`. Les dix chambres sont décrites dans le tableau `ROOMS`.

## Avant une publication sur Google Play
- Créez une clé de signature et construisez en `release`.
- Passez `targetSdk` à 35 et gérez les marges système (affichage bord à bord).
- Remplacez l'identifiant `com.manoir.horloger` par le vôtre.

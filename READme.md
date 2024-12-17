# Station Météo Zigbee avec thingy:53

Il facilite la réception des données via Zigbee. Grâce à ce code, Vous pouvez facilement interagir avec les capteurs et les services fournis par le Thingy:53.

**Matériel nécessaire:**
- Thingy:91
- Câble micro USB
- nRF Connect for Desktop
- Visual Studio Code (VS Code)
- nRF Connect sur téléphone

**Installation et Configuration:**
Pour exécuter ce projet, vous devez installer et configurer le nRF Connect for Desktop et Visual Studio Code (VS Code). 

Note : Assurez-vous que la chaîne d'outils (Toolchain) et le SDK sont installés sur le disque C:\ de l'ordinateur, dans un dossier dédié. Le dossier contenant le code pour le Thingy:91 doit également être placé dans un dossier de programmation sur le disque C:\.

Suivez les étapes ci-dessous pour la configuration :
1. Installation des outils en ligne de commande nRF
  - Téléchargez et installez les nRF Command Line Tools depuis le lien suivant : https://www.nordicsemi.com/Products/Development-tools/nRF-Command-Line-Tools/Download.
  - Les nRF Command Line Tools incluent nrfjprog, un outil essentiel pour flasher le firmware sur vos kits de développement Nordic.

2. Installation de Visual Studio Code
  - Rendez-vous sur https://code.visualstudio.com/download et installez la version de VS Code correspondant à votre système d'exploitation.

4. Installation du nRF Connect Extension Pack dans VS Code
  - Dans la barre d'activités de VS Code, cliquez sur l'icône Extensions.
  - Recherchez nRF Connect for VS Code Extension Pack, puis cliquez sur Installer.

Le nRF Connect Extension Pack dans VS Code permet de :
  - Développer, créer, déboguer et déployer des applications embarquées basées sur le SDK nRF Connect.
  - Interagir avec le compilateur, l'éditeur de liens, le système de construction complet, un débogueur compatible RTOS, et le SDK nRF Connect.
  - Utiliser un éditeur visuel pour les fichiers Devicetree et un terminal série intégré.

4. Installation de la chaîne d'outils (Toolchain) sur VS Code
- Lors du premier lancement de l'extension nRF Connect for VS Code (cliquez sur l'extension dans la barre de gauche), vous serez invité à installer une Toolchain. Si aucune n'est détectée, procédez ainsi :
    - Cliquez sur Installer la Toolchain.
    - Choisissez une version compatible avec la version du SDK nRF Connect que vous utiliserez (la dernière version recommandée).
    - L'installation peut prendre quelques minutes.

5. Installation du SDK nRF Connect

Dans nRF Connect pour VS Code, cliquez sur Gérer le SDK.

Dans cette section, vous pourrez installer, désinstaller et sélectionner la version active du SDK.
- Cliquez sur Installer le SDK pour afficher les versions disponibles et choisir celle que vous souhaitez utiliser et installer la, le mieux est de sélectionner la dernière sans parenthèse.
- Une fois ces étapes terminées, votre environnement est prêt pour le développement avec le SDK nRF Connect et Visual Studio Code.

**Envoi du code au Thingy:53:**
- Connectez la carte Thingy:53 à votre ordinateur via un câble micro-USB.
- Allumez la carte en appuyant sur le bouton SW1 puis en activant l'interrupteur ON/OFF.

![thingy53](https://github.com/user-attachments/assets/3cd97461-9562-450e-85fc-998dda2f8b63)
-  Ouvrez nRF Connect for Desktop, puis l'outil Programmer (à installer si nécessaire).
- Cliquez sur Select a Device et sélectionnez le Thingy:91 dans la liste.
- Dans Add File, cliquez sur Browse, allez dans le dossier téléchargé > ouvrez le dossier .zip.
- Cliquez ensuite sur Write, puis Write à nouveau dans la fenêtre de confirmation pour flasher le code.

**Pairage avec Matter :**
1. Activation du mode de pairage
- Sur le Thingy:53, appuyez sur le bouton utilisateur (SW1) jusqu’à ce que la LED clignote en indiquant le mode de pairage Zigbee.

2. Ajouter le Thingy:53 à une passerelle Zigbee
- Ouvrez votre passerelle Zigbee (ex. Zigbee2MQTT, Philips Hue, ou autre)
- Mettez la passerelle en mode pairage et suivez les instructions spécifiques à votre passerelle pour détecter et connecter le Thingy:53.
- Une fois connecté, le Thingy:53 apparaîtra comme un dispositif dans votre réseau Zigbee.
- Utilisez l’interface de votre passerelle pour visualiser les données des capteurs ou configurez un outil comme Zigbee2MQTT pour les exporter vers une plateforme comme Home Assistant.

NS-3 est principalement développé pour les systèmes basés sur Unix/Linux, ce qui signifie qu'il peut être plus facile d'installer et d'utiliser NS-3 sur un environnement Unix/Linux tel qu'Ubuntu. Cependant, il existe des moyens d'exécuter NS-3 sur Windows sans avoir besoin d'une machine virtuelle Ubuntu. Voici quelques options que vous pouvez envisager :

**1. Utilisation de WSL (Windows Subsystem for Linux) :**
   - Windows 10 prend en charge WSL, qui vous permet d'exécuter un environnement Linux directement sur Windows.
   - Vous pouvez installer une distribution Linux telle qu'Ubuntu via WSL et ensuite suivre les étapes d'installation de NS-3 comme si vous étiez sur un système Linux.

**2. Utilisation d'une Machine Virtuelle Linux :**
   - Vous pouvez installer une machine virtuelle (VM) avec Ubuntu sur votre système Windows à l'aide de logiciels de virtualisation comme VirtualBox ou VMware.
   - Dans la VM Ubuntu, vous pouvez installer et exécuter NS-3 comme vous le feriez sur un système Ubuntu natif.

**3. Utilisation d'Environnements de Développement Intégrés (IDE) :**
   - Certains IDE, comme Visual Studio Code, offrent des extensions qui permettent de développer et d'exécuter des projets NS-3 directement sur Windows.
   - Ces extensions peuvent fournir un environnement de développement NS-3 plus convivial pour les utilisateurs Windows.

**4. Utilisation de Docker :**
   - Docker peut être utilisé pour créer des conteneurs Linux légers qui exécutent NS-3. Cela peut vous éviter de configurer un environnement Linux complet sur votre système Windows.

Il est important de noter que bien que ces options permettent d'exécuter NS-3 sur Windows, certaines fonctionnalités ou performances spécifiques peuvent différer par rapport à un environnement Unix/Linux natif. Le choix dépend de vos préférences personnelles et de votre niveau de confort avec ces outils.

Si vous êtes prêt à investir un peu de temps, l'utilisation de WSL ou d'une VM Linux peut être une option pratique pour exécuter NS-3 sur Windows tout en bénéficiant de l'environnement Linux recommandé.
 
*Utilisation de WSL (Windows Subsystem for Linux)*

L'utilisation de WSL (Windows Subsystem for Linux) pour exécuter NS-3 sur Windows est une option pratique, car elle vous permet de créer un environnement Linux directement sur votre système Windows. Voici comment vous pouvez procéder :

**A. Installer une Distribution Linux (par exemple, Ubuntu)**

***1. Activer WSL :***
   - Assurez-vous que vous utilisez Windows 10 version 1903 ou ultérieure.
   - Ouvrez PowerShell en tant qu'administrateur et exécutez la commande suivante pour activer WSL :
     ```
     dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
     ```
   - Redémarrez votre ordinateur pour que les modifications prennent effet.
     
***2. Choisir et Installer une Distribution Linux :***
   - Dans PowerShell, exécutez la commande suivante pour installer la distribution Linux de votre choix  :
     ```
     wsl --install -d Ubuntu
     ```  
***3. Configuration de la Distribution Linux :***
   - Après l'installation, lancez la distribution Linux depuis le menu Démarrer.
   - Attendez que la configuration initiale soit effectuée. Vous devrez créer un nom d'utilisateur et un mot de passe.

***4. Utiliser la Distribution Linux via WSL :***
   - Une fois la configuration terminée, vous pouvez lancer la distribution Linux depuis le menu Démarrer à tout moment. Cela ouvrira une invite de commande Linux.

***5. Mise à Jour et Installation des Paquets :***
   - Dans la fenêtre de l'invite de commande Linux, exécutez les commandes suivantes pour mettre à jour les listes de paquets et installer les mises à jour :
     ```
     sudo apt update
     sudo apt upgrade
     ```
Maintenant que vous avez installé une distribution Linux via WSL, vous pouvez accéder à un environnement Linux complet à partir de Windows. Vous pouvez utiliser cette distribution Linux pour exécuter NS-3 et d'autres applications Linux directement sur votre système Windows. N'hésitez pas à continuer avec les étapes d'installation et de configuration de NS-3 dans cet environnement.
   

**B. Installation de NS-3 :**
   L'installation de NS-3 dans un environnement Windows via WSL (Windows Subsystem for Linux) implique essentiellement d'effectuer les mêmes étapes que vous feriez sur une machine Linux. Voici comment procéder :

***1. Ouvrir WSL :***
   - Ouvrez le menu Démarrer, recherchez la distribution Linux que vous avez installée (par exemple, Ubuntu) et lancez-la pour ouvrir l'environnement WSL.

***2. Télécharger et Extraire NS-3 :***
   - Utilisez WSL pour télécharger NS-3 depuis le terminal. Assurez-vous d'être dans le répertoire où vous souhaitez installer NS-3. Vous pouvez créer un dossier spécifique pour NS-3 en utilisant la commande `mkdir` (make directory). Par exemple :
     ```
     mkdir ns3-installation
     ```
     Créer un dossier d'installation spécifique pour NS-3 peut vous aider à garder votre environnement propre et organisé.
     
   - Téléchargez le fichier tarball NS-3 depuis le site officiel ou un miroir. Utilisez la commande `wget` pour télécharger le fichier tarball NS-3. Par exemple :
     ```
     wget https://www.nsnam.org/release/ns-allinone-3.xx.tar.bz2
     ```
   - Utilisez la commande `tar` pour extraire le contenu du tarball dans le dossier d'installation que vous avez créé. Par exemple :
     ```
     tar -xvf ns-allinone-3.xx.tar.bz2 -C ns3-installation
     ```

***3. Configurer et Compiler NS-3 :***
   - Accédez au répertoire NS-3 nouvellement créé :
     ```
     cd ns3-installation/ns-allinone-3.xx/ns-3.xx
     ```
   - Utilisez la commande `./waf configure` pour configurer NS-3.  Vous pouvez ajouter des options de configuration si nécessaire.
   - Une fois la configuration terminée, utilisez la commande `./waf` pour compiler NS-3. Cela peut prendre un certain temps en fonction de votre système.

***4. Exécuter des Exemples :***
   - Après la compilation, vous pouvez exécuter les exemples de simulation NS-3 pour vous assurer que tout fonctionne correctement. Utilisez la commande `./waf --run exemple` pour exécuter un exemple donné.

   - À partir de maintenant, vous pouvez créer et exécuter vos propres scénarios de simulation NS-3 en utilisant les fichiers de script et les commandes appropriés.
    

**C. Accès aux Fichiers :**
   - Vous pouvez accéder aux fichiers de votre système Windows depuis WSL en naviguant vers le répertoire `/mnt` (par exemple, `/mnt/c/` pour le lecteur C).
   - Vous pouvez accéder aux fichiers de votre environnement Ubuntu installé via WSL (Windows Subsystem for Linux) à partir de Windows en utilisant le chemin `/mnt`. Voici comment vous pouvez voir le contenu des fichiers dans Windows :

***1. Ouvrir l'Explorateur de Fichiers :***
   - Ouvrez l'Explorateur de fichiers sur votre système Windows.

***2. Accéder aux Fichiers WSL :***
   - Dans la barre d'adresse de l'Explorateur de fichiers, tapez le chemin `/mnt` suivi du lecteur de votre distribution Linux. Par exemple :
     - `/mnt/c` pour accéder au lecteur C.
     - `/mnt/d` pour accéder au lecteur D.
     - Et ainsi de suite.

***3. Accéder au Dossier d'Installation de NS-3 :***
   - Si vous avez créé un dossier d'installation spécifique pour NS-3 dans votre environnement Ubuntu, vous pouvez naviguer jusqu'à ce dossier en utilisant le chemin complet. Par exemple :
     - `/mnt/c/Chemin/Vers/Votre/Dossier/ns3-installation`

Une fois que vous avez accédé au dossier de votre environnement Ubuntu via l'Explorateur de fichiers Windows, vous pourrez voir et interagir avec les fichiers et dossiers de la même manière que vous le feriez dans n'importe quel autre dossier Windows. Cela peut être utile pour éditer des fichiers de script NS-3 dans un éditeur de texte Windows ou pour visualiser des résultats de simulation générés par NS-3.

L'utilisation de WSL vous permet d'exécuter NS-3 dans un environnement Linux natif sans avoir à configurer une machine virtuelle distincte. Cependant, gardez à l'esprit que WSL n'offre pas nécessairement la même performance qu'un système Linux natif, mais il devrait être suffisamment adéquat pour l'apprentissage et le développement NS-3.

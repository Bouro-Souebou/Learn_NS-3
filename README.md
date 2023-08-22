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

**B. Installer les Outils et Dépendances :**
Avant d'installer NS-3 dans votre environnement Ubuntu via WSL (Windows Subsystem for Linux), vous devrez vous assurer d'avoir les outils et dépendances nécessaires pour la compilation et l'exécution de NS-3. Voici comment vous pouvez installer ces outils et dépendances :

***1. Ouvrir le Terminal :***
   - Ouvrez votre environnement Ubuntu installé via WSL en lançant la distribution Linux à partir du menu Démarrer.

***2. Installer les Outils de Compilation :***
   - NS-3 nécessite des outils de compilation tels que le compilateur C++ et les bibliothèques de développement. Installez-les en exécutant la commande suivante :
     ```
     sudo apt install g++ build-essential
     ```

***3. Installer Python :***
   - NS-3 utilise Python pour diverses tâches. Assurez-vous d'avoir Python installé en exécutant la commande :
     ```
     sudo apt install python3
     ```

***4. Installer les Bibliothèques de Développement :***
   - NS-3 peut nécessiter certaines bibliothèques de développement pour des fonctionnalités spécifiques. Vous pouvez installer les bibliothèques de base en utilisant la commande suivante :
     ```
     sudo apt install libgtk2.0-dev libboost-all-dev
     ```
***5. Installer CMake :***
   - CMake est un outil de génération de systèmes de construction qui facilite la création, la configuration et la compilation de projets logiciels. Il est largement utilisé pour simplifier le processus de compilation et de création de projets complexes. NS-3 utilise CMake pour générer les fichiers de configuration nécessaires à la compilation de son code source. Utilisez la commande suivante pour installer CMake :
   ```
   sudo apt install cmake
   ```
***5. Installer les Autres Dépendances :***
   - Selon la version de NS-3 que vous utilisez et les fonctionnalités que vous souhaitez, d'autres dépendances pourraient être nécessaires. Consultez la documentation NS-3 pour obtenir des informations spécifiques.
   - Les dépendances spécifiques peuvent varier en fonction de la version de NS-3 que vous utilisez et des fonctionnalités que vous souhaitez utiliser. Cependant, voici quelques dépendances supplémentaires qui pourraient être nécessaires pour certaines fonctionnalités spécifiques de NS-3 ou pour la compilation de certains modules :

****a. Dépendances pour le support de Python :****
      - Si vous prévoyez d'utiliser des scripts Python avec NS-3, vous pourriez avoir besoin de certaines bibliothèques Python. Installez-les avec la commande :
     ```
     sudo apt install python3-dev python3-setuptools
     ```

****b. Bibliothèques liées à la simulation sans fil :****
      - Si vous travaillez avec des simulations sans fil, vous pourriez avoir besoin de bibliothèques supplémentaires pour la gestion des interfaces sans fil. Installez-les avec la commande :
     ```
     sudo apt install libxml2 libxml2-dev libgtk-3-dev
     ```

****c. Bibliothèques pour la visualisation graphique :****
      - Si vous prévoyez d'utiliser les fonctionnalités de visualisation graphique de NS-3, vous pourriez avoir besoin de bibliothèques graphiques. Installez-les avec la commande :
     ```
     sudo apt install gnuplot libqt5core5a libqt5gui5 libqt5widgets5 libpcap-dev
     ```

****d. Bibliothèques pour les simulations Wi-Fi :****
      - Si vous travaillez avec des simulations Wi-Fi, vous pourriez avoir besoin de bibliothèques supplémentaires pour le support Wi-Fi. Installez-les avec la commande :
     ```
     sudo apt install libnl-3-dev libnl-genl-3-dev
     ```

****e. Bibliothèques pour les simulations LTE :****
      - Si vous travaillez avec des simulations LTE, vous pourriez avoir besoin de bibliothèques supplémentaires pour le support LTE. Installez-les avec la commande :
     ```
     sudo apt install libsqlite3-dev libfftw3-dev libzmq3-dev
     ```

Assurez-vous de consulter la documentation spécifique de NS-3 pour la version que vous utilisez et pour les fonctionnalités que vous prévoyez d'exploiter. La documentation de NS-3 vous fournira des informations détaillées sur les dépendances requises pour les différents modules et fonctionnalités.

En installant ces outils et dépendances, vous vous assurez que votre environnement Ubuntu via WSL est prêt à compiler et exécuter NS-3. Après avoir installé les dépendances, vous pouvez passer à l'étape suivante, c'est-à-dire télécharger et extraire NS-3, puis configurer et compiler le logiciel conformément à la documentation.

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
**C. Configurer NS-3 :**
   - Accédez au répertoire NS-3 nouvellement créé :
     ```
     cd ns3-installation/ns-allinone-3.xx/ns-3.xx
     ```
   - Utilisez la commande `./waf configure` pour configurer NS-3. Lors de la configuration de NS-3, vous pouvez ajouter des options de configuration spécifiques en fonction de vos besoins. Ces options vous permettent de personnaliser la manière dont NS-3 sera construit et les fonctionnalités qui seront incluses dans la compilation. Voici comment vous pouvez ajouter des options de configuration lors de la configuration de NS-3 :

****1. Lancer la Configuration :****
   - Accédez au répertoire NS-3 dans votre terminal WSL (Ubuntu).
   - Utilisez la commande `./waf configure` pour commencer la configuration de NS-3.

****2. Ajouter des Options de Configuration :****
   - Vous pouvez ajouter des options de configuration en utilisant la syntaxe `--option=valeur`. Par exemple :
     ```
     ./waf configure --enable-examples --disable-tests --with-foo=/chemin/vers/quelquechose
     ```
   - Voici quelques options de configuration courantes que vous pourriez rencontrer :
     - `--enable-module` : Active un module spécifique.
     - `--disable-module` : Désactive un module spécifique.
     - `--enable-examples` : Active la construction des exemples.
     - `--disable-tests` : Désactive la construction des tests.
     - `--with-foo=/chemin/vers/quelquechose` : Spécifie un chemin pour quelque chose (par exemple, une bibliothèque externe).

****3. Vérifier les Options de Configuration et les dépendances :****
   - Une fois que vous avez ajouté vos options de configuration, vous pouvez exécuter la commande `./waf --help` pour voir la liste complète des options et pour vérifier que vos options ont été prises en compte. Une fois la configuration terminée, utilisez la commande `./waf` pour compiler NS-3.
   - Pour vérifier la version de NS-3 installée dans votre environnement Ubuntu via WSL, vous pouvez exécuter la commande suivante :

   ```
   ./waf --version
   ```

Assurez-vous d'exécuter cette commande depuis le répertoire NS-3 où vous avez configuré et compilé le logiciel. Cette commande affichera la version de NS-3 que vous avez installée.

Si vous souhaitez vérifier la version de NS-3 depuis n'importe quel répertoire, vous pouvez ajouter le chemin complet vers l'exécutable `waf` dans la commande. Par exemple :

   ```
   /chemin/vers/ns3-installation/ns-allinone-3.xx/ns-3.xx/waf --version
   ```

Remplacez "/chemin/vers/ns3-installation" par le chemin réel vers le dossier d'installation de NS-3 sur votre système.
Il n'existe pas de commande unique pour vérifier la version de toutes les dépendances de NS-3 en une seule fois. Cependant, vous pouvez vérifier la version des dépendances individuellement en utilisant des commandes spécifiques à chaque bibliothèque ou outil. Voici quelques exemples de commandes que vous pouvez utiliser pour vérifier la version de certaines dépendances courantes :

      ```Vérification de la Version de Python
      python3 --version
      ```
      
      ```Vérification de la Version de G++ (Compilateur C++)
      g++ --version
      ```
      ```Vérification de la Version du Système de construction (cmake)
      cmake --version
      ```
      
      
      ```Vérification de la Version de Boost
      dpkg -l | grep libboost
      ```
      
      ```Vérification de la Version de libxml2
      dpkg -l | grep libxml2
      ```
      
      ```Vérification de la Version de libpcap
      dpkg -l | grep libpcap
      ```
      
      ```Vérification de la Version de libnl
      dpkg -l | grep libnl
      ```
      ```Vérification de la Version de libsqlite3
      dpkg -l | grep libsqlite3
      ```


**D. Compiler NS-3 :**
   - Une fois la configuration terminée, utilisez la commande `./waf` pour compiler NS-3. Cela peut prendre un certain temps en fonction de votre système.

**E. Exécuter des Exemples :**
   - Après la compilation, vous pouvez exécuter les exemples de simulation NS-3 pour vous assurer que tout fonctionne correctement. Utilisez la commande `./waf --run exemple` pour exécuter un exemple donné.

   - À partir de maintenant, vous pouvez créer et exécuter vos propres scénarios de simulation NS-3 en utilisant les fichiers de script et les commandes appropriés.
    
**F. Accès aux Fichiers :**
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

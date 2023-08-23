*Exemples de simulateurs de réseau de capteurs sans fil pour différentes approches de simulation :*

**1. Simulation à Événements Discrets :**
   - **NS-3 (Network Simulator 3)** : NS-3 est un exemple de simulateur à événements discrets très utilisé. Il permet de modéliser les réseaux de capteurs sans fil en simulant des événements discrets tels que les envois de paquets, les réceptions, les collisions, etc. Il prend en compte le comportement des nœuds capteurs, les protocoles de communication et les interactions entre les entités du réseau. En résumé, l'expression "réseau à événements discrets" décrit la façon dont le simulateur de réseau gère le temps et les interactions dans le système modélisé, en se concentrant sur des moments spécifiques où des événements significatifs se produisent plutôt que sur un flux de temps continu.

**2. Modélisation Continue :**
   - **OMNeT++** : OMNeT++ est un simulateur de réseau basé sur une modélisation à composants où le temps est considéré comme un continuum. Il permet de modéliser des réseaux de capteurs avec des composants continus et discrets, ce qui est utile pour simuler des phénomènes qui varient de manière continue.

**3. Simulateurs basés sur des Équations Différentielles :**
   - **Matlab/Simulink** : Matlab et Simulink sont largement utilisés pour modéliser et simuler des systèmes basés sur des équations différentielles. Ils peuvent être utilisés pour modéliser des capteurs, des réseaux de capteurs et des comportements complexes basés sur des équations de taux de changement.

**4. Simulation basée sur des Règles :**
   - **SwarmSim** : SwarmSim est un simulateur basé sur des règles conçu pour modéliser des comportements d'essaim et de réseau de capteurs. Il permet de définir des règles individuelles pour chaque nœud capteur et d'observer comment ces règles influencent le comportement global du réseau.

**5. Modélisation basée sur des Automates :**
   - **Cellular Automata Sensor Network Simulator (CA-SNS)** : CA-SNS est un simulateur qui utilise des automates cellulaires pour modéliser le comportement des nœuds capteurs et des interactions dans un réseau de capteurs. Les automates cellulaires permettent de représenter les états des nœuds et les transitions entre eux.

**6. Modélisation basée sur des Réseaux de Petri :**
   - **Petri-NS (Petri Net Simulator)** : Petri-NS est un exemple de simulateur basé sur des réseaux de Petri pour modéliser des réseaux de capteurs. Il permet de définir les places, les transitions et les règles de transition pour modéliser le comportement des nœuds et des communications dans le réseau.

Chacun de ces simulateurs utilise une approche différente pour modéliser les réseaux de capteurs sans fil en fonction de la méthode de simulation choisie. Le choix du simulateur dépend des spécificités de votre projet, de vos besoins de simulation et du niveau de détail que vous recherchez.

*NS-3 (Network Simulator 3)*

NS-3 est principalement développé pour les systèmes basés sur Unix/Linux, ce qui signifie qu'il peut être plus facile d'installer et d'utiliser NS-3 sur un environnement Unix/Linux tel qu'Ubuntu. Cependant, il existe des moyens d'exécuter NS-3 sur [Windows](https://www.nsnam.org/docs/installation/html/windows.html) sans avoir besoin d'une machine virtuelle Ubuntu. Voici quelques options que vous pouvez envisager :

**1. Utilisation de [WSL](https://learn.microsoft.com/en-us/windows/wsl/) (Windows Subsystem for Linux) :**
   - Windows 10 prend en charge [WSL](https://learn.microsoft.com/en-us/windows/wsl/), qui vous permet d'exécuter un environnement Linux directement sur Windows.
   - Vous pouvez installer une distribution Linux telle qu'Ubuntu via WSL et ensuite suivre les étapes d'installation de NS-3 comme si vous étiez sur un système Linux.

**2. Utilisation d'une Machine Virtuelle Linux :**
   - Vous pouvez installer une machine virtuelle (VM) avec Ubuntu sur votre système Windows à l'aide de logiciels de virtualisation comme VirtualBox ou VMware.
   - Dans la VM Ubuntu, vous pouvez installer et exécuter NS-3 comme vous le feriez sur un système Ubuntu natif.

**3. Utilisation d'Environnements de Développement Intégrés (IDE) :**
   - Certains IDE, comme [Visual Studio Code](https://code.visualstudio.com/docs/remote/wsl), offrent des extensions qui permettent de développer et d'exécuter des projets NS-3 directement sur Windows.
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
Maintenant que vous avez installé une distribution Linux via WSL, vous pouvez accéder à un environnement Linux complet à partir de Windows. Vous pouvez utiliser cette distribution Linux pour exécuter NS-3 et d'autres applications Linux directement sur votre système Windows. Pour en savoir plus sur [Les commandes de base en console linux](https://doc.ubuntu-fr.org/tutoriel/console_commandes_de_base#les_commandes_de_base_en_console_linux) N'hésitez pas à continuer avec les étapes d'installation et de configuration de NS-3 dans cet environnement.

**B. Installer les Outils et Dépendances :**

Avant d'installer NS-3 dans votre environnement Ubuntu via WSL (Windows Subsystem for Linux), vous devrez vous assurer d'avoir les outils et dépendances nécessaires pour la compilation et l'exécution de NS-3. Les scripts dans ns-3 sont réalisés en C++ ou Python. La plupart de l' API ns-3 est disponible en Python, mais les modèles sont écrits en C++ dans les deux cas. Voici comment vous pouvez installer ces outils et dépendances :

***1. Ouvrir le Terminal :***
   - Ouvrez votre environnement Ubuntu installé via WSL en lançant la distribution Linux à partir du menu Démarrer.

***2. Installer les Outils de Compilation :***
   - NS-3 nécessite des outils de compilation tels que le compilateur C++ et les bibliothèques de développement. Installez-les en exécutant la commande suivante :
     ```
     sudo apt install g++ build-essential
     ```
Si vous êtes nouveau en C++, [Une connaissance pratique du C++ et des concepts orientés objet](https://cplusplus.com/doc/tutorial/)

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
   - CMake est un outil de génération de systèmes de construction qui facilite la création, la configuration et la compilation de projets logiciels. Il est largement utilisé pour simplifier le processus de compilation et de création de projets complexes. Pour les détails de CMake, les documents CMake sont disponibles [ici](https://cmake.org/cmake/help/latest/index.html) ou le [code](https://gitlab.kitware.com/cmake/cmake). NS-3 utilise CMake pour générer les fichiers de configuration nécessaires à la compilation de son code source. Utilisez la commande suivante pour installer CMake :
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

**C. Installation de NS-3 :**
   L'installation de NS-3 dans un environnement Windows via WSL (Windows Subsystem for Linux) implique essentiellement d'effectuer les mêmes étapes que vous feriez sur une machine Linux. Voici comment procéder :

***1. Ouvrir WSL :***
   - Ouvrez le menu Démarrer, recherchez la distribution Linux que vous avez installée (par exemple, Ubuntu) et lancez-la pour ouvrir l'environnement WSL.

***2. Télécharger et Extraire NS-3 :***
   - Utilisez WSL pour télécharger NS-3 depuis le terminal. Assurez-vous d'être dans le répertoire où vous souhaitez installer NS-3. Vous pouvez créer un dossier spécifique pour NS-3 en utilisant la commande `mkdir` (make directory). Par exemple :
     ```
     mkdir ns3-installation
     ```
     Créer un dossier d'installation spécifique pour NS-3 peut vous aider à garder votre environnement propre et organisé. Accedez au dossier crée : 
     ```
     cd ns3-installation
     ```
     
   - Téléchargez le fichier tarball NS-3 depuis le site officiel ou un miroir. Utilisez la commande `wget` (un outil de ligne de commande pour récupérer des objets sur le Web) pour télécharger le fichier tarball NS-3. Par exemple :
     ```
     wget https://www.nsnam.org/releases/ns-allinone-3.39.tar.bz2
     ```
   - Utilisez la commande `tar` pour extraire le contenu du tarball dans le dossier d'installation que vous avez créé. Par exemple :
     ```
     tar -xvf ns-allinone-3.39.tar.bz2
     ```
- si vous accédez au répertoire ns-allinone-3.39 `cd ns-allinone-3.39` puis `ls`, vous devriez voir un certain nombre de fichiers et de répertoires : `README.md  bake  build.py  constants.py  netanim-3.109  ns-3.39  util.py`

*Bâtiment ns-3* 
Dans le contexte de NS-3 (Network Simulator 3), le processus de build consiste à configurer et compiler le code source de NS-3 afin de générer les exécutables nécessaires pour exécuter des simulations de réseaux. La configuration et la compilation sont gérées à l'aide d'outils comme CMake, qui permettent de définir des options, de gérer les dépendances et de générer les fichiers de construction nécessaires.

En général, pour configurer et construire NS-3, vous devrez suivre des étapes spécifiques en utilisant le système de construction CMake. Voici les étapes typiques que vous devriez suivre pour configurer et construire NS-3 :

**D. Construire NS-3**
CMake doit être installé avant de construire ns-3

***1. Accéder au Répertoire NS-3 :***
   - Ouvrez votre terminal dans l'environnement Ubuntu via WSL.
   - Naviguez vers le répertoire NS-3 où vous avez extrait les fichiers source de NS-3.
     ```
     cd ns3-installation/ns-allinone-3.39
     ```
   - Le script build.py disponible dans le repertoire peut orchestrer une construction simple de composants. 
     ```
     ./build.py --enable-examples --enable-tests
     ```
     les arguments de build.py lui disent de construire des exemples et des tests. Le programme construit également par défaut tous les modules disponibles. Plus tard, vous pourrez construire ns-3 sans exemples ni tests, ou éliminer les modules qui ne sont pas nécessaires à votre travail, si vous le souhaitez.
     Pour continuer, veuillez acceder au répertoire ns-3.39. 
     ```
     cd ns-3.39
     ```
***3. Construire avec le wrapper ns3 CMake :***
- Nettoyez la version précédente n'est généralement pas strictement nécessaire mais constitue une bonne pratique
     ```
     ./ns3 clean
     ```
  cela supprimera les bibliothèques et les fichiers objets précédemment construits trouvés dans le répertoire build/
  - Pour indiquer à ns-3 qu'il doit effectuer des builds optimisés incluant les exemples et les tests, vous devrez exécuter les commandes suivantes :
     ```
     ./ns3 configure --build-profile=optimized --enable-examples --enable-tests
     ```
  - Certaines options ns-3 ne sont pas activées par défaut ou nécessitent la prise en charge du système sous-jacent pour fonctionner correctement ( ). D'autres options peuvent dépendre de bibliothèques tierces qui, si elles ne sont pas trouvées, seront désactivées ( ).
  - Maintenant, continuez et revenez à la version de débogage qui inclut les exemples et les tests.
     ```
     ./ns3 clean
     ```
  - 
     ```
     ./ns3 configure --build-profile=debug --enable-examples --enable-tests
     ```
  - Le système de build est maintenant configuré et vous pouvez construire les versions de débogage des programmes ns-3 en tapant simplement :
     ```
     ./ns3 build
     ```
  - Bien que les étapes ci-dessus vous aient obligé à créer deux fois la partie ns-3 du système, vous savez maintenant comment modifier la configuration et créer du code optimisé.
  - Une commande existe pour vérifier quel profil est actuellement actif pour un projet déjà configuré :
     ```
     ./ns3 show profile
     ```
**E. Test de ns-3 :**
Vous pouvez exécuter les tests unitaires de la distribution ns-3 en exécutant le script ./test.py :
     ```
     ./test.py --no-build
     ```
 `Running without Building` : Les commandes `./test.py --no-build` et `./test.py` sont liées à l'exécution des tests dans un projet logiciel. L'option `--no-build`, signifie que les tests ne seront pas reconstruits avant leur exécution. Cela peut être utile lorsque vous avez déjà compilé et construit les tests auparavant, et que vous souhaitez simplement les exécuter à nouveau sans passer par la phase de construction.Ce qui est important est que la ligne récapitulative à la fin indique que tous les tests ont réussi ; aucun n'a échoué ou ne s'est écrasé. 
 
**F. Exécuter des Exemples (un script) :**
   - Pour exécuter un programme, utilisez simplement l'option `--run` dans ns3. Exécutons l' équivalent ns-3 du programme omniprésent `hello world` en tapant ce qui suit :
     ```
     ./ns3 run hello-simulator
     ```    
   - À partir de maintenant, vous pouvez créer et exécuter vos propres scénarios de simulation NS-3 en utilisant les fichiers de script et les commandes appropriés.
   - 
***1. Arguments du programme / Paramètres d'Exécution (Facultatif):***
   - Pour transmettre des arguments de ligne de commande à un programme ns-3, utilisez ce modèle :
```
./ns3 run <ns3-program> --command-template="%s <args>"
ou
./ns3 run '<ns3-program> --arg1=value1 --arg2=value2 ...'
ou
./ns3 run '<ns3-program> --arg1=value1 --arg2=value2 ...' --no-build
```
   - Pour appeler `test-runner` directement pour un seul test :
```
./ns3 run test-runner --command-template="%s --help"
```

***2. Débogage  :***
- Pour exécuter des programmes ns-3 sous le contrôle d'un autre utilitaire, tel qu'un débogueur ( par exemple gdb ) ou un vérificateur de mémoire ( par exemple valgrind ), vous utilisez un --command-template="..." :
  ```
  ./ns3 run hello-simulator --command-template="gdb %s --args <args>"
  ```
  - On peut combiner cette recette et la précédente pour faire un test sous le débogueur :
    ```
    ./ns3 run test-runner --command-template="gdb %s --args --suite=mytest --verbose"
    ```

****3. Visualiser les Résultats :****
   - Après avoir exécuté un exemple de simulation, vous pouvez consulter les fichiers de sortie ou de journalisation générés pour voir les résultats de la simulation.

****4. Explorer d'autres Exemples :****
   - NS-3 propose de nombreux autres exemples de simulation dans divers domaines. Explorez le répertoire des exemples pour en savoir plus sur les fonctionnalités de NS-3.
 
**G. Accès aux Fichiers :**
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



***3. Vérifier les Options de Configuration et les dépendances :***
   
Il n'existe pas de commande unique pour vérifier la version de toutes les dépendances de NS-3 en une seule fois. Cependant, vous pouvez vérifier la version des dépendances individuellement en utilisant des commandes spécifiques à chaque bibliothèque ou outil. Voici quelques exemples de commandes que vous pouvez utiliser pour vérifier la version de certaines dépendances courantes :
    - Vérification de la Version de Python
      ```
      python3 --version
      ```
    - Vérification de la Version de G++ (Compilateur C++)  
      ```
      g++ --version
      ```
      - Vérification de la Version du Système de construction (cmake)
      ```
      cmake --version
      ```
      - Vérification de la Version de Boost
      ```
      dpkg -l | grep libboost
      ```
      - Vérification de la Version de libxml2
      ```
      dpkg -l | grep libxml2
      ```
      - Vérification de la Version de libpcap
      ```
      dpkg -l | grep libpcap
      ```
      - Vérification de la Version de libnl
      ```
      dpkg -l | grep libnl
      ```
      - Vérification de la Version de libsqlite3
      ```
      dpkg -l | grep libsqlite3
      ```

*Programmation des sockets*
Pour un bon aperçu de [la programmation des sockets TCP/IP](https://shop.elsevier.com/books/tcp-ip-sockets-in-c/donahoo/978-0-12-374540-8)
La source des exemples du livre [ici](http://cs.baylor.edu/~donahoo/practical/CSockets/)
Un livre sur [les sockets multicast](https://shop.elsevier.com/books/multicast-sockets/makofske/978-1-55860-846-7)

*Profil de build*
Dans le contexte du développement logiciel et de la construction de projets, un "profil de build" fait référence à un ensemble spécifique de configurations et d'options de compilation utilisées pour générer une version spécifique d'un logiciel. Chaque profil de build peut être conçu pour répondre à des besoins particuliers, tels que la génération d'une version de production, d'une version de débogage, d'une version optimisée, etc.

Les profils de build permettent aux développeurs de personnaliser la manière dont le logiciel est construit en fonction des objectifs du projet et des conditions d'utilisation. Voici quelques exemples courants de profils de build :

1. **Release :** Le profil de build de version finale destiné à la distribution. Il est généralement optimisé pour la performance et ne contient pas d'informations de débogage. C'est la version que les utilisateurs finaux installeront.

2. **Debug :** Le profil de build utilisé pour le débogage. Il peut inclure des informations de débogage, des assertions et des vérifications supplémentaires pour faciliter la recherche et la correction d'erreurs.

3. **Optimized :** Un profil de build optimisé pour les performances, généralement utilisé pour les tests de performance. Les optimisations de compilation sont activées pour améliorer les performances du logiciel.

4. **Test :** Un profil de build pour exécuter des tests unitaires ou de validation. Il peut inclure des informations de débogage supplémentaires pour faciliter l'identification des erreurs lors des tests.

5. **Profile :** Un profil de build utilisé pour la profilage de performance, visant à identifier les parties du code qui consomment le plus de ressources.

6. **Minimal :** Un profil de build minimal qui ne compile que le strict minimum nécessaire. Cela peut être utile pour créer des versions légères du logiciel.

Chaque profil de build peut être configuré avec différentes options de compilation, de liaisons de bibliothèques et d'autres paramètres en fonction des besoins. En utilisant des profils de build, les développeurs peuvent facilement générer différentes versions du logiciel pour différentes fins sans avoir à réajuster les options à chaque fois.
 - Si vous avez du code qui ne doit s'exécuter que dans des profils de build spécifiques, utilisez la macro Code Wrapper indiquée :
```
NS_BUILD_DEBUG(std::cout << "Part of an output line..." << std::flush; timer.Start());
DoLongInvolvedComputation();
NS_BUILD_DEBUG(timer.Stop(); std::cout << "Done: " << timer << std::endl;)
```
 - La combinaison d'un répertoire de sortie différent avec l'option `--out`  avec des profils de build vous permet de basculer entre les différentes options de compilation de manière claire :
```
./ns3 configure --build-profile=debug --out=build/debug
./ns3 build
...
./ns3 configure --build-profile=optimized --out=build/optimized
./ns3 build
...
```
 - Lorsque vous changez de profil de build comme celui-ci, vous devez faire attention à donner les mêmes paramètres de configuration à chaque fois. Il peut être pratique de définir certaines variables d'environnement pour vous aider à éviter les erreurs :
```
$ export NS3CONFIG="--enable-examples --enable-tests"
$ export NS3DEBUG="--build-profile=debug --out=build/debug"
$ export NS3OPT=="--build-profile=optimized --out=build/optimized"

$ ./ns3 configure $NS3CONFIG $NS3DEBUG
$ ./ns3 build
...
$ ./ns3 configure $NS3CONFIG $NS3OPT
$ ./ns3 build
```
 - 


*Conceptual Overview*

     **Noeud**
     
     Dans ns-3, l'abstraction de base du dispositif informatique est appelée le nœud. La `class Node` fournit des méthodes pour gérer les représentations de dispositifs informatiques dans les simulations.
     
     **Application**
      - **Système logiciel (System Software) :**  la mémoire, les cycles du processeur, le disque, le réseau, etc.
      - **Application logiciel ( application software ) :** acquiert et utilise les ressources contrôlées par le logiciel système pour atteindre un objectif.
      - Tout comme les applications logicielles s'exécutent sur des ordinateurs pour effectuer des tâches dans le « monde réel », les applications ns-3 s'exécutent sur ns-3 Nodes pour piloter des simulations dans le monde simulé.
     Dans ns-3, l'abstraction de base pour un programme utilisateur qui génère une activité à simuler est l'application. Cette abstraction est représentée en C++ par la  `classe Application`.
     
     **Channel(Cannal)**
     
         Dans le monde simulé de ns-3 , on connecte un Node à un objet représentant un canal de communication. Ici, l'abstraction de base du sous-réseau de communication est appelée le canal et est représentée en C++ par la `classe Channel`.
         
         **Périphérique Internet(Net Device)**
         
         Dans ns-3 , l' abstraction Net Device couvre à la fois le pilote logiciel et le matériel simulé. Un Net Device est « installé » dans un Node afin de permettre au Node de communiquer avec les autres Nodes dans la simulation via Channels. Tout comme dans un ordinateur réel, un Node peut être connecté à plusieurs Channel via plusieurs fichiers NetDevices.
         
         L'abstraction du périphérique réseau est représentée en C++ par la `classe NetDevice`. La class NetDevice fournit des méthodes pour gérer les connexions des objets Node et Channel ; et peut être spécialisé par les développeurs dans le sens de la programmation orientée objet. Il y a différentes versions spécialisées de NetDevice, `CsmaNetDevice, PointToPointNetDeviceet WifiNetDevicedans`. Tout comme une carte réseau Ethernet est conçue pour fonctionner avec un réseau Ethernet, la CsmaNetDeviceest conçue pour fonctionner avec un CsmaChannel; le PointToPointNetDeviceest conçu pour fonctionner avec a PointToPointChannelet a WifiNetDeviceest conçu pour fonctionner avec a WifiChannel.

*Un premier script ns-3 *

- Accédez au `examples/tutorial` répertoire. Vous devriez voir un fichier nommé `first.cc` . Il s'agit d'un script qui créera un simple lien point à point entre deux nœuds et fera écho à un seul paquet entre les nœuds.
- 

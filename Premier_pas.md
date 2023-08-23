*Noeud*
Dans ns-3, l'abstraction de base du dispositif informatique est appelée le nœud. La `class Node` fournit des méthodes pour gérer les représentations de dispositifs informatiques dans les simulations.

*Application*
 - **Système logiciel (System Software) :**  la mémoire, les cycles du processeur, le disque, le réseau, etc.
 - **Application logiciel ( application software ) :** acquiert et utilise les ressources contrôlées par le logiciel système pour atteindre un objectif.
 - Tout comme les applications logicielles s'exécutent sur des ordinateurs pour effectuer des tâches dans le « monde réel », les applications ns-3 s'exécutent sur ns-3 Nodes pour piloter des simulations dans le monde simulé.
Dans ns-3, l'abstraction de base pour un programme utilisateur qui génère une activité à simuler est l'application. Cette abstraction est représentée en C++ par la  `classe Application`.

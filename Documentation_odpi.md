Utilisation d'odpic
===================

Pour utiliser odpic, il y a deux trois étapes à faire pour que celui soit fonctionnel

Pré requis
----------

- Réaliser un git clone du dépot dans un terminal : ````git clone https://github.com/oracle/odpi.git````
- Dans le terminal, Il faut se rendre dans le dossier puis taper la commande ````make```` puis ```make install```
- Il faut conserver les élements dans lib/

Avec gcc
-------- 

il suffit lors de la compilation de mettre les opitions ```-L/path_to_repository/lib/ -lodpic```

Exemple de commande : ```gcc main.c -o main.o -L~/Downloads/odpi-master/lib/ -lodpic```


Avec clang
---------- 

il suffit lors de la compilation de mettre les opitions ```-L/path_to_repository/lib/ -lodpic```

- Exemple de commande : ``` clang main.c -o main.o -L~/Downloads/odpi-master/lib/ -lodpic```

Avec cLion
----------

- Le plus simple consiste à copier le contenu du dossier ```odpi-master/lib``` généré dans le dossier  ```/usr/local/lib/```.
- Puis dans la CMakeListes.txt, il faut ajouter la ligne : ```target_link_libraries(C "-lodpic")```
Dans notre cas, C correspond à ce qu'il y a entre parenthèse dans la ligne project(C C)

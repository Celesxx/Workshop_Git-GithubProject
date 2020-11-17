# Workshop_Git-GithubProject

Introduction : 
What is Git ?

What is Github ?

What is Github Project ?

Vous incarnerez 🐒.

Step 0 : Création du projet
===
🐒 Décide de créer un super site web dont le code source serait hébergé sur Github.

- Créer un *repository* Github en y ajoutant le code que 🐎 lui a donné directement depuis la page du repository. (Readme, gitignore ?)

- Se rendre dans la partie *projet* et en créer un nouveau. (Template ?)

- Créer des notes / issues


Step 1 - Récupérer le repository en local
===
🐒 Est prêt à coder son site, pour ça il *clone* son projet sur son PC.
```console
rafale@workshop:~$ git clone <SSH KEY>
``` 

2 - Intéragir avec les modifications apportées au repository
===
🐒 Apporte des modifications à son projet mais a oublié quels fichiers ont été modifiés, il se demande quelle commande pourrait l'aider à s'en rappeler.
```console
rafale@workshop:~$ git diff <FILE PATH || SOURCE BRANCH>
```
🐒 Aimerait maintenant savoir quelles modifications ont été apportées aux fichiers, quelle commande utiliser ?
```console
rafale@workshop:~$ git diff <FILE PATH || SOURCE BRANCH>
```
🐒 N'a plus envie d'apporter des modifications à son README, il cherche la commande pour remettre ce fichier à son état d'origine.
```console
rafale@workshop:~$ git checkout <FILE PATH>
```
🐒 Est sous Max OS, un *.DS_Store* a été crée, il pourrait le supprimer à main mais en tant que bon développeur il se demande comment faire en sorte que ce fichier n'intéragisse jamais avec git, comment faire ?
```console
rafale@workshop:~$ cat .gitignore
```
    /node_modules   #Indique que le dossier node_modules ne sera pas pris en compte par git

    *.log   #Indique que tous les fichiers ayant pour extension .log ne seont pas pris en compte par git
    
    .DS_Store   #Indique que le fichier DS_Store ne sera pas pris en compte par git

3 - Envoyer des modifications
===
🐒 Est maintenant satisfait de son travail, il aimerait *ajouter* ses fichiers.
```console
rafale@workshop:~$ git add <FILE PATH>
rafale@workshop:~$ git add -A
```
🐒 Se change d'avis et décide de ne plus ajouter ses fichiers.
```console
rafale@workshop:~$ git reset <FILE PATH>
rafale@workshop:~$ git reset
```
🐒 Rechange d'avis et ajoute ses fichiers et décide de les envoyer sur Github. (Commit name)
```console
rafale@workshop:~$ git commit -m <COMMIT MESSAGE>
rafale@workshop:~$ git push <BRANCH NAME>
```

4 - Récupérer des modifications
===
🐒 Décide de modifier son site directement depuis la page de son repository sur Github.
Il continue aussi d'apporter des modifications depuis son PC sans les ajouter, commit et push.
Il a quasiment fini la feature sur laquelle il travaillait mais aimerait récupérer ce qu'il a fait sur Github, quelle serait la commande à utiliser ?
```console
rafale@workshop:~$ git pull <BRANCH NAME>
```
🐒 Pense avoir bien fait mais git lui demande de *commit* avant de pourvoir récupérer les modifications, hors il n'a pas envie de commit avant d'avoir récupéré son travail, il décite donc de mettre son travail en local de côté le temps de récupérer son travail en local.
```console
rafale@workshop:~$ git stash
rafale@workshop:~$ git pull <BRANCH NAME>
rafale@workshop:~$ git stash pop
```
(Merge ?)

5 - Revenir en arrière
===
🐒 Ne se rappelle plus de tout le travail qu'il a fait, il sait qu'une commande git existe pour avoir accès à ses commits mais laquelle ?
```console
rafale@workshop:~$ git log
```
🐒 Est nostalegique et aimerait revenir à l'époque où Diablox9 était plus connu que Kim Glow, il aimerait donc revenir à son premier commit, quelle serait la commande à utiliser ?
```console
rafale@workshop:~$ git checkout <COMMIT ID>
rafale@workshop:~$ git switch - #Pour revenir à la dernière version
```

6 - Travailler avec des branches
===
```console
rafale@workshop:~$ git branch
```
```console
rafale@workshop:~$ git checkout <BRANCH NAME>
```
```console
rafale@workshop:~$ git fetch
```
```console
rafale@workshop:~$ git merge
```
```console
rafale@workshop:~$ git rebase
```

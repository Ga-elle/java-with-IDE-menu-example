# MyMenu project for Java Bases course on OpenClassrooms

## Java history

Quand on parle de Java, on ne parle pas seulement du langage mais aussi de tout l'écosystème qui va autour. Des centaines d'outils associés à Java en font l'un des 3 grands piliers du Backend web. Parmi ces piliers on trouve :

+ l'écosystème Java ;
+ les technologies Microsoft .NET ;
+ le reste : PHP, NodeJS, Ruby, etc.

+ Langage  compilé : C, C++
+ Langage interprété : code lu ligne par ligne, et exécution au fur et à mesure (python, javascript, php)
+ Langage intermédiaire : java. Il est pseudo-compilé et ensuite lu par un interpréteur.

### C'est quoi la JVM ?

Le pseudo-langage en Java s'appelle le ByteCode. L'interpréteur Java s'appelle la Java Virtual Machine (JVM). Cet interpréteur comprend de nombreux outils :
+ un interpréteur de ByteCode ;
+ un outil de gestion de la mémoire ;
+ un ensemble de fonctionnalités déjà codées ;
+ un optimiseur de code.

## Installation

### Variables d'environnement

+ JAVA_HOME
+ _JAVA_OPTIONS="-Djavax.net.ssl.trustStore=<path vers le certificat>"
+ PATH

### Modules

Si dans l'import d'un module, le module n'est pas reconnu par IntelliJ, il faut l'ajouter.
Par exemple, si `import org.junit.jupyter.api.Tests;` est non reconnu, cliquer sur `junit`et faire `alt`+ `entrée` un court instant, puis faire *Add Junit5.0 to classpath*.


### Pop up server certificates

To get rid of the pop up message go to below location and click on Accept non-trusted certificates automatically.

File | Settings | Tools | Server Certificates for Windows and Linux


## Development 

### Unitary tests

Une bonne pratique est le Test Driven Development (coder les tests avant les fonctions).
Lors de l'écriture d'un test, utiliser la méthode du "Given/When/Then": étant donné les inputs, quand je fais telle action alors, ...

### Ajouter rapidement une fonction main()

Saisir `psvm` (pour public static void main), puis Entrée : cela va automatiquement créer une nouvelle méthode main.

### Retour à la ligne

Sur Windows, sur Linux et sur Mac OS X, le retour à la ligne ne s'affiche pas de la même façon.

Il y a un mécanisme prévu dans Java pour gérer pour ce problème. 
En mettant  `%n`  dans une variable  String  puis en utilisant  `String.format`  sur cette variable, 
cela va automatiquement transformer  `%n`  en  `\n`  ou  `\r\n`  selon le système d'exploitation.

## Quick usages

### Exécutez facilement le code 

> Flèche verte à côté de la fonction > Run Main()

### Exporter le programme

> File > Project structure > Artifacts > JAR > From modules with dependencies
> Cliquer sur les 3 petits points de la classe principale (Main Class), choisir la main class dans Project et faire OK.
L'artifact est créé.

Pour créer le fichier .jar, aller dans 
> Build > Build artifacts > HelloWorld:jar > Build
Le jar apparait dans le répertoire out, il peut être exécuté en faisant clic droit.
Il peut aussi être exécuté en ligne de commande:
```
java -jar out/artifacts/HelloWorld_jar/HelloWorld.jar 
```
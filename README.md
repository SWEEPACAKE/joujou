# Procédure de démarrage d'un projet Angular
## Prérequis
- WSL2 avec Ubuntu
- Node v20+
- npm v11+
- Angular CLI v21+










```
npm i @angular/cli
```






## Démarrer un projet

```
ng new nomDuProjet
```

Puis choisir le moteur CSS que l'on veut, si on veut le SSR, et si on veut une IA pour nous assister pendant le développement. 

```
cd nomDuProjet/
```

Dans le fichier tsconfig.json, il peut-être utile d'ajouter la propriété suivante dans **compilerOptions** si l'on souhaite initialiser des propriétés de classe sans leur assigner de valeurs : 
```
"strictPropertyInitialization": false
```

## Créer un composant
```
ng generate component nomDuComposant
```
Ou alors 
```
ng g c nomDuComposant
```
On peut lui donner un chemin si on souhaite ranger nos composants, comme par exemple : 
```
ng generate component mesComposants/nomDuComposant
```


## Créer un service
```
ng generate service nomDuService
```
Ou alors 
```
ng g s nomDuService
```
On peut lui donner un chemin si on souhaite ranger nos services, comme par exemple : 
```
ng generate service mesServices/nomDuService
```

## Compiler le projet pour le développement
Cette commande devrait vous ouvrir l'appli directement sur le navigateur à l'adresse [http://localhost:4200](https://), si le build a fonctionné. Si il n'a pas fonctionné, consultez les erreurs potentielles dans le terminal pour débuguer

```
ng serve --open
```


## Compiler le projet pour la prod

Cette commande va générer un build du projet qu'elle va stocker dans le répertoire dist/votreAppli/browser. Ce répertoire contiendra un fichier index.html et les fichiers CSS et JavaScript générés. Ils seront prêts à être déployés tels quels sur un serveur web. Pour plus d'informations, voir : [https://angular.dev/tools/cli/deployment#automatic-deployment-with-the-cli](https://)
```
ng build
```

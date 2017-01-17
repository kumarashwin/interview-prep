#Questions générales

##Moi:
**Présentez-vous!**
> C'est moi qui a créé le site web *jeveuxcodermaville.com* pour accompagner ma candidature et pour vous démontrer ma motivation pour ce poste.
 
> Vous pouvez trouver des informations professionnelles et personnelles à mon propos dans les premiers billets de mon blogue, mais en résumé: J'ai développé un intérêt pour le français et ensuite j'ai été charmé par la ville de Montréal quand j'ai visité en 2013. Donc, je suis déménagé en 2014 pour m'installer à Montréal définitivement.

**Quels sont vos objectifs?**
> Mon but c'est d'obtenir un travail stable où je peux continuer à m'améliorer de façon professionnelle et personnelle; où je peux contribuer à quelque chose que je trouve important pour la société. Je cherche un travail qui peut me faire évoluer, et pas seulement sur le plan financier.

**Quelles sont vos qualités?**
**Quelles sont vos faiblesses?**
> Premièrement, le français n'est pas ma langue maternelle. Cela dit, ça m'a pas empêché de travailler dans un centre d'appel, majoritairement en français. J'ai parfois besoin de plus de temps pour bien m'exprimer mais je comprends très bien quand on me parle.

> Deuxièmement, j'ai encore du mal à estimer combien de temps va me prendre une tâche de programmation. Même ma copine est d'accord. En fait c'est une des raisons pour laquelle j'ai entrepris mon projet de programmation le plus important: une application de gestion du temps.

**Qu’est-ce qui est le plus important dans votre vie ?**
**Pourquoi avez-vous quitté votre emploi?**
**Qu’avez-vous fait depuis votre dernier emploi ?**
**Quel poste aimeriez-vous occuper dans 5 ans ?**
**Pourquoi changez-vous d'emploi constamment ?**

##Eux:
**Pourquoi voulez-vous travailler ici?**
**Que connaissez-vous de notre organisation ?**
**Pouvez-vous me préciser ce que vous avez compris du poste ?**
**Qu’est ce qui selon vous va vous poser des difficultés à ce poste ?**
**Vous n’avez aucune expérience dans ce domaine.**
**Pourquoi devrait-on vous embaucher? Pourquoi vous et pas les autres candidats?**

##Travail:
**Comment travaillez-vous en équipe ? Comment réglez-vous des problèmes avec un collègue? Donnez un exemple vécu.**
**De quoi êtes-vous le plus fier (dernier emploi) ?**
**De quoi êtes-vous le plus fier (carrière) ?**
**Quand étiez-vous le plus satisfait dans votre emploi?**
**Trois choses positives que votre employeur précédent dirait?**

##D'autres:
**Disponibilité?**
> Comme je n'ai pas d'emploi présentement, je peux commencer d'ici quelques jours si vous en avez besoin. Toutefois, comme j'ai étudié presque sans arrêt pendant les 8 derniers mois, je préfèrerais une pause de quelques semaines avant le début de mon emploi, pour arriver frais et dispo. Comme je suis très enthousiaste à travailler dans votre équipe, je suis prêt à en discuter avec vous pour trouver une date qui soit optimale pour tous.  

**Avez-vous des questions à nous poser ?**


#Questions techniques

##Web:
**Quelle est la difference entre les protocoles sans statut et ceux avec statut?**
>Un protocole de communication sans statut traite chaque demande comme une transaction independente. Donc, le serveur n’a pas besoin de conserver la session, l’identité de l’utilisateur, ou l’information concernant la nature de multiples demandes de la même source. De la même façon, le client ne peut pas compter sur le serveur pour garder de telle renseignments.

>Par contre, en ce qui concerne un protocole de communication avec statut, le serveur garde l’information du statut, c’est-à-dire, de la session, de l’identité de l’utilisateur, etc. au travers de multiples demandes de la même source.

**Pourquoi l’HTTP est un protocole sans statut?**
>Dans le cas d’HTTP, le server n’est pas exigé à garder l’information ou le statut à propos de chaque utilisateur au travers de multiples demandes.

>De différents serveurs utilisent différents façons pour instaurer le suivi de statut: des cookies, des en-têtes personnalisés, champs de formulaire cachés, etc. Cependant, au coeur même de chaque application Web, tout dépend sur l’HTTP qui est toujours un protocole simple; un système de demande-réponse.

**Qu’est-ce que c’est ‘REST’? Qu’est-ce que ça signifie quand on dit qu’un service est ‘RESTful’?**
>REST, un acronym pour ‘Representational State Transfer’, est un style d’architecture pour les systèmes hypermédia distribués qui se trouve le plus souvent dans les application Web qui eux-mêmes fonctionnent à travers d’HTTP.

>Certains caractéristiques d’un système qui instaure un architecture ‘REST’, c’est-à-dire, un service RESTful:

>Au moins deux parties principaux dans l’application: le client et le serveur, chacun possèdent leur propre responsabilités.

>Sans statut: chaque requête d’un client vers un serveur doit contenir toute l’info nécessaire pour permettre au serveur de comprendre la demande sans devoir dépendre d’un context conservé sur le serveur.

>Chaque réponse du serveur comprend de détails importants comme la date de création de la réponse, sa validité jusqu’à quel moment etc. Ainsi, cela evite les demandes inutiles de la part du client et sert aussi à éviter la réutilisation des données expirées.

>Une interface uniforme: Chaque ressource est uniquement identifiée; elles ont de représentation définies et on est capable de les manipuler que avec ces répresentations sans exiger la ressource même; chaque message est auto-descriptif et permet l’interpréteur à comprendre le message du contenu dedans;

>Dans le cas de services Web, ceux qui s’appellent souvent de RESTful APIs:

>Les ressources sont accessible par un URL de base, e.g. http://api.site.com/resources/
Représentations des ressource par un type MIME qui communique au client comment traiter le contenu
Une interface uniforme qui utilisent les méthodes HTTP: GET, PUT, POST, DELETE pour faciliter la lecture, la manipulation, la suppression etc. des données du côté du serveur

**Quels sont les différents types de demande d’HTTP?**
>Les plus connus:
GET: Pour aller chercher qqch du serveur (en n’ayant aucun d’autre effect vis-à-vis les données au côté du serveur)
POST: Pour envoyer les données concernant une nouvelle entité au serveur. Par exemple, en téléchargeant un fichier ou en soumettant un formulaire
PUT: Pour mettre à jour une entité qui existe déjà 
DELETE: Pour effacer une entité de données

>D’autres qui existe mais qui ne sont pas utilisés souvent:
PATCH: Il fonctionne pareillement au PUT mais se fait utiliser que pour ne mettre à jour que certains champs d’une entité qui existe déjà
TRACE: Permet à évaluer ce que une machine à travers du réseau reçoit quand un demande est fait. Donc, il retourne simplement ce que lui a été envoyé
OPTIONS: Un client peut utiliser celui-ci pour obtenir plus d’info sur les types de demande offerts par le serveur.
HEAD: Comme GET mais où le serveur répond que avec les en-têtes et non le contenu
CONNECT: Pour évaluer qu’un lien peut être établi

**Les champs d'en-tête d'HTTP, à quoi servent-ils?**
>Ils comprennent l'information importante à propos du demande ou de la réponse ou de l'objet envoyé dans le corps du message.

>Il y a, par exemple, la date de traitement. Selon si c'est un demande ou une réponse, il y a d'autres champ d'en-têtes, tels que:

>Quand c'est le serveur qui répond:
Location: Pour ce quand il faut rediriger le client vers une autre page;
Set-Cookie: Celui-ci, en faisant partie d'une réponse du serveur, contient une paire nom-valeur de l'information qui le client devrait garder;

>Quand le client envoye une demande au serveur:
Accept: Les *Content-Type* qui sont acceptable pour la réponse;
Authorization: Comprend l'info pour autoriser l'utilisateur à accéder une ressource;
User-Agent: Le navigateur utilisé par le client;
Cookie: Le même *cookie* qui a été envoyé tout à l'heure par le serveur peut être inclut dans une demande du client par ce champ-ci;

>Il y a des champs d'en-tête pour mieux définer le contenu. Par example:
Content-Type: pour le type MIME des données transfertes;
Content-Language: pour la language;
Expires: pour établir le moment où la réponse devrait être considèrée obsolète;
Last-Modified: Selon le serveur, le dernier moment quand les données étaient modifiées.

**Qu'est-ce que c'est un type MIME?**
>MIME ou ‘Internet media type’ ou bien ‘Content-type’, comme il s’appelle dans les en-tête de demandes d’HTTP, est un identifiant de format de données. Celui-ci est employé comme la façon uniforme pour classer le type de fichier sur l’internet.

>Les serveurs Web et les navigateurs comme Firefox, Chrome etc. ont des listes précises de types MIME. Cela facilite le transfert de fichiers d’un type connu.

>Par example, un type MIME très utilisé est celui de application/javascript. Un autre encore plus important: text/html.

**Comment fonctionne les *cookies*? Quelles sont les risques liées à leur utilisation?**
>Un cookie n'est q'une petite quantité de données, stockées soit dans un fichier texte ou dans la mémoire du système ou dans la session de navigation. Celui-ci contient les données qui permettent à un serveur d'identifier des clients basé sur leur visites précédentes.

>Eux-mêmes, les cookies posent aucune risque étant donné qu'ils sont créés seulement pour le site Web qui les ont générés. Cela dit, il posent des risques sécuritaire s'ils sont compromis vu qu'il portent l'information privée d'un client. En plus, un imposteur peut utiliser un cookie compromis pour se déguiser comme un vrai client afin d'accéder à l'information secrète du côté du serveur.

**Les termes 'ViewState' et 'SessionState' que signifient-ils?**
>Les deux concernent le stockage de données de client à travers d'une session quand le client interagit avec une application Web.

>'ViewState' fait référence aux données stockées dans une page de Web par exemple, dans un champ caché d'un formulaire. Celui-ci disparaît aussitôt qu'une action entraîne un changement de page.

>'SessionState', par contre, fait référence aux données stockées tel qu'elles resteront accéssible à travers de la session au complet, peu importe le changement d'une page à l'autre.

##Back-end:
**Quelle est la meilleure façon de stocker le valuer d'une couleur dans une base de données?**
>Avec n'importe quelle application, comment vous stocker des données dans la base de données, peu importe le type, dépend grandement de comment vous entendez de les accéder et les utiliser et aussi sur la base de données.

>Par exemple, d'une expériences personelle je peux vous dire que les dates-heures sont souvent stocker différemment dans les base de données populaires c'est-à-dire Oracle, MSSQL. J'ai pas d'expérience avec chacuc d'eux mais j'ai quand même trouver des solutions différentes quand je cherchais une solution pour les problèmes de mon propes project qui utilise MSSQL.

>Bref, il y a pas une façon qui est généralement mieux que d'autres. Cela dit, je peux vous donner l'exemple de mon propre projet dans lequel j'utilise une méthode quand même très commune: je les stocke en format hexadécimale. C'était la solution la plus simple étant donné que les données sont utilisées au côté client par le JavaScript pour colorer les rectangles SVG du graphique.

**Qu'est-ce que c'est les *microservices*?**
>Quand votre application consiste des microservice, ça veut dire qu'elle consiste de nombreuses petites applications indépendentes, chacune capable de gérer leur propre stockage et de s'élargir indépendement à travers de multiple machines, si nécessaire.

**Qu'est-ce que c'est les applications *monolithes*, alors?**
>Contrairement aux microservices, une application monolithe consiste d'une cohésive de code où les composants différents sont faits tel qu'ils fonctionnent unitairement en partageant les ressouces de mémoires et de traitement.

**Que sont les avantages et les désavantages des deux?**

Monolithic:
>Avantages:

>* Meilleure gestion des ressouces qui sont communment partager dans une application: e.g. l'enregistrement cronologique, fonctions d'autorisation, de sécurité etc.
* Meilleure performance dù au partage des ressources de mémoire et de traitement.

>Désavantages: 

>* Les applications monolithes ont une tendance à devenir étroitement jumelées et empêtrées au cours du temps. Cela rend difficile de isoler les services pour les faire meiux ou pour affectuer une amélioration de la base de code.
* Pour les mêmes raisons, telles architectures sont plus difficiles à comprendre dû aux dépéndances cachées, effets secondaires, etc.

Microservices:
>Avantages:

>* Celles-ci sont typiquement mieux organiser. Chaque service a sa propre application très précise et il se concerne pas avec les applications des autres composants.
* Les services sont plus facilement à reutiliser dans d'autres application. e.g. une API peut être servir une application cellulaire, une application Web et également une application d'analyse des données, instaurée sur l'ordinateur d'un chercheur.
* Elles pourraient entrainer à des améliorations de performances étant donné qu'elles sont plus facile à modifier individuellement.

>Désavantages:

>* Le développement d'une architecture microservices est plus couteux à l'égard du temps de développement parce qu'il y a souvent beaucoup de services qu'il faut développer tel qu'ils fonctionneraient indépendamment dans le futur. Par contre, cela pourrait être fait dans un mannière pas si rigoreuse dans le cas d'une application monolithe.
* Il faut allouer plus de ressources vu qu'il y a plus de services à entretenir.

How would you model user authorization, user profiles and permissions in a database?

##Database/SQL:
**Qu'est-ce que c'est des base de données NoSQL? Que signifie ce terme-ci?**
>Les bases de données NoSQL sont des systèmes; des architectures; des applications qui offerent une façon différente de les bases de données rélationelles utilisées traditionellement pour stocker des données qui se prètent pas facilement à la structure, ou dont les caractéristiques changent si rapidement que il y a pas facile de déterminer le schéma requis.

>Ces applications comprennent des logiciels comme MongoDb (avec laquelle j'ai un peu d'expérience), CouchDb, DynamoDb d'Amazon etc. Le terme, 'NoSQL' et lui-même une abréviation pour 'Not only SQL'.

>Telles bases de données sont évoluées en fonction des besoins de développement d'application moderne qui est caractérisé par de certains facteur clés :

>- La génération rapide et massive des nouveaux types de données non-structurées, semi-structurées etc.
- Applications qui font face à une base d'utilisateurs globale; qui fonctionnent tous les heures; qui devraient être accésible à une multitude d'appareils.
- Étant donné que ce mêmes applications pourraient servir des millards d'utilisateurs les organisme ont besoin des architectures qui peuvent s'élargir rapidement et à meilleur marché.
- Les base de données relationnelles se trouvent peu adaptées à plusieurs changements au schéma; ce qui arrive assez souvent en suivant des méthodes agile de dévéloppement.

>Bref, on trouve que les bases de données rélationnelles n'était pas créés pour faire face aux défis actuels de l'immensité des données générées avec tellement de vitesse, ni à prendre avantage de la disponibilité des ressources de stockage et de traitement.

**Que sont les différents types de base de données NoSQL?**
>- Entrepôts clés-valuers : Celles-ci sont les plus simple car chaque object stocké consiste un attribut, c'est-à-dire la clé, jumelé avec le valeur associé. E.g. Riak, Berkeley DB.
- Base de données documentaires : Chaque clé est jumelé avec une structure de données complexe qui s'appelle un document. Chaque document peut consister plusieurs différentes paires clés-valeur ou d'autres documents encapsulés.
- Entrepôts graphiques : Pour stocker l'information à propos des réseaux de données, comme des liens sociaux.
- Entrepôts larges colonnes : Comme CassandraDB et HBase qui sont utilisées pour des requêtes à traves d'une quantité massive de données et où les nommes et les formats des colonnes peuvent varier d'une ligne à l'autre.

**Quelles sont les avantages des bases de données NoSQL vis-à-vis des bases de données relationnelles? Quelles sont les désavantages?**

>Avantanges:

>- Quand il faut élargir l'application; disons pour la rendre capable de traiter des augmentations dans le nombre d'utilisateurs ou dans la quantité de stockage nécessaire, avec les RDBMS cela implique une amélioration du matériel de serveur. C'est souvent très couteux. Les RDBMS ne se prètent pas facilement non plus à notre âge actuel des services infonuagiques ou il est souvent plus économique de tirer des ressources de traitement et de stockage de multiples machines étalées à travers le monde. Par contre, les bases de données NoSQL sont faites avec cette réalité en tête et peuvent sembler plus économiques en comparaison.
- Les mêmes avantages soulignées au point précédent montre que les bases de données sont mieux capable de gérér la revolution actuelle de *Big Data*.
- Finalement, elles rendre capable à stocker et traiter les données non ou semi-structurées, une avantage qui, au moins en théorie, permet à développer des applications plus rapidement et avec clarité.

>Désavantanges:

>* Les bases de données relationnelles sont matures. Elles sont stables et offrent une grande variété de fonctionalité.
* Il est plus facile de trouver des experts de RDBMS plutot que ceux de NoSQL. Voire, il est souvent plus économique à les employer aussi par rapport à l'autre.
* La vaste majorité des outils de *Business Intelligence* c'est-à-dire intelligence d'affaires sont faits pour être utilisés avec des RDBMS.
* Il y a une plus grande disponibilité du support technique et administratif par de grands compagnies comme Oracle et Microsoft pour leurs suites logiciels d'entreprise. Par contre, même si les bases de données NoSQL temoignent une bonne croissance d'adoption parmi des startups, elles comprennent quand même de technologies *open-source* sans garantie de support compréhensif.
* Finalement, les bases de données relationnelles se prètent plus facilement à l'administration.

**Dans quels scénarios utiliseriez-vous des base de données NoSQL plutot que celles qui sont relationnelles? Et l'inverse?**
>Cela va dependre sur plusieurs facteurs:
- Premièrement, est-ce que les données recueillies se prètent facilement à la structure ou non.
- Est-ce qu'il y a une possibilité que l'application va temoigner constamment une croissance en terme de nombre des utilisateurs, disponiblité de stockage? Qu'il faudra augmenter la capacité assez tôt après qu'il est sortie et assez souvent ?
- Est-ce que c'est nécessaire que l'application soit bâtie sur une fondation de technologie assez connue dans le marché, une histoire de stabilité avec une bonne disponibilité de soutien ?
- Si vous utiliserez d'autre application parallèlement, disons comme un logiciel d'intelligence d'affaires, est-ce que cela va fonctionner avec votre choix final?

**Le terme 'ACID', qu'est-ce ça signifie?**
>ACID est un acronyme de *Atomicity, Consistency, Isolation, Durability*

>Atomicity: En interagissant avec une base de données, le record est mise à jour complètement. S'il y a un problème, aucune mise à jour se déroule c'est-à-dire soit tout se passe soit rien ne se passe.

>Consistency: Une transaction créerait un nouveau état de données. S'il y a un échec pedant le processus, l'état est mis comme il était avant le commencement de la transaction. Donc, soit un réussite soit rien change.

>Isolation: Des requêtes à la base de données, soit une ou plus, devraient fonctionner indépendamment des autres processus.

>Durability: Une fois enregistrées, même en cas d'échec du système, les données ne devraient pas être affectées.

What's the difference between a left join and an inner join?

##Pratique:
Write your own linked list class without using the built-in classes.
Write your own hashtable class without using the built-in classes.
Write a class that represents a binary tree. Write a method that traverses all nodes of the tree.
Write a method to perform a binary search on an array without using built-in methods.
Draw a database schema for a blog. Each user only has one blog, each blog has many categories, each category has many posts, and each post can belong to more than one category. Ask your applicant to write queries to pull specific information out.

##Algorithmes:
How do you find out if a number is a power of 2? And how do you know if it is an odd number?
How would you change the format of all the phone numbers in 10,000 static html web pages?
How would you write a function to reverse a string? And can you do that without a temporary string?
In an array with integers between 1 and 1,000,000 one value is in the array twice. How do you determine which one?
Can you name an example of a recursive solution that you created?
What is the last thing you learned about algorithms from a book, magazine or web site?

##Data Structures:
What is a pointer?
How do you find the middle item in a linked list?
What is a hashtable?
Which is faster: finding an item in a hashtable or in a sorted list?
What is the difference between a queue and a stack?
Stacks refer to a list in which all items are accessed and processed on the Last-In-First-Out (LIFO) basis. In a stack, elements are inserted (push operation) and deleted (pop operation) from the same end called top.

Queues refer to a list in which insertion and deletion of an item is done on the First-In-First-Out (FIFO) basis. The items in a queue are inserted from the one end, called the rear end, and are deleted from the other end, called the front end of the queue.
What is the difference between storing data on the heap vs. on the stack?

##OOP:
What is abstraction?
What is inheritance?
What is polymorphism?
What is encapsulation?
What is the difference between a class and an object/instance?
What is a constructor?
What is a destructor?
What is an abstract class?
What is operator overloading?
What is method overloading?
What is method overriding?
How does overriding differ from overloading?
How does pass by value differ from pass by reference?
What is 'this'?
What is 'super'?
What is boxing?
What are design patterns?
Which design patterns have you used, and in what situations?
What is a singleton?
What is Dependency Injection?
What are the SOLID principles of Object-oriented development?

##JavaScript:
**Que sont les variables globales ?**
> Les variables globales sont des variables qui ont aucune portée (*scope*) et qui sont accéssibles n'importe où dans le code.

> Par contre, des variable locales ont des portées qui peuvent restreindre leur accésibilité jusqu'aux limites d'où les variables étaient déclarées. Ceci est fait en utilisant le mot-clé 'var' avant le variable pour la déclarer localement.

**Est-ce qu'il y a des désavantanges à l'utilisation frequente de variables globales ?**
>- Possibilité de conflits de nommes entre des variables globales et celles qui sont locales.
- Code qui dépend lourdement sur des variables globales pour fonctionner est difficile à vérifier et maintenir.

**Quelle est la différence entre 'undefined' et 'null' ?**
> Le valeur d'une variable non-initialisée est 'undefined'.

> Par contre, des variables peuvent être vider de leur valeurs en mettant 'null' comme valeur. 

**Quelle est la significance du mot-clé 'this' en *JavaScript* ?**
> Le mot-clé 'this' en JavaScript fait référence à l'objet à qui la méthode appartient mais cela dépend de comment la fonction est appelé. Bref, il indique l'objet actuellement en portée qui possède la ligne de code en train d'être traiter.
> Par exemple, une fonction comme *setInterval* appèlée n'importe où provient dans l'object *Window*. Donc, dans le contenu de cette fonction, 'this' fera référence au *Window*. 
> En générale, en ce qui concerne des gestionnaires d'événement, 'this' fait référence à l'objet qui a généré l'événement.
> Par contre, si la ligne de code en train d'être traité fait partie d'un object créé par le mot-clé 'new', 'this' ferait référance à cet object-là.

**Qu'est-ce que c'est la propogation d'événement (*event bubbling*)?**
> En ce qui concernce le DOM (*Document Object Model*), la propogation d'événement (*Event bubbling*) est l'habitude de chaque noeud de passer de mannière automatique chaque événement qu'il traite à son parent.
> C'est utile parce que comme ça vous n'avez pas besoin de placer plus qu'une gestionnaire d'événement pour attendre des événements qui vont provenir de différents noeuds enfants.
> Par exemple, vous pouvez mettre un gestionnaire à un élément *table* pour gérér des événement provenant des enfants cellules.
> Il y a donc des avantages de réutilisation de code et de simplicité mais aussi celle d'une vitesse améliorée vu que le code va traverser seulement une fois l'arborescence DOM.

**Qu'est-ce que c'est l'opérateur '===' et comment diffère-t-il de l'opérateur '==' ?**
>'===' est le opérateur d'égalité stricte c'est-à-dire qu'il répond *true* (vrai) seulement si les deux opérandes n'ont pas seulement le même valeur mais qu'il sont aussi de même type.

>Par contre, '==' vérifie seulement si les deux opérandes sont égaux à l'égard de leurs valeurs. S'il y a une différence de types des deux, il transforme le type des deux à un format qui correspond le mieux selon les spécifications ECMA.

**Qu'est-ce que c'est une fonctione anonyme en *JavaScript* ?**
> Une fonction déclarée sans indentifiant nommé. En gérérale, ces fonctions sont inaccessible après être déclarée.

**Qu'est-ce que c'est une clôture en *JavaScript* ?**
> Une fermeture ou clôture (en anglais : closure) est une fonction accompagnée de son environnement lexical. L'environnement lexical d'une fonction est l'ensemble des variables non locales qu'elle a capturé, soit par valeur (c'est-à-dire par copie des valeurs des variables), soit par référence (c'est-à-dire par copie des adresses mémoires des variables).

> Une fermeture est donc créée, entre autres, lorsqu'une fonction est définie dans le corps d'une autre fonction et utilise des paramètres ou des variables locales de cette dernière.

>En *JavaScript*, une fermeture peut être passée en argument d'une fonction dans l'environnement où elle a été créée (passée vers le bas) ou renvoyée comme valeur de retour (passée vers le haut).

>Voici un exemple simple des fermetures :
```
var globalVar = "xyz";

(function outerFunc(outerArg) {
  var outerVar = 'a';
  
  (function innerFunc(innerArg) {
    var innerVar = 'b';
    
   console.log(
      "outerArg = " + outerArg + "\n" +
      "innerArg = " + innerArg + "\n" +
      "outerVar = " + outerVar + "\n" +
      "innerVar = " + innerVar + "\n" +
      "globalVar = " + globalVar);
    
  })(456);
})(123);
``` 
>Dans l'exemple précédent, les variables *innerFunc*, *outerFunc* et l'espace de nommage sont tous en portée à l'intérieur d'*innerFunc*. Le résult ci-dessous va donc être produit:
```
outerArg = 123
innerArg = 456
outerVar = a
innerVar = b
globalVar = xyz
```

** Qu'est-ce que c'est un 'promis' (*Promise*) en *JavaScript* ? **
> Un promis est une méthode qui produit un valeur événtuellement. Au lieu de passer une fonction comme argument, ce qui est le cas des callbacks, une fois que le résultat est reçu d'une opération asynchrone, le fonction requise est exécutée (normallement placée en queue de la fonction qui la précède)
> C'est-à-dire, on utilise pas des callbacks pour passer comme arguments à l'opération asynchrone. C'est plus facile de l'expliquer en exemple :
>```
callAsyncFunction()
.then(firstFunction)
.then(secondFunction)
.then(thirdFunction)
.then(fourthFunction);
```

Why would we wrap the entire content of a JavaScript source file in a function block?
How does JavaScript's prototype-based OOP differentiate it from other class-based languages?
How do classes in JavaScript differ from those in other languages?
How do properties of objects work in JavaScript?
How does inheritance work in JavaScript?
What frameworks do you use?

##TypeScript:
**Qu'est-ce c'est le *TypeScript* ? Pourquoi devrait-on l'utiliser ?**
> Le *TypeScript* est une langage de programmation développée par Anders Hejlsberg, aussi créateur de C#, entretenu et développé par Microsoft. Elle est un sur-ensemble stricte de *JavaScript* qui ajoute de types statics et un systèmes de programmation objet-orientée avec des classes.

> *TypeScript* a été conçu pour surmonter les défis qui existent avec l'utilisation de *JavaScript* comme l'absense d'un fort système des types, l'absense des classes, la manque de vérification d'erreur au temps de compilation, etc. 

**Quelles sont les avantages de *TypeScript* ?**
>* Aide à mieux structurer le code
* Faire disponible un système de programmation objet-orientée fondée sur des classes
* Permet à mettre en place des lignes directrices de codage
* Vérification de type
* Vérification d'erreurs au moment de compilation

**Quelles sont quelques désavantages ?**
>* *TypeScript* offre une autre façon d'écrire *JavaScript*. Il régle pas finalement les problèmes qui ont toujours existés avec l'utilisation de *JavaScript*
* Peut-être que vous ne voulez pas disperser vos ressources pour maintenir la connaissance d'une autre langage
* Dépendances sur de fichiers de définition de type si vous voulez utiliser des bibliothèques qui existent déjà
* Dépendance sur la définition de types est un problème; comment peut-on être confiant de leur qualités?
* Faut également garder les définitions à jour.
* Faut ajouter une autre étape dans le processus de compilation pour transformer le *TypeScript* à *JavaScript*
* Bien qu'il rend facile certaines choses, *TypeScript* n'ajoute rien de nouveau. Certains parmi vos développeurs ne trouveront rien qu'ils peuvent faire mieux avec *TypeScript*

##NodeJs:
**Qu'est-ce que c'est la programmation asyncrone ?**
> Des programmes fonctionnent normalement dans une mannière synchrone c'est-à-dire les lignes de code sont traiter séquentiellement. Des opérations comme lire un fichier ou envoyer une requête à un serveur et faire quelque chose avec la réponse cause un blockage jusqu'au moment où le processus bloquant est terminé.

> Par contre, dans le cas de programmation asynchrone, l'application fontionne dans une boucle d'événement. Quand il y a besoin de faire quelque chose de bloquant, la requête est envoyée et l'application continue à traiter le code qui suit sans se bloquer en attendant le résultat. Quand celui-ci est prêt, une interruption est causée et le gestionnaire d'événement traite le résultat. Dans cette façon, un programme peut traiter plusieurs opérations simultanément.

> Un bon exemple d'une application asynchrone dans la vraie vie: tous les système d'interfaces utilisateur qui, par leur natures, passent la plupart de leur temps en attendant. Une action de l'utilisateur interompra la boucle d'événement et faire fonctionner les gestionnaires d'événement.

**Pourquoi est-elle importante vis-à-vis NodeJs ?**
> NodeJs est une application monofilaire. Il soutien des processus concurrents par des événements et des callbacks. Il fonctionne donc dans une mannière fondamentallement asynchrone en utilisant le patron de conception d'*Observer*.
 
> Node utilise une boucle d'événement. Celle-ci est la partie d'application qui s'occupe à attendre des interruptions. Par exemple, une interruption est causée par une demande sur le réseau. La boucle continue à accepter plus de telles demandes.

> Une fois qu'une tâche est terminé elle appele le callback associé en passant comme paramètre le résultat de traitement de la demande. Les autres processus ne sont pas bloqués pendant ce temps-là. 

> Chaque API du NodeJs est asynchrone dans telle façon et il est donc non-bloquant dans cette mannière-ci.

**Qu'est-ce que c'est un *callback* ?**
> Un *callback* est l'équivalent asynchrone d'une fonction c'est-à-dire qu'il est appelé comme une fonction à la fin d'une tâche. Par exemple, une fonction pour lire un fichier peut commencer par lire le fichier et puis retourner la controle à l'environnement tout de suite après tel que l'application peut traiter la prochaîne instruction.
> Une fois le processus de lecture est terminé la fonction *callback* est appelé avec le contenu du fichier comme paramètre. Il n'y a donc aucun blocage.
> Cela rend NodeJs très extensible vu qu'il peut traiter un grand nombre de requêtes sans attendant la réponse d'une fonction ou d'autre.

**Qu'est-ce que cela veut dire, le *callback hell* ?**
>Ce terme fait référence au modèle de codage où il y a plusieurs fonctions callbacks imbriquées et où le code prend la forme d'une pyramide et fini par se rendre difficile à débouger.

**Que signifie la programmation événementielle (*Event-driven programming*) ?**
>La programmation événementielle est un paradigme de programmation dans lequel le flux de l'application est déterminé par des événements comme des messages des autres programmes.

**Quelles sont les avantages liées à l'utilisation de NodeJs ?**
>* Asynchrone et événementielle : Chaque API du NodeJs est asynchrone et non-bloquant. En effect, un serveur NodeJs attend jamais pour la réponse d'un API; il continue au traitement du API suivant et utilise la boucle d'événement pour gérér la réponse de l'appel à l'API précédent.
* Rapide : Grâce à moteur V8 de Google Chrome, Node.js est très rapide à l'exécution du code.
* Monofilaire mais très extensible : Même si Node.js est monofilaire, il employe une boucle d'événement. Cela permet le serveur à répondre dans une façon non-bloquant. Donc, le serveur reste beaucoup plus extensible et aussi plus performant que les applications traditionelles de serveur comme Apache qui créent de multiples fils pour gérér les requêtes.
* Pas de tampon: Node.js n'utilise pas de tampon. Par contre, l'application sorte les données dans des *chunks*.
* Tout en *JavaScript*: Bien que le *JavaScript* n'est pas très utile pour construire des applications de traitement intensif et exigeant, l'avantage est quand même considérable qu'on peut construire le *front-end* et le *back-end* tout en *JavaScript* avec NodeJs. Cela peut appliquer même au niveau de la base de données si on utilise des bases de données documentaire comme MongoDb et stocke les données en format JSON.
	
**Quelles sont les désavantages ?**
>- Instabilité : L'API de NodeJs est pas aussi stable comparé à certaines d'autres cadriciels majeurs (Rails, ASP.NET, Django etc.) et il s'avance et change très rapidement et frequemment
- Défis liès au modèle asynchrone de programmation événementielle : Avec NodeJs il n'y a aucune d'autre option que de maitriser le modèle de programmation asynchrone. Toutefois, celui-ci est souvent plus complexe à mettre en oeuvre que le modèle traditionel de programmation linéaire.
- Complexité : Il est essentiel d'utiliser des *callbacks* à chaque étape. Ceci entraîne un grande nombre de callbacks imbriqués qui à son tour abouti à une base de code plus complexe.
- Monofilaire : Présentement, NodeJs se trouve peu adapté à la construction de grandes applications complexe vu qu'il soutein pas de programmation multifilaire (*multi-thread*)
- Il y a finalement les désavantages liées avec l'utilisation de JavaScript comme votre langue de programmation fondamentalle.

**Où peut-on utilisé le NodeJs ?**
>* Il est particulièrement bien adapté aux applications Web et certainements ceux qui fonctionnent en temps-réel.
* Applications de réseau
* Applications de systèmes distribués
* Autres types d'application généraux


##Testing/Debugging:
Can you explain what Test-Driven Development is?
How do you test for the quality of your code?
How do you make sure that your code handles different kinds of error situations?
How do you make sure that your code is both safe and fast?
How do you find an error in a large file with code that you cannot step through?
Can you tell me something that you have learned about testing and quality assurance in the last year?

##SDLC:
Can you describe the process you use for writing a piece of code, from requirements to delivery?
What is important when updating a product that is in production and is being used?
How can you make sure that changes in code will not affect any other parts of the product?
How do you create technical documentation for your products?
What measures have you taken to make your software products more easily maintainable?
How can you debug a system in a production environment, while it is being used?
Can you name reasons why maintenance of software is the biggest/most expensive part of an application’s life cycle?
How can you make sure that team members know who changed what in a software project?

##D'autres:
Describe the project you've worked on?
What did you do that worked out particularly well?
What would you do differently?
What industry sites and blogs do you read regularly?

##C#:
What is the difference between a struct and a class?
Class:
A class is a reference type.
While instantiating a class, CLR allocates memory for its instance in heap.
Classes support inheritance.
Variables of a class can be assigned as null.
Class can contain constructor/destructor. 

	Structure:
A structure is a value type.
In structure, memory is allocated on stack.
Structures do not support inheritance.
Structure members cannot have null values.
Structure does not require constructor/destructor and members can beinitialiazed automatically.

Difference between abstract class and an interface?
Abstract Class:
A class can extend only one abstract class
The members of abstract class can be private as well as protected.
Abstract classes should have subclasses
Any class can extend an abstract class.
Methods in abstract class can be abstract as well as concrete.
There can be a constructor for abstract class.
The class extending the abstract class may or may not implement any of its method.
An abstract class can implement methods. 

Interface
A class can implement several interfaces
An interface can only have public members.
Interfaces must have implementations by classes
Only an interface can extend another interface.
All methods in an interface should be abstract
Interface does not have constructor.
All methods of interface need to be implemented by a class implementing that interface.
Interfaces cannot contain body of any of its method.

What are collections and generics?
What is a delegate?
What is an event?
When do you use polymorphism and when do you use delegates?
What is the virtual keyword used for?
Why use a private constructor?
Why use a static constructor?
What is the difference between a static and a non-static method?
How do you prevent a class from being inherited?
Is string a value type or a reference type?
What is the difference between protected and internal?
What about "protected internal"?
What is the StringBuilder class? Why use it?
What is the difference between 'ref' and 'out'?
What is a weak-reference? When would you want to use one?
What is the difference between 'readonly' and 'const'?
What is strong-typing versus weak-typing?
What is the difference between a thread and a process?
What is Reflection?
What is the difference between early-binding and late-binding?
What is lazy-loading?

##ASP.NET
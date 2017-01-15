#Questions générales

##Moi:
**Présentez-vous!**
**Quels sont vos objectifs?**
**Quelles sont vos faiblesses?**
**Qu’est-ce qui est le plus important dans votre vie ?**
**Pourquoi avez-vous quitté votre emploi?**
**Qu’avez-vous fait depuis votre dernier emploi ?**
**Quel poste aimeriez-vous occuper dans 5 ans ?**
**Pourquoi changez-vous d'emploi constamment ?**

##Eux:
**Pourquoi voulez-vous travailler ici?**
**Que connaissez-vous de notre entreprise ?**
**Pourquoi devrait-on vous embaucher?**
**Pourquoi vous et pas les autres candidats?**
**Pouvez-vous me préciser ce que vous avez compris du poste ?**
**Vous n’avez aucune expérience à ce type de poste, comment comptez vous faire pour vous adapter ?**
**Qu’est ce qui selon vous va vous poser des difficultés à ce poste ?**

##Travail:
**Comment travaillez-vous en équipe ? How do you resolve issues in a team?**
**De quoi êtes-vous le plus fier (dernier emploi) ?**
**De quoi êtes-vous le plus fier (carrière) ?**
**Quand étiez-vous le plus satisfait dans votre emploi?**
**Trois choses positives que votre employeur précédent dirait?**

##D'autres:
**Disponibilité?**
**Quel salaire recherchez-vous? Quelle rémunération attendez-vous?**
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

Which are the most important features of NoSQL databases?
Explain the difference between NoSQL v/s Relational database?
When should I use a NoSQL database instead of a relational database?

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
What are global variables?
Global variables are available throughout your code: that is, the variables have no scope. Local variables scope, on the other hand, is restricted to where it is declared (like within a function). The var keyword is used to declare a local variable or object, while omitting the var keyword creates a global variable.

Most JavaScript developers avoid globals. One reason why is they're averse to naming conflicts between local and globals, Also, code that depends on globals can be difficult to maintain and test.

What is the difference between undefined and null?
The value of a variable with no value is undefined (i.e., it has not been initialized). Variables can be emptied by setting their value to null. You can test for each using the === (three equal signs) or == (two equal signs) for comparison checking. The big difference is the latter uses coercion, which can have some odd results — it returns true for a null or undefined comparison if they are either.

What is JavaScript's this keyword?
JavaScript's this keyword normally refers to the object that owns the method, but it depends on how a function is called. Basically, it points to the currently in scope object that owns where you are in the code. When working within a Web page, this usually refers to the Window object. If you are in an object created with the new keyword, the this keyword refers to the object being created. When working with event handlers, JavaScript's this keyword will point to the object that generated the event.

What is event bubbling?
Event bubbling describes the behaviour of events in child and parent nodes in the Document Object Model (DOM); that is, all child node events are automatically passed to its parent nodes. The benefit of this method is speed, because the code only needs to traverse the DOM tree once. This is useful when you want to place more than one event listener on a DOM element since you can put just one listener on all of the elements, thus code simplicity and reduction. One application of this is the creation of one event listener on a page's body element to respond to any click event that occurs within the page's body.

How does JavaScript's prototype-based OOP differentiate it from other class-based languages?
How do classes in JavaScript differ from those in other languages?
How do properties of objects work in JavaScript?
How does inheritance work in JavaScript?
What is === operator? How is it different from the == operator?
=== is called as strict equality operator which returns true when the two operands have the same value and are of the same type.
== only checks for value after type-converting the operands into the 'best' format, according to ECMA specs.

What is an anonymous function in JavaScript?
A function that is declared without any named identifier is known as an anonymous function. In general, an anonymous function is inaccessible after its declaration.

What is a closure?
A closure is an inner function that has access to the variables in the outer (enclosing) function’s scope chain. The closure has access to variables in three scopes; specifically: (1) variable in its own scope, (2) variables in the enclosing function’s scope, and (3) global variables.

Here is a simple example:
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
In the above example, variables from innerFunc, outerFunc, and the global namespace are all in scope in the innerFunc. The above code will therefore produce the following output:
```
outerArg = 123
innerArg = 456
outerVar = a
innerVar = b
globalVar = xyz
```
Why would we wrap the entire content of a JavaScript source file in a function block?
What frameworks do you use?


##TypeScript:
What is TypeScript? Why should we use it?
JavaScript is the only client side language universally supported by all browsers. But JavaScript is not the best designed language. It’s not a class-based object-oriented language, doesn’t support class based inheritance, unreliable dynamic typing and lacks in compile time error checking. And TypeScript addresses all these problems. In other words, TypeScript is an attempt to “fix” JavaScript problems.

TypeScript is a free and open source programming language developed and maintained by Microsoft. It is a strict superset of JavaScript, and adds optional static typing and class-based object-oriented programming to the language. TypeScript is quite easy to learn and use for developers familiar with C#, Java and all strong typed languages. At the end of day “TypeScript is a language that generates plain JavaScript files.”

What are the pros of TypeScript?
It helps in code structuring
Use class based object oriented programming
Impose coding guidelines
Offers type checking
Compile time error checking
Intellisense

What are some cons of using TypeScript?
TypeScript is just another way to write JavaScript. It doesn’t fix the problems of JavaScript. It just creates an illusion that it does.
One more tool to learn.
TypeScript has dependency on type definition files, if you wish to use any existing JavaScript libraries.
Quality of type definition files is a concern as how can you be sure the definitions are correct?
Frequent releases of new versions JavaScript library is also a pain area. Because if their type definition files are not updated then you can’t use them instantly.
In order to run the application in the browser, a compile step is required to transform TypeScript into JavaScript.
Web developers are using JavaScript from decades and TypeScript doesn’t bring anything new.
To use any third party library, definition file is you need. And not all the third party library have definition file available.

##NodeJs:
What is asynchronous programming? Why is it important in Node?
Synchronous programming means that, barring conditionals and function calls, code is executed sequentially from top-to-bottom, blocking on long-running tasks such as network requests and disk I/O.

Asynchronous programming means that the engine runs in an event loop. When a blocking operation is needed, the request is started, and the code keeps running without blocking for the result. When the response is ready, an interrupt is fired, which causes an event handler to be run, where the control flow continues. In this way, a single program thread can handle many concurrent operations.

User interfaces are asynchronous by nature, and spend most of their time waiting for user input to interrupt the event loop and trigger event handlers.

Node is asynchronous by default, meaning that the server works in much the same way, waiting in a loop for a network request, and accepting more incoming requests while the first one is being handled.

This is important in JavaScript, because it is a very natural fit for user interface code, and very beneficial to performance on the server.

What does event-driven programming mean?
In computer programming, event driven programming is a programming paradigm in which the flow of the program is determined by events like messages from other programs or threads. It is an application architecture technique divided into two sections 1) Event Selection 2) Event Handling
Where can we use node.js?
Web applications ( especially real-time web apps )
Network applications
Distributed systems
General purpose applications

What is the advantage of using node.js?
Aynchronous and Event Driven:
All APIs of Node.js library are aynchronous that is non-blocking. It essentially means a Node.js based server never waits for a API to return data. Server moves to next API after calling it and a notification mechanism of Events of Node.js helps server to get response from the previous API call.

Very Fast:
Being built on Google Chrome's V8 JavaScript Engine, Node.js library is very fast in code execution.

Single Threaded but highly Scalable:
Node.js uses a single threaded model with event looping. Event mechanism helps server to respond in a non-bloking ways and makes server highly scalable as opposed to traditional servers which create limited threads to handle requests. Node.js uses a single threaded program and same program can services much larger number of requests than traditional server like Apache HTTP Server.

No Buffering:
Node.js applications never buffer any data. These applications simply output the data in chunks.

What are the pros and cons of Node.js?
Pros:
	If your application does not have any CPU intensive computation, you can build it in Javascript top to bottom, even down to the database level if you use JSON storage object DB like MongoDB.
	Crawlers receive a full-rendered HTML response, which is far more SEO friendly rather than a single page application or a websockets app run on top of Node.js.

Cons:
	Any intensive CPU computation will block node.js responsiveness, so a threaded platform is a better approach.
	Using relational database with Node.js is considered less favourable

What is a Callback?
Callback is an asynchronous equivalent for a function.

A callback function is called at the completion of a given task. Node makes heavy use of callbacks. All APIs of Node are written is such a way that they supports callbacks.

For example, a function to read a file may start reading file and return the control to execution environment immidiately so that next instruction can be executed. Once file I/O is complete, it will call the callback function while passing the callback function, the content of the file as parameter. So there is no blocking or wait for File I/O. This makes Node.js highly scalable, as it can process high number of request without waiting for any function to return result.

What is callback hell and how can it be avoided?
Callback hell refers to a coding pattern where there is a lot of nesting of callback functions. The code forms a pyramid like structure and it becomes difficult to debug.

Explain the non-blocking nature of Node?
If application has to wait for some I/O operation in order to complete its execution any further then the code responsible for waiting is known as blocking code. By providing callback function. Callback function gets called whenever corresponding event triggered.

What is a Promise?
A promise is a method that eventually produces a value. Instead of passing a function as argument as with callbacks, “Once the result is received from an asynchronous operation then the required function is executed”. The required functions are never passed as arguments to the asynchronous operation. E.g.

callAsyncFunction()
.then(firstFunction)
.then(secondFunction)
.then(thirdFunction)
.then(fourthFunction);

What is the Event loop?
Node js is a single threaded application but it support concurrency via concept of event and callbacks. As every API of Node js are asynchronous and being a single thread, it uses async function calls to maintain the concurrency. Node uses observer pattern. Node thread keeps an event loop and whenever any task get completed, it fires the corresponding event which signals the event listener function to get executed.

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
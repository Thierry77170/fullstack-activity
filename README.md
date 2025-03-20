# Cas pratique #

J'ai créé une API fonctionnelle dans le cadre d'un cas pratique. Mon API est connectée à une base de données, car les différentes opérations CRUD sont testées et vérifiées !

J'ai créé une API basique pour une boutique en ligne qui permet de créer, lire, modifier et supprimer des produits ( Product ). Les Product ont quatre champs obligatoires :

name : le nom du produit, de type String ;
description : la description du produit, de type String ;
price : le prix du produit, de type Number ;
inStock : si le produit est en stock, de type Boolean.

J'ai implémenter cinq routes :

GET: /api/products
Retourne tous les produits sous la forme { products: Product[] }

GET:/api/products/:id
Retourne le produit avec le _id fourni sous la forme { product: Product }

POST:/api/products
Crée un nouveau Product dans la base de données.
Le corps de la requête a pour forme :
![fullstack-activity](Frontend/images/cinqRoutes.webp)
Il retourne le Product ainsi créé (y compris son champ _id ), sous la forme{ product: Product }.
La Promise retournée par la méthode save() de mon modèle Mongoose reçoit le produit créé :
![fullstack-activity](Frontend/images/promiseSave.webp)

PUT: /api/products/:id
Modifie le produit avec le _id fourni selon les données envoyées dans le corps de la requête.
Le corps de la requête a pour forme :
![fullstack-activity](Frontend/images/promiseSave.webp)
Retourne un objet de la forme { message: 'Modified!' }

DELETE : /api/products/:id
Supprime le produit avec le _id fourni.
Retourne un objet de la forme { message: 'Deleted!' }

Mon API tourne en locale en localhost (port 3000) et accepter les requêtes HTTP venant de n'importe quelle origine (avec la configuration CORS !).

Pour tester l'API, vous allez installer dans un premier temps une mini-application front-end. Clonez le repo.

Depuis le dossier frontend, exécutez npm install puis npm start . Vous devriez voir s'ouvrir une fenêtre de navigateur comme celle-ci :
![fullstack-activity](Frontend/images/fenetreNavigateur.webp)

Dans un deuxième temps, après avoir installé les technologie utilisées (Node.js, Express, mongoose et nodemon), exécutez nodemon server. Vous pouvez lancer le teste.

En cas de succès, vous verrez la fenêtre de navigation comme celle-ci :
![fullstack-activity](Frontend/images/fenetreSucces.webp)

## Les technologies utilisées

- Node.js
- Express
- MongoDB Atlas
- Mongoose
- Nodemon
- JavaScript


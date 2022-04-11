
# Individual Project - Infinite Video Games App 🎮


<div>
    <img height="270" src="https://res.cloudinary.com/djbiam1gm/image/upload/v1649704622/VG%20PI/slide01_mini.png" />
    <img height="270" src="https://res.cloudinary.com/djbiam1gm/image/upload/v1649704623/VG%20PI/slide02_mini.png" />
</div>

<div>
    <img height="270" src="https://res.cloudinary.com/djbiam1gm/image/upload/v1649704623/VG%20PI/slide03_mini.png" />
    <img height="270" src="https://res.cloudinary.com/djbiam1gm/image/upload/v1649704622/VG%20PI/slide04_mini.png" />
</div>

## Project Goals

- Create an App using the following technologies:
    - [ ] React
    - [ ] Redux
    - [ ] Express
    - [ ] Sequelize - Postgres


- Learn and practicw GIT Workflow
- Practice testing


## Features

The main objetive was to create an application in which videogame cards can be seen together with relevant information about them using the external API [rawg](https://rawg.io/apidocs) and from it, do the following:

  - Find video games
  - Filter / sort video games
  - Create a new video game
 
 __IMPORTANT__: To be able to use this external API it was necessary to create an account to obtain an API Key that was then be included in all the requests which were made to rawg simply by adding `?key={API_KEY}` at the end of each endpoint.


### Endpoints/Flags used

  - GET https://api.rawg.io/api/games
  - GET https://api.rawg.io/api/games?search={game}
  - GET https://api.rawg.io/api/genres
  - GET https://api.rawg.io/api/games/{id}
  - GET https://api.rawg.io/api/platforms


### Frontend

A React/Redux app was developed containing the following screens/routes:


- [ ] Landing Page: with the following content:
    - A background image representative of the project
    - Button to access homa page (`Main route`)


- [ ] Home Page : with the following content:
    - Input for searching video games by name
    - Area where video game cards  are displayed, with the following data :
      🔹 Image
      🔹 Name
      🔹 Genre
    - Feature to sort games by rating or alphabetically.
    - Feauture to filter games by genre and by origin (stored in DB or from API )
    - Pagination to search and display 15 games per page


- [ ] Video Game Detail: with the following information:
    - Name
    - Image
    - Genre
    - Description
    - Release date
    - Rating
    - Plataforms

- [ ] Create New Video Game: with the following information:
    - Controlled Form __with JavaScript__ with the following fields:
      🔹 Name
      🔹 Description
      🔹 Release date
      🔹 Rating
    - Feature to select and add many genres
    - Feature to select and add many platforms
    - Button to create new video game


### Database

The database model was created with the following entities 

- [ ] Video game with the following properties:
  - ID
  - Name
  - Description
  - Release date
  - Rating
- [ ] Genre with the following properties:
  - ID
  - Name
- [ ] Platform with the following properties:
  - ID
  - Name



#### Backend

Se debe desarrollar un servidor en Node/Express con las siguientes rutas:

__IMPORTANTE__: No está permitido utilizar los filtrados, ordenamientos y paginados brindados por la API externa, todas estas funcionalidades tienen que implementarlas ustedes.

- [ ] __GET /videogames__:
  - Obtener un listado de los videojuegos
  - Debe devolver solo los datos necesarios para la ruta principal
- [ ] __GET /videogames?name="..."__:
  - Obtener un listado de las primeros 15 videojuegos que contengan la palabra ingresada como query parameter
  - Si no existe ningún videojuego mostrar un mensaje adecuado
- [ ] __GET /videogame/{idVideogame}__:
  - Obtener el detalle de un videojuego en particular
  - Debe traer solo los datos pedidos en la ruta de detalle de videojuego
  - Incluir los géneros asociados
- [ ] __GET /genres__:
  - Obtener todos los tipos de géneros de videojuegos posibles
  - En una primera instancia deberán traerlos desde rawg y guardarlos en su propia base de datos y luego ya utilizarlos desde allí
- [ ] __POST /videogame__:
  - Recibe los datos recolectados desde el formulario controlado de la ruta de creación de videojuego por body
  - Crea un videojuego en la base de datos


#### Testing
- [ ] Al menos tener un componente del frontend con sus tests respectivos
- [ ] Al menos tener una ruta del backend con sus tests respectivos
- [ ] Al menos tener un modelo de la base de datos con sus tests respectivos

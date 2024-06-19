# Practica Calificada 4

Preguntas de Diseño e implementacion:

# Construimos la logica del Juego

Vamos construyendo clase por clase.

• ¿Cómo implementarías la clase Map para representar el mapa del juego, asegurando que se puedan agregar y verificar posiciones de torres y caminos?

# Clase Map

Empezamos creando los atributos y el constructor

![Untitled](Imagenes.png)

Ahora creamos los metodos:

![Untitled](Imagenes%201.png)

![Untitled](Imagenes%202.png)

• Implementa un método en la clase Map llamado isValidPosition(int x, int y) que verifique si una posición es válida para colocar una torre.

![Untitled](Imagenes%203.png)

Con este metodo implementado podemos refactorizar el metodo `insertarTower()`

![Untitled](Imagenes%204.png)

Ahora vamos con la siguiente clase.

# Clase Enemy

Empezamos por crear los atributos y el constructor.

![Untitled](Imagenes%205.png)

Ahora los Getters y setters

![Untitled](Imagenes%206.png)

Ahora crearemos los metodos:

![Untitled](Imagenes%207.png)

• Diseña e implementa una clase SpeedyEnemy que herede de Enemy y tenga una velocidad mayor pero menos vida.

Ahora crearemos clases derivadas para cada tipo de Enemigo

![Untitled](Imagenes%208.png)

![Untitled](Imagenes%209.png)

![Untitled](Imagenes%2010.png)

# Clase Tower

Empezaremos creando los atributos y el constructor.

![Untitled](Imagenes%2011.png)

Ahora crearemos los getters y setters

![Untitled](Imagenes%2012.png)

• ¿Cómo implementarías el método attack(List enemies) en la clase Tower para atacar a los enemigos dentro de su alcance?

Ahora crearemos los metodos 

![Untitled](Imagenes%2013.png)

• Implementa una clase SniperTower que tenga un daño alto y un alcance muy largo pero una velocidad de disparo baja.

Ahora creamos las clases derivadas para cada tipo de Torre:

![Untitled](Imagenes%2014.png)

![Untitled](Imagenes%2015.png)

![Untitled](Imagenes%2016.png)

![Untitled](Imagenes%2017.png)

# Clase Wave

Empezaremos creando los atributos y el constructor.

![Untitled](Imagenes%2018.png)

• ¿Cómo diseñarías la generación de oleadas para que cada oleada sea progresivamente más difícil?

Ahora creamos los metodos:

![Untitled](Imagenes%2019.png)

![Untitled](Imagenes%2020.png)

• Implementa un método en la clase Wave llamado spawnEnemies() que genere los enemigos de la oleada y los coloque en el mapa.

![Untitled](Imagenes%2021.png)

Para implementar este metodo tenemos que hacer una refactorizacion a las clases `Wave`, `Map` y `Enemy` 

En la clase `Wave` se añaden los siguientes atributos

![Untitled](Imagenes%2022.png)

Para la Clase `Map` se añade el siguiente metodo

![Untitled](Imagenes%2023.png)

Para la Clase `Enemy` se añaden los siguientes atributos y sus getters

![Untitled](Imagenes%2024.png)

![Untitled](Imagenes%2025.png)

Y el siguiente setter para devolver la posicion 

![Untitled](Imagenes%2026.png)

# Clase Player

Empezaremos creando los atributos y el constructor.

![Untitled](Imagenes%2027.png)

Ahora creamos los getters:

![Untitled](Imagenes%2028.png)

- ¿Cómo actualizarías la puntuación del jugador y la salud de la base cuando un enemigo es derrotado o alcanza la base?

Ahora creamos los metodos:

![Untitled](Imagenes%2029.png)

![Untitled](Imagenes%2030.png)

![Untitled](Imagenes%2031.png)

# Clase Game

Empezaremos creando los atributos y el constructor.

![Untitled](Imagenes%2032.png)

Ahora creamos los metodos:

![Untitled](Imagenes%2033.png)

![Untitled](Imagenes%2034.png)

![Untitled](Imagenes%2035.png)

Ahora creamos las Interfaces y clases de Mocking:

# Interfaz EnemyFactory

Creamos la interfaz

![Untitled](Imagenes%2036.png)

Creamos las clases:

## Clase BasicEnemyFactory

![Untitled](Imagenes%2037.png)

## Clase FastEnemyFactory

![Untitled](Imagenes%2038.png)

## Clase BossEnemyFactory

![Untitled](Imagenes%2039.png)

# Interfaz TowerFactory

Creamos la interfaz

![Untitled](Imagenes%2040.png)

## Clase CannonTowerFactory

![Untitled](Imagenes%2041.png)

## Clase LaserTowerFactory

![Untitled](Imagenes%2042.png)

## Clase ArrowTowerFactory

![Untitled](Imagenes%2043.png)
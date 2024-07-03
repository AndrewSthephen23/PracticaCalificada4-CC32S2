# Practica Calificada 4

Preguntas de Diseño e implementacion:

# Construimos la logica del Juego

Vamos construyendo clase por clase.

• ¿Cómo implementarías la clase Map para representar el mapa del juego, asegurando que se puedan agregar y verificar posiciones de torres y caminos?

# Clase Map

Empezamos creando los atributos y el constructor

![Untitled](Imagenes/Untitled.png)

Ahora creamos los metodos:

![Untitled](Imagenes/Untitled%201.png)

![Untitled](Imagenes/Untitled%202.png)

• Implementa un método en la clase Map llamado isValidPosition(int x, int y) que verifique si una posición es válida para colocar una torre.

![Untitled](Imagenes/Untitled%203.png)

Con este metodo implementado podemos refactorizar el metodo `insertarTower()`

![Untitled](Imagenes/Untitled%204.png)

Ahora vamos con la siguiente clase.

# Clase Enemy

Empezamos por crear los atributos y el constructor.

![Untitled](Imagenes/Untitled%205.png)

Ahora los Getters y setters

![Untitled](Imagenes/Untitled%206.png)

Ahora crearemos los metodos:

![Untitled](Imagenes/Untitled%207.png)

• Diseña e implementa una clase SpeedyEnemy que herede de Enemy y tenga una velocidad mayor pero menos vida.

Ahora crearemos clases derivadas para cada tipo de Enemigo

![Untitled](Imagenes/Untitled%208.png)

![Untitled](Imagenes/Untitled%209.png)

![Untitled](Imagenes/Untitled%2010.png)

# Clase Tower

Empezaremos creando los atributos y el constructor.

![Untitled](Imagenes/Untitled%2011.png)

Ahora crearemos los getters y setters

![Untitled](Imagenes/Untitled%2012.png)

• ¿Cómo implementarías el método attack(List enemies) en la clase Tower para atacar a los enemigos dentro de su alcance?

Ahora crearemos los metodos 

![Untitled](Imagenes/Untitled%2013.png)

• Implementa una clase SniperTower que tenga un daño alto y un alcance muy largo pero una velocidad de disparo baja.

Ahora creamos las clases derivadas para cada tipo de Torre:

![Untitled](Imagenes/Untitled%2014.png)

![Untitled](Imagenes/Untitled%2015.png)

![Untitled](Imagenes/Untitled%2016.png)

![Untitled](Imagenes/Untitled%2017.png)

# Clase Wave

Empezaremos creando los atributos y el constructor.

![Untitled](Imagenes/Untitled%2018.png)

• ¿Cómo diseñarías la generación de oleadas para que cada oleada sea progresivamente más difícil?

Ahora creamos los metodos:

![Untitled](Imagenes/Untitled%2019.png)

![Untitled](Imagenes/Untitled%2020.png)

• Implementa un método en la clase Wave llamado spawnEnemies() que genere los enemigos de la oleada y los coloque en el mapa.

![Untitled](Imagenes/Untitled%2021.png)

Para implementar este metodo tenemos que hacer una refactorizacion a las clases `Wave`, `Map` y `Enemy` 

En la clase `Wave` se añaden los siguientes atributos

![Untitled](Imagenes/Untitled%2022.png)

Para la Clase `Map` se añade el siguiente metodo

![Untitled](Imagenes/Untitled%2023.png)

Para la Clase `Enemy` se añaden los siguientes atributos y sus getters

![Untitled](Imagenes/Untitled%2024.png)

![Untitled](Imagenes/Untitled%2025.png)

Y el siguiente setter para devolver la posicion 

![Untitled](Imagenes/Untitled%2026.png)

# Clase Player

Empezaremos creando los atributos y el constructor.

![Untitled](Imagenes/Untitled%2027.png)

Ahora creamos los getters:

![Untitled](Imagenes/Untitled%2028.png)

- ¿Cómo actualizarías la puntuación del jugador y la salud de la base cuando un enemigo es derrotado o alcanza la base?

Ahora creamos los metodos:

![Untitled](Imagenes/Untitled%2029.png)

![Untitled](Imagenes/Untitled%2030.png)

![Untitled](Imagenes/Untitled%2031.png)

# Clase Game

Empezaremos creando los atributos y el constructor.

![Untitled](Imagenes/Untitled%2032.png)

Ahora creamos los metodos:

![Untitled](Imagenes/Untitled%2033.png)

![Untitled](Imagenes/Untitled%2034.png)

![Untitled](Imagenes/Untitled%2035.png)

Ahora creamos las Interfaces y clases de Mocking:

# Interfaz EnemyFactory

Creamos la interfaz

![Untitled](Imagenes/Untitled%2036.png)

Creamos las clases:

## Clase BasicEnemyFactory

![Untitled](Imagenes/Untitled%2037.png)

## Clase FastEnemyFactory

![Untitled](Imagenes/Untitled%2038.png)

## Clase BossEnemyFactory

![Untitled](Imagenes/Untitled%2039.png)

# Interfaz TowerFactory

Creamos la interfaz

![Untitled](Imagenes/Untitled%2040.png)

## Clase CannonTowerFactory

![Untitled](Imagenes/Untitled%2041.png)

## Clase LaserTowerFactory

![Untitled](Imagenes/Untitled%2042.png)

## Clase ArrowTowerFactory

![Untitled](Imagenes/Untitled%2043.png)
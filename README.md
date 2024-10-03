# Snake Game Documentation

## English Version

### Overview
This project implements a simple **Snake Game** using HTML, CSS, and JavaScript. The goal of the game is for the snake to grow as much as possible by eating food that appears on the game board, without colliding with the walls or its own body.

### Files Structure
1. **index.html** - The main HTML file, defining the structure of the game interface.
2. **styles.css** - The CSS file responsible for the visual layout and design of the game.
3. **script.js** - The JavaScript file containing the game logic (snake movement, collisions, and score).
4. **Font Awesome** - Icons for the directional arrows in the controls (via CDN).

### Features
- **Dynamic Snake Movement**: The snake moves in the direction chosen by the player using arrow keys or control buttons.
- **Food Generation**: The snake grows by eating randomly placed food items.
- **Score Tracking**: The player's score increases with each piece of food consumed.
- **High Score Persistence**: The game stores the highest score in local storage, so it remains between game sessions.
- **Game Over Detection**: The game ends if the snake hits the walls or collides with itself.
- **On-Screen Controls**: In addition to keyboard input, the game provides on-screen buttons for controlling the snake.

### Code Breakdown

#### HTML (`index.html`)
- The structure is composed of:
    - A wrapper that contains the game board and the score details.
    - A grid-based **play-board** where the snake moves and the food appears.
    - A **controls** section with four directional buttons, each linked to an arrow key event.
    - The JavaScript is linked at the end to ensure it is loaded after the DOM is ready.

#### CSS (`styles.css`)
- **Play Board**: A 30x30 grid where the snake moves.
- **Snake and Food Styling**: The snake’s body (`.head`) is styled with a light blue color, while the food (`.food`) is red.
- **Responsive Design**: The wrapper adjusts based on the viewport size (using `vmin` for width and height).
- **Controls Styling**: Four Font Awesome icons are used for the arrow controls, arranged in a flexbox.

#### JavaScript (`script.js`)
- **Variables**:
    - `snakeX`, `snakeY`: The snake’s initial position.
    - `velocityX`, `velocityY`: The direction of the snake’s movement.
    - `foodX`, `foodY`: The coordinates of the food.
    - `score` and `highScore`: Tracks the player’s current and highest score.
    - `snakeBody`: An array representing the snake's body, which grows as it eats food.
    - `gameOver`: A flag to check if the game is over.
    - `setIntervalId`: Controls the game loop.

- **Main Functions**:
    - `changeFoodPosition`: Randomly places the food on the grid.
    - `changeDirection`: Updates the direction of the snake based on keyboard input or button click.
    - `initGame`: Updates the game state (snake movement, collisions, score update, etc.).
    - `handleGameOver`: Stops the game and displays a game-over message.

- **Game Flow**:
    - The game starts with the snake moving in a fixed direction. The player can control the snake using arrow keys or the on-screen buttons.
    - Every time the snake eats food, its body grows, and the score increases.
    - If the snake hits a wall or itself, the game ends, and a **Game Over** message appears.

### How to Play
1. Start the game by pressing any of the arrow keys or on-screen controls.
2. The snake moves continuously in the current direction.
3. Guide the snake to eat the food without colliding with the walls or its own body.
4. The game is over if the snake runs into the grid’s boundaries or itself.
5. The score and high score are displayed at the top of the game board.

---

## Versión en Español

### Descripción General
Este proyecto implementa un sencillo juego de **Serpiente** utilizando HTML, CSS y JavaScript. El objetivo del juego es hacer que la serpiente crezca lo máximo posible comiendo la comida que aparece en el tablero, sin chocar con las paredes o con su propio cuerpo.

### Estructura de Archivos
1. **index.html** - El archivo principal de HTML, que define la estructura de la interfaz del juego.
2. **styles.css** - El archivo CSS que se encarga del diseño visual del juego.
3. **script.js** - El archivo JavaScript que contiene la lógica del juego (movimiento de la serpiente, colisiones, y puntaje).
4. **Font Awesome** - Iconos para las flechas direccionales en los controles (vía CDN).

### Funcionalidades
- **Movimiento Dinámico de la Serpiente**: La serpiente se mueve en la dirección elegida por el jugador usando las teclas de flechas o botones de control.
- **Generación de Comida**: La serpiente crece comiendo los alimentos colocados aleatoriamente.
- **Seguimiento del Puntaje**: El puntaje del jugador aumenta con cada pieza de comida consumida.
- **Persistencia del Puntaje Más Alto**: El juego almacena el puntaje más alto en el almacenamiento local, por lo que persiste entre sesiones.
- **Detección de Fin de Juego**: El juego termina si la serpiente choca con las paredes o con su propio cuerpo.
- **Controles en Pantalla**: Además de la entrada del teclado, el juego proporciona botones en pantalla para controlar la serpiente.

### Desglose del Código

#### HTML (`index.html`)
- La estructura se compone de:
    - Un contenedor que incluye el tablero de juego y los detalles del puntaje.
    - Un **play-board** basado en una cuadrícula donde se mueve la serpiente y aparece la comida.
    - Una sección de **controles** con cuatro botones direccionales, cada uno vinculado a un evento de tecla de flecha.
    - El archivo JavaScript se vincula al final para asegurarse de que se cargue después de que el DOM esté listo.

#### CSS (`styles.css`)
- **Tablero de Juego**: Una cuadrícula de 30x30 donde se mueve la serpiente.
- **Estilo de la Serpiente y la Comida**: El cuerpo de la serpiente (`.head`) tiene un color azul claro, mientras que la comida (`.food`) es roja.
- **Diseño Responsivo**: El contenedor se ajusta según el tamaño de la ventana (usando `vmin` para el ancho y la altura).
- **Estilo de Controles**: Se usan cuatro iconos de Font Awesome para los controles de flechas, dispuestos en un flexbox.

#### JavaScript (`script.js`)
- **Variables**:
    - `snakeX`, `snakeY`: La posición inicial de la serpiente.
    - `velocityX`, `velocityY`: La dirección del movimiento de la serpiente.
    - `foodX`, `foodY`: Las coordenadas de la comida.
    - `score` y `highScore`: Rastrea el puntaje actual y el más alto del jugador.
    - `snakeBody`: Un array que representa el cuerpo de la serpiente, que crece a medida que come comida.
    - `gameOver`: Una bandera para verificar si el juego ha terminado.
    - `setIntervalId`: Controla el bucle del juego.

- **Funciones Principales**:
    - `changeFoodPosition`: Coloca aleatoriamente la comida en la cuadrícula.
    - `changeDirection`: Actualiza la dirección de la serpiente en función de la entrada del teclado o del clic en un botón.
    - `initGame`: Actualiza el estado del juego (movimiento de la serpiente, colisiones, actualización del puntaje, etc.).
    - `handleGameOver`: Detiene el juego y muestra un mensaje de **Game Over**.

- **Flujo del Juego**:
    - El juego comienza con la serpiente moviéndose en una dirección fija. El jugador puede controlar la serpiente usando las teclas de flechas o los botones en pantalla.
    - Cada vez que la serpiente come comida, su cuerpo crece y el puntaje aumenta.
    - Si la serpiente choca con una pared o con ella misma, el juego termina y aparece un mensaje de **Game Over**.

### Cómo Jugar
1. Comienza el juego presionando cualquiera de las teclas de flecha o los controles en pantalla.
2. La serpiente se mueve continuamente en la dirección actual.
3. Guía a la serpiente para que coma la comida sin chocar con las paredes o su propio cuerpo.
4. El juego termina si la serpiente se estrella contra los límites de la cuadrícula o contra sí misma.
5. El puntaje y el puntaje más alto se muestran en la parte superior del tablero del juego.
+++

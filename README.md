# Estructura de un juego pygame

## Inicializacion 

- como todo programa de python se debe inplementar modulo o ibrerias a utilizar
`import pygame`

- inicializar pygame inicializando la funcion init() comienza todos los modulos de pygame importados.
`pygame.init()`

## Visualizacion de la ventana

`ventana = pygame.display.set_mode((600, 400))`

- set_mode() es la funcion encargada de definir el tamaño de la ventana. En el ejemplo, se esta definiendo una ventana de 600 px de ancho, por 400 px alto.

`pygame.display.c_caption("mi ventana")`

- set_caption() es la funcion que añade un titulo a la ventana.

### Funcion set_mode ()

`set_mode_size = (0.01).flags = 0, depth = 0,display = 0`

- size = (600,400) : define el tamaño de la ventana.
    - vallores:
        -pygame_FULLSCREEN
        -pygame_RESISTABLE
    - ejemplo
        - flags = pygame.FULLSCREEN  |   pygame.RESISTABLE : pantalla completa, dimenciones modificables.

##  bucle del juego o game loup

- bucle infinito que se interrumpira cuando se cumplan ciertos crietrios
- reloj interno
- en cada iteracion de bucle del juego podemos mover un personaje del juego. o tener en cuenta la linea de llegada lo que quiere decir que "Game Over". 
- cada interacion es una oportunidad de actualizar todos los datos reacionados con el estado actual de la partida
- en cada iteracion se realiza las siguientes tareas:

    1. comprobar que no se alcanza las condicciones de partida, en cuyo caso se interrumpe el bucle
    2. actualizar los recursos necesarios
    3. obtener las entradas de sistema, o de interacin del jugador.
    4. actualizar las identidades y caracteristicas del juego.
    5. refrescar la pantalla.

## superficies pygame
- superficie:
    - elemento geometrico
    - linea, poligono, imagen, texto que se muestra en la pantalla
    - el poligono se puede o no rellenar de color
    - las superficies se crea de diferente manera dependiendo del tipo
        - imagen: imagen.load()
        - texto: texto.render()
        - superficie generica: pygame.superfice()
        - vetana de juego: pygame.dispay.set_mode()



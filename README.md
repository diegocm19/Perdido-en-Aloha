# Ruta A* - Perdido en Aloha

Juego de laberinto estilo arcade inspirado en Pac-Man. Controla a Pac-Man, recoge los cinco puntos y escapa del fantasma mientras el algoritmo A* calcula las rutas mas cortas del tablero.

## Descripcion

En cada partida se genera un laberinto nuevo con atajos y rutas alternativas. La linea amarilla muestra el camino mas corto hacia el punto mas cercano. El fantasma utiliza A* para perseguir al jugador, pero se mueve cada dos turnos para que la partida sea ganable.

El objetivo es recoger todos los puntos sin ser atrapado. Al completar la mision se muestra la pantalla de victoria con el total de movimientos.

## Controles

- Flechas del teclado: mover a Pac-Man.
- `W`, `A`, `S`, `D`: mover a Pac-Man.
- Botones direccionales: utiles en pantallas tactiles.
- **Nuevo laberinto**: comenzar una partida con un mapa diferente.

## Requisitos

- Un navegador moderno con soporte para HTML5 Canvas y JavaScript.
- No requiere Node.js, dependencias, servidor ni conexion a internet.
- Funciona en escritorio y dispositivos moviles.

## Como ejecutar

### Opcion 1: abrir directamente

1. Descarga o clona este repositorio.
2. Abre `index.html` con Chrome, Edge, Firefox o Safari.
3. Empieza a jugar con las flechas, WASD o los botones en pantalla.

### Opcion 2: servidor local

Desde la carpeta del proyecto puedes usar cualquier servidor estatico. Por ejemplo, si tienes Python instalado:

```bash
python -m http.server 8000
```

Despues abre `http://localhost:8000` en el navegador.

## Algoritmo A*

El juego implementa A* con:

- **Coste real `g(n)`**: movimientos realizados desde el inicio.
- **Heuristica `h(n)`**: distancia Manhattan hasta el objetivo.
- **Prioridad `f(n) = g(n) + h(n)`**: selecciona primero los nodos mas prometedores.

A* se utiliza para calcular la ruta amarilla hacia el punto mas cercano y para actualizar la persecucion del fantasma despues de los movimientos del jugador.

## Estructura

- `index.html`: interfaz, estilos, generacion del laberinto, logica del juego y algoritmo A*.
- `README.md`: documentacion del proyecto.

## Licencia

Proyecto creado con fines educativos y de practica de algoritmos de busqueda.

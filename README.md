# ExploracionMarte

Este proyecto simula la exploración de un robot tipo Perseverance Rover en Marte. El rover tiene dos objetivos principales: primero, realizar una exploración con un punto de origen y un punto de destino utilizando diversos algoritmos de búsqueda, y segundo, realizar un descenso hacia un cráter utilizando algoritmos metaheurísticos para encontrar la mejor ruta. Durante la simulación, se implementaron algoritmos de búsqueda ciega, heurística y metaheurística para cumplir con estas misiones.

### Algoritmos de Búsqueda Implementados
### 1. Exploración con Punto de Origen y Destino
Para la exploración con un punto de origen y un punto de destino, se utilizaron los siguientes algoritmos de búsqueda:

- Búsqueda en Anchura (BFS): Este algoritmo explora los nodos en niveles, primero explorando los más cercanos al nodo inicial antes de continuar con los más lejanos. Es útil para encontrar la solución más cercana en términos de pasos.

- Búsqueda en Profundidad (DFS): Este algoritmo explora profundamente cada rama antes de retroceder. A pesar de que es más rápido, no garantiza la solución óptima y puede entrar en ciclos si no se controla correctamente.

- Búsqueda Greedy: La búsqueda Greedy toma decisiones basadas en el nodo más cercano al objetivo sin considerar el camino ya recorrido. Aunque es eficiente, no siempre encuentra la solución óptima.

- A (A-Star):* A diferencia de la búsqueda Greedy, A* evalúa tanto el costo del camino recorrido como una estimación del costo restante para llegar al objetivo. Es un algoritmo eficiente y preciso que garantiza encontrar la ruta óptima si se aplica la heurística adecuada.

### 2. Descenso al Cráter
Para el descenso hacia el cráter, se utilizaron dos algoritmos metaheurísticos que son más adecuados para problemas de optimización continua, donde el objetivo es encontrar una solución en un espacio de búsqueda más complejo y no necesariamente en una cuadrícula de nodos discretos:

- Hill Climbing: Este algoritmo iterativamente se mueve hacia el vecino más prometedor (el que tiene el valor más bajo en una función de coste o energía). Aunque puede encontrar soluciones rápidas, es susceptible a quedar atrapado en óptimos locales.

- Recocido Simulado (Simulated Annealing): Basado en el proceso físico de enfriamiento de materiales, este algoritmo explora el espacio de soluciones de manera probabilística. A través de un proceso de "enfriamiento", permite escapar de óptimos locales y eventualmente converge hacia una solución cercana al óptimo global.

## Simulación del Perseverance Rover
En la simulación, el rover parte desde un punto inicial dentro de un mapa de Marte (representado como una cuadrícula 2D) y tiene como objetivo alcanzar un punto de destino o realizar un descenso al cráter. Para cada uno de estos casos, se aplicaron los algoritmos mencionados para explorar el terreno y tomar decisiones de ruta.

Exploración con Punto de Origen y Destino: Los algoritmos de búsqueda (BFS, DFS, Greedy, A*) fueron utilizados para planificar la ruta desde el punto inicial hasta el objetivo, teniendo en cuenta obstáculos y limitaciones del terreno.

Descenso al Cráter: Los algoritmos de Hill Climbing y Recocido Simulado fueron implementados para encontrar la mejor ruta hacia el cráter, optimizando la trayectoria de descenso en un entorno más complejo y dinámico.

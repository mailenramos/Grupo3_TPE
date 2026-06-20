1. Algoritmo Greedy
Ordena los paquetes de mayor a menor peso. Decidimos hacerlo así para sacarnos de encima los bultos más grandes primero, asegurándonos de que entren de entrada y no nos dejen mucho peso  al final.

Control: Para cada paquete recorre los camiones. Lo sube de forma definitiva al primer camión que tenga espacio libre y cumpla con la restriccion de refrigeracion

Resultado: Con nuestros datos de prueba encontró una solución (0 kg afuera) revisando solo 4 opciones.

2. Algoritmo Backtracking
Prueba todas las combinaciones posibles . Para cada paquete analiza qué pasa si lo mete en el camión 1, en el 2, en el 3, etc., y también prueba la opción de no asignarlo, en caso de que después entren otros paquetes más convenientes (Dejo uno de 50kg para que entren 2 paquetes de 30 kg).

solGreedy: Para que el algoritmo tarde menos, ejecutamos Greedy al principio de todo para obtener solGreedy. Como Greedy ya nos dio un resultado de 0 kg afuera, el Backtracking arranca sabiendo que ese es el número que encontro Greedy(solucion optima, no la mejor)

Podas:

Por espacio y refrigeracion: Si un camión no tiene lugar o no tiene refrigeración para la comida, ese camino se descarta.

->Sin el resultado de Greedy: Para 4 paquetes y 3 camiones (contando la opción de dejar paquetes abajo),  total de 256 combinaciones.

->Con el resultado de Greedy: el Backtracking solo tuvo que revisar 25 candidatos.

La conclusión es que lo mejor es combinar las dos cosas: usar el bajo costo computacional de Greedy para encontrar una buena solución inicial y usar ese resultado para achicar el trabajo del Backtracking.
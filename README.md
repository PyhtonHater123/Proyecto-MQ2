Grover's Algorithm with IBM Quantum Backends
Este repositorio implementa el Algoritmo de Grover utilizando la librería Qiskit y los backends reales de IBM Quantum (ibm_brisbane y ibm_sherbrooke) a través de qiskit_ibm_runtime. Se incluyen implementaciones del algoritmo para 2, 3 y 4 cúbits, junto con la visualización de los resultados de medición como histogramas de probabilidad.

Descripción general del proyecto
El algoritmo de Grover permite resolver problemas de búsqueda no estructurados con una ventaja cuadrática sobre los algoritmos clásicos. Este proyecto demuestra su funcionamiento en distintos tamaños de espacio de búsqueda utilizando dispositivos cuánticos reales, y muestra cómo el estado objetivo es amplificado en la salida del circuito.

Componentes principales:
Inicialización: Se crea una superposición uniforme de todos los estados aplicando compuertas Hadamard.

Oráculo: Se define un oráculo sencillo con puertas CZ que marca estados como 11 (para 2 cúbits) o 101 y 110 (en versiones extendidas).

Difusor generalizado (difuse): Se implementa un operador de inversión alrededor del promedio usando compuertas X, H y una compuerta Z controlada por múltiples cúbits (realizada mediante una envoltura con MCXGate).

Ejecución remota: Se transpilan los circuitos y se ejecutan en los dispositivos ibm_sherbrooke y ibm_brisbane mediante el servicio IBM Runtime.

Visualización: Se grafican los resultados con matplotlib y qiskit.visualization.plot_histogram.

Casos implementados:
grover_circuit: Implementación de Grover con 2 cúbits (estado objetivo |11⟩).

grover_circuit2: Versión con 3 cúbits, con oráculo marcando los estados |101⟩ y |110⟩.

grover_circuit3: Extensión a 4 cúbits, demostrando escalabilidad.

Requisitos
Python 3.7+

Qiskit

qiskit_ibm_runtime

Matplotlib

Cuenta activa en IBM Quantum (se requiere token de autenticación)

# Quantum Exercises: Hadamard, J Gate, and H-X Circuit

Este repositorio contiene simulaciones de ejercicios de computación cuántica de *Quantum Country*, usando Qiskit y Python. Exploramos:
- Verificación de \( H \cdot H = I \) (puerta de Hadamard).
- Por qué la matriz \( J \) no es una puerta cuántica válida.
- Un circuito \( H \rightarrow X \) con simulación.

## Requisitos
- Python 3.11+
- Dependencias: `pip install -r requirements.txt`

## Cómo ejecutar
1. Clona el repositorio: `git clone https://github.com/TuUsuario/QuantumExercises.git`
2. Instala dependencias: `pip install -r requirements.txt`
3. Ejecuta: `python quantum_exercises.py`

## Resultados
- **Ejercicio 1**: \( H \cdot H \) da la matriz identidad, confirmando que \( H \) es su propia inversa.
- **Ejercicio 2**: \( J \) no es unitaria (\( J^\dagger J \neq I \)) y colapsa el estado \( \frac{|0\rangle - |1\rangle}{\sqrt{2}} \) a \( [0, 0] \).
- **Ejercicio 3**: Circuito \( H \rightarrow X \), resultados simulados con 1024 shots.

### Histograma del circuito H -> X
![Histograma](histogram.png)

### Circuito
 ┌───┐┌───┐┌─┐
 q_0: ┤ H ├┤ X ├┤M├
 └───┘└───┘└╥┘
c: 1/═══════════╩═
             0


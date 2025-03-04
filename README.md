# Quantum Exercises: Hadamard, J Gate, and H-X Circuit

Este repositorio contiene simulaciones de ejercicios de computación cuántica inspirados en *Quantum Country*, implementados con Qiskit y Python. El objetivo es explorar conceptos fundamentales de puertas cuánticas y circuitos, mientras aprendemos a simularlos computacionalmente.

## Objetivos del proyecto
- **Ejercicio 1**: Verificar que \( H \cdot H = I \), demostrando que la puerta de Hadamard es su propia inversa.
- **Ejercicio 2**: Analizar por qué la matriz \( J \) no es una puerta cuántica válida, ya que no es unitaria y no preserva la norma de ciertos estados.
- **Ejercicio 3**: Simular un circuito cuántico \( H \rightarrow X \), analizando su comportamiento con 1024 shots.

## Requisitos
- Python 3.11+
- Dependencias:
 pip install -r requirements.txt

## Instalación y ejecución
1. Clona el repositorio:
 git clone https://github.com/Fisman23/QuantumExercises.git
2. Navega al directorio:
   cd QuantumExercises
3. Instala las dependencias
4. Ejecuta el script:
   python quantum_exercises.py

## Resultados
- **Ejercicio 1**: \( H \cdot H \) resulta en la matriz identidad \( I \), confirmando que \( H \) es su propia inversa:
    [[1.  0.]
    [0.  1.]]

   **Ejercicio 2**: La matriz \( J \) no es unitaria, ya que \( J^\dagger J \neq I \):
    [[1. 1.]
    [1. 1.]]

  
Además, colapsa el estado \( \frac{|0\rangle - |1\rangle}{\sqrt{2}} \) a \( [0, 0] \), violando la conservación de la norma.
- **Ejercicio 3**: El circuito \( H \rightarrow X \) produce probabilidades cercanas al 50% para \( |0\rangle \) y \( |1\rangle \), como se esperaba:
  
  {'0': 497, '1': 527}


### Histograma del circuito \( H \rightarrow X \)
![Histograma del circuito H -> X](histogram.png)

### Visualización del circuito
El circuito simulado aplica una puerta de Hadamard \( H \) seguida de una puerta \( X \) (NOT cuántico) y una medición:

      ┌───┐┌───┐┌─┐
 q_0: ┤ H ├┤ X ├┤M├
     └───┘└───┘└╥┘
c: 1/═══════════╩═
                0


## Conclusiones
- La puerta \( H \) es crucial para crear superposiciones, y su propiedad \( H \cdot H = I \) la hace reversible.
- La matriz \( J \) falla como puerta cuántica porque no es unitaria, lo que tiene implicaciones en criptografía cuántica (ej. protocolos como QKD).
- El circuito \( H \rightarrow X \) demuestra cómo las puertas cuánticas interactúan, produciendo resultados probabilísticos típicos de la superposición.

## Autor
Joseph Guagnelli - Estudiante de ciberseguridad y computación cuántica. Apasionado por la intersección entre cuántica, ciberseguridad y análisis de datos.

## Licencia
MIT License - Consulta el archivo [LICENSE](LICENSE) para más detalles.

## Contribuciones
¡Siéntete libre de hacer fork y contribuir! Abre un issue o un pull request si tienes ideas o mejoras.






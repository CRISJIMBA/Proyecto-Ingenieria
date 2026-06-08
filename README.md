# Portafolio de Ingeniería: Análisis Termodinámico del Ciclo de Carnot

## 1. Introducción
Este proyecto forma parte de una actividad práctica de ingeniería orientada a la automatización de procesos mediante el uso de Inteligencia Artificial (IA) y el desarrollo de algoritmos en Python. El objetivo es resolver problemas de ingeniería termodinámica aplicando principios físicos y metodologías de diseño de software.

## 2. Definición del Problema
El análisis se centra en el **Ciclo de Carnot**, el cual define la eficiencia máxima teórica de un motor térmico que opera entre dos fuentes de temperatura. El problema planteado es determinar la eficiencia del ciclo y el calor ($Q_H$) requerido para generar un trabajo útil ($W$) específico.

### Aplicación en el Mundo Real
Para asimilar esto a aplicaciones industriales, imagina que eres un ingeniero de energía encargado de **optimizar una planta de generación eléctrica**:
* **Optimización de Desperdicio:** Si conoces la temperatura de tu fuente fría (ej. un río o ambiente) y tu fuente caliente (ej. calderas), este algoritmo te permite calcular instantáneamente si tu planta está operando cerca de su límite teórico o si hay pérdidas de energía excesivas (entropía).
* **Diseño de HVAC:** Es vital en sistemas de aire acondicionado industrial y refrigeración criogénica para calcular cuánto trabajo eléctrico (compresor) necesitas para mover calor de una zona fría a una caliente.

## 3. Metodología y Algoritmo
Siguiendo las mejores prácticas de ingeniería, el proceso de diseño se dividió en:
1. **Modelado Matemático:** Conversión de unidades ($^\circ C \to K$) y aplicación de las leyes de la termodinámica.
2. **Estructuración:** Creación de un script en Python que valida la lógica termodinámica (asegurando que $T_H > T_L$).
3. **Automatización:** Implementación de variables dinámicas para facilitar la toma de decisiones basada en datos.

## 4. Código Fuente
```python
def calcular_ciclo_carnot():
    # El algoritmo solicita los parámetros operativos de la máquina
    print("--- Calculadora de Eficiencia de Carnot ---")
    
    t_celsius_h = float(input("Temperatura fuente caliente (°C): "))
    t_celsius_l = float(input("Temperatura fuente fría (°C): "))
    trabajo_deseado = float(input("Trabajo útil deseado (Joules): "))
    
    t_h = t_celsius_h + 273.15
    t_l = t_celsius_l + 273.15
    
    if t_h <= t_l:
        print("Error: El ciclo no es físicamente posible.")
        return

    eficiencia = 1 - (t_l / t_h)
    q_h = trabajo_deseado / eficiencia
    
    print(f"\nResultados:")
    print(f"Eficiencia teórica: {eficiencia * 100:.2f} %")
    print(f"Calor requerido (Qh): {q_h:.2f} Joules")

if __name__ == "__main__":
    calcular_ciclo_carnot()

import math

def calcular_trayectoria():
    print("--- Calculadora de Proyectiles ---")
    # Entrada de datos
    v0 = float(input("Ingresa la velocidad inicial (m/s): "))
    angulo_grados = float(input("Ingresa el ángulo de lanzamiento (grados): "))
    
    # Conversión a radianes para las funciones trigonométricas
    theta = math.radians(angulo_grados)
    g = 9.81
    
    # Cálculos
    tiempo_vuelo = (2 * v0 * math.sin(theta)) / g
    altura_max = (v0**2 * (math.sin(theta)**2)) / (2 * g)
    alcance = (v0**2 * math.sin(2 * theta)) / g
    
    # Resultados
    print(f"\nResultados:")
    print(f"Tiempo de vuelo: {tiempo_vuelo:.2f} s")
    print(f"Altura máxima: {altura_max:.2f} m")
    print(f"Alcance horizontal: {alcance:.2f} m")

if __name__ == "__main__":
    calcular_trayectoria()

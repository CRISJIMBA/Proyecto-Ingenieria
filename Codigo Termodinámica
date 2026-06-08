def calcular_ciclo_carnot():
    print("--- Calculadora de Eficiencia de Carnot ---")
    
    # Entrada de datos
    t_celsius_h = float(input("Temperatura fuente caliente (°C): "))
    t_celsius_l = float(input("Temperatura fuente fría (°C): "))
    trabajo_deseado = float(input("Trabajo útil deseado (Joules): "))
    
    # Conversión a Kelvin
    t_h = t_celsius_h + 273.15
    t_l = t_celsius_l + 273.15
    
    # Validar que sea un ciclo posible
    if t_h <= t_l:
        print("Error: La fuente caliente debe estar a mayor temperatura que la fría.")
        return

    # Cálculos
    eficiencia = 1 - (t_l / t_h)
    q_h = trabajo_deseado / eficiencia
    
    # Resultados
    print(f"\nResultados:")
    print(f"Eficiencia teórica: {eficiencia * 100:.2f} %")
    print(f"Calor requerido (Qh): {q_h:.2f} Joules")

if __name__ == "__main__":
    calcular_ciclo_carnot()

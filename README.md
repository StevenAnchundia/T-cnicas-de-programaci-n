class Estudiante:
    def __init__(self, nombre, codigo, carrera, nota_promedio):
        self.nombre = nombre
        self.codigo = codigo
        self.carrera = carrera
        self.nota_promedio = nota_promedio
    
    def mostrar_informacion(self):
        print(f"\n=== Información del Estudiante ===")
        print(f"Nombre: {self.nombre}")
        print(f"Código: {self.codigo}")
        print(f"Carrera: {self.carrera}")
        print(f"Nota Promedio: {self.nota_promedio}/10")
        print(f"=================================")
    
    def actualizar_nota(self, nueva_nota):
        if 0 <= nueva_nota <= 10:
            self.nota_promedio = nueva_nota
            print(f"Nota actualizada exitosamente para {self.nombre}")
            return True
        else:
            print(f"Error: La nota debe estar entre 0 y 10")
            return False


if __name__ == "__main__":
    estudiante1 = Estudiante("María González", "EC2024001", "Ingeniería en Sistemas", 8.5)
    
    estudiante2 = Estudiante("Carlos Rodríguez", "EC2024002", "Administración", 7.8)
    
    print("Bienvenido al Sistema de Gestión de Estudiantes")
    print("=" * 50)
    
    estudiante1.mostrar_informacion()
    estudiante2.mostrar_informacion()
    
    print("\nActualizando notas...")
    estudiante1.actualizar_nota(9.0)
    estudiante2.actualizar_nota(8.2)
    
    print("\nInformación actualizada:")
    estudiante1.mostrar_informacion()
    estudiante2.mostrar_informacion()
    
    print("\nIntentando actualizar con nota inválida:")
    estudiante1.actualizar_nota(15.0)

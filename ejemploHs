class Nodo:
    def __init__(self, nombre, cedula, prioridad):
        self.nombre = nombre
        self.cedula = cedula
        self.prioridad = prioridad
        self.siguiente = None


class Lista:
    def __init__(self):
        self.cabeza = None

    def agregar_con_prioridad(self, nombre, cedula, prioridad):
        nodo = Nodo(nombre, cedula, prioridad)

        # Caso 1: lista vacía
        if self.cabeza is None:
            self.cabeza = nodo

        # Caso 2: mayor prioridad que el primero
        elif prioridad < self.cabeza.prioridad:
            nodo.siguiente = self.cabeza
            self.cabeza = nodo

        # Caso 3: buscar la posición correcta
        else:
            actual = self.cabeza
            while (actual.siguiente is not None and
                   actual.siguiente.prioridad <= prioridad):
                actual = actual.siguiente

            nodo.siguiente = actual.siguiente
            actual.siguiente = nodo

    def mostrar(self):
        actual = self.cabeza
        while actual is not None:
            print(f"Nombre: {actual.nombre} | Cédula: {actual.cedula} | Prioridad: {actual.prioridad}")
            actual = actual.siguiente

lista = Lista()
lista.agregar_con_prioridad("Usuario2", 222, 2)
lista.agregar_con_prioridad("Usuario1", 111, 1)
lista.agregar_con_prioridad("Usuario4", 333, 3)

lista.mostrar()

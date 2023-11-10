# NietoRomero_Marta_PJ
import random
def primerjuego():
    # Seleccionar un número aleatorio entre 0 y 99
    número = random.randint(0,99)
    intentos = 0
    adivinanza = None
    print("Bienvenido al juego")
    while adivinanza != número:
       try: 
           adivinanza = int(input("Adivina el número (entre 0 y 99)."))
           if 0 <= adivinanza <= 99:
               intentos += 1
               if adivinanza < número:
                   print("Te has quedado corto. Inténtalo de nuevo.")

               if adivinanza > número:
                   print("Te has pasado. Inténtalo de nuevo.")
           else: 
               print("Felicidades. Has adivinado el número.")
       except ValueError:
           print("Por favor, ingresa un número entero válido.")
if __name__ == "__main__":
    primerjuego()

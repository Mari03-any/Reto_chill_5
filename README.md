# Reto_chill_5
Elaborado por Maria Fernanda Parra Osorio-1014980661
1. Dado la figura de la imagen, desarrolle:

<div align='center'>
<figure> <img src="https://i.postimg.cc/FRvCmpxx/image.png" alt="" width="400" height="auto"/></br>
<figcaption><b></b></figcaption></figure>
</div>

+ Una función matemática para calcular el volumen y el área superficial.
+ Cree dos funciones en python para calcular los valores antes establecidos, al ingresar por teclado `r1`, `r2` y `h`.
+ Revise como utilizar el valor de `pi` usando *import math* y *math.pi*
## Desarrollo
```python
import math

def calcular_area_esfera(r1):
  area_esfera = 4 * math.pi * (r1 ** 2)
  return area_esfera
def calcular_volumen_esfera(r1):
  volumen_esfera =  (4/3) * math.pi * (r1 ** 3)
  return volumen_esfera
def calcular_area_cono(r2, h):
    if r2 > 0 and h > 0:
        g = math.sqrt(r2**2 + h**2) 
        area_lateral = math.pi * r2 * g
        area_base = math.pi * (r2 ** 2)
        area_cono = area_lateral + area_base
        return area_cono
def calcular_volumen_cono(r2, h):
    volumen_cono = (1/3) * math.pi * (r2 ** 2) * h
    return volumen_cono


if __name__ == "__main__":
    r1 = float(input("Ingrese el radio 1 de la esfera:"))
    r2 = float(input("Ingrese el radio 2 del cono:"))
    h = float(input("Ingrese la altura del cono:"))
    if r1 > 0 and r2 > 0 and h > 0:
      area_esfera = calcular_area_esfera(r1)
      volumen_esfera = calcular_volumen_esfera(r1)
      area_cono = calcular_area_cono(r2, h)
      volumen_cono = calcular_volumen_cono(r2, h)
      print(f"El área de la esfera es: {area_esfera:.2f}")
      print(f"El volumen de la esfera es: {volumen_esfera:.2f}")
      print(f"El área total del cono es: {area_cono:.2f}")
      print(f"El volumen de la cono es: {volumen_cono:.2f}")
    else:
      print("El radio y la altura deben ser números positivos.")
```
### Resultado
[![Captura-de-pantalla-2024-12-08-231512.png](https://i.postimg.cc/NMs9ymh6/Captura-de-pantalla-2024-12-08-231512.png)](https://postimg.cc/JyF4vyz0)</br></br>
2. Dado la figura de la imagen, desarrolle:

<div align='center'>
<figure> <img src="https://i.postimg.cc/1t4MrzsL/image.png" alt="" width="400" height="auto"/></br>
<figcaption><b></b></figcaption></figure>
</div>

+ Una función matemática para calcular el área y el perimetro.
+ Cree dos funciones en python para calcular los valores antes establecidos, al ingresar por teclado `r`, `a` y `b`.
+ Revise como utilizar el valor de `pi` usando *import math* y *math.pi*

## Desarrollo
```python
import math

def calcular_perimetro_rectangulo(a, b):
  perimetro_rectangulo = 2 * (a + b)
  return perimetro_rectangulo
def calcular_area_rectangulo(a, b):
  area_rectangulo = a * b
  return area_rectangulo
def calcular_perimetro_circulo(r):
  perimetro_circulo = 2 * math.pi * r
  return perimetro_circulo
def calcular_area_circulo(r):
  area_circulo = math.pi * (r ** 2)
  return area_circulo

if __name__ == "__main__":
    a = float(input("Ingrese el primer lado del rectangulo:"))
    b = float(input("Ingrese el segundo lado del rectangulo:"))
    r = float(input("Ingrese el radio de los circulos:"))
    if a > 0 and b > 0 and r > 0:
      perimetro_rectangulo = calcular_perimetro_rectangulo(a, b)
      area_rectangulo = calcular_area_rectangulo(a, b)
      perimetro_circulo = calcular_perimetro_circulo(r)
      area_circulo = calcular_area_circulo(r)
      print(f"El perimetro del rectangulo es: {perimetro_rectangulo:.2f}")
      print(f"El área del rectangulo es: {area_rectangulo:.2f}")
      print(f"El perimetro de los circulos es: {perimetro_circulo:.2f}")
      print(f"El área de los circulos es: {area_circulo:.2f}")
    else:
      print("El radio y los lados deben ser números positivos.")
```
### Resultado
[![Captura-de-pantalla-2024-12-08-235230.png](https://i.postimg.cc/fRgS3Jzp/Captura-de-pantalla-2024-12-08-235230.png)](https://postimg.cc/0zDyF5J0)</br></br>
3. Diseñe una función que calcule la cantidad de carne de aves en kilos si se tienen N gallinas, M gallos y K pollitos cada uno pesando 6 kilos, 7 kilos y 1 kilo respectivamente.

4. Haga un programa que utilice una función para calcular el valor de un préstamo `C` usando interés compuesto del `i` por `n` meses.

5. Escriba un programa que pida 5 números reales y calcule las siguientes operaciones usando una función para cada una:
  + El promedio
  + El promedio multiplicativo (multilplica todos y luego calcula la raíz de la cantidad de operandos)
  + La potencia del mayor número elevado al menor número
  + La raíz cúbica del menor número

6. Consultar qué es y cómo funciona *pip* en python.

7. Hacer un listado de módulos populares para python que se puedan instalar com *pip* y consultar cómo instalarlos.

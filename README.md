# Reto_chill_5
Elaborado por Maria Fernanda Parra Osorio_1014980661
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
        g = math.sqrt(r2**2 + h**2) #Formula de la generatriz
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

## Desarrollo
```python
def calcular_carne_aves(n_gallinas, m_gallos, k_pollitos):
    peso_gallina = 6 
    peso_gallo = 7    
    peso_pollito = 1  
    
    carne_total = (n_gallinas * peso_gallina) + (m_gallos * peso_gallo) + (k_pollitos * peso_pollito)
    return carne_total

if __name__ == "__main__":
  n = int(input("Ingrese el número de gallinas: "))
  m = int(input("Ingrese el número de gallos: "))
  k = int(input("Ingrese el número de pollitos: "))

if n >= 0 and m >= 0 and k >= 0:
    carne_total = calcular_carne_aves(n, m, k)
    print(f"La cantidad total de carne de aves es: {carne_total} kilos.")
else:
    print("El número de aves debe ser un valor positivo o cero.")
```
### Resultado
[![Captura-de-pantalla-2024-12-09-071216.png](https://i.postimg.cc/RFWgb4zy/Captura-de-pantalla-2024-12-09-071216.png)](https://postimg.cc/Kky71XjD) </br></br>
4. Haga un programa que utilice una función para calcular el valor de un préstamo `C` usando interés compuesto del `i` por `n` meses.

## Desarrollo
```python
def calcular_prestamo(p, i, n):
  return p * (1 + i)**n #P: es el valor inicial del prestamo

if __name__ == "__main__":
    p = float(input("Ingrese el valor inicial del prestamo:"))
    i = float(input("Ingrese el interes compuesto(en porcentaje):"))
    n = float(input("Ingrese el numero de meses:"))
    
    if p > 0 and i > 0 and n > 0:
        valor_c = calcular_prestamo(p, i, n)
        print(f"El valor del prestamo de {n} meses es: {valor_c:.2f}")
    else:
        print("Ingrese valores postitivos")
```
### Resultado
[![Captura-de-pantalla-2024-12-09-180629.png](https://i.postimg.cc/Nft4r5n4/Captura-de-pantalla-2024-12-09-180629.png)](https://postimg.cc/CdvD3LSB)</br></br>
5. Escriba un programa que pida 5 números reales y calcule las siguientes operaciones usando una función para cada una:
  + El promedio
  + El promedio multiplicativo (multilplica todos y luego calcula la raíz de la cantidad de operandos)
  + La potencia del mayor número elevado al menor número
  + La raíz cúbica del menor número

## Desarrollo
```python
import math

def calcular_promedio(n, i, x, y, z):
  return (n + i + x + y + z)/5
def calcular_promedio_multiplicativo(n, i, x, y, z):
  return (n * i * x * y * z)** (1 / 5)
def potencia_mayor_menor(n, i, x, y, z):
    mayor = max(n, i, x, y, z)
    menor = min(n, i, x, y, z)
    return mayor ** menor
def raiz_menor(n, i, x, y, z):
    menor = min(n, i, x, y, z)
    return menor ** (1 / 3)
  
if __name__ == "__main__":
  n = float(input("Ingrese el primer numero real:"))
  i = float(input("Ingrese el segundo numero real:"))
  x = float(input("Ingrese el tercer numero real:"))
  y = float(input("Ingrese el cuarto numero real:"))
  z = float(input("Ingrese el quinto numero real:"))
  
if n > 0 and i > 0 and x > 0 and y > 0 and z > 0:
    promedio = calcular_promedio(n, i, x, y, z)
    promedio_multiplicativo = calcular_promedio_multiplicativo(n, i, x, y, z)
    potencia = potencia_mayor_menor(n, i, x, y, z)
    raiz_cubica = raiz_menor(n, i, x, y, z)
    
    print(f"Promedio: {promedio:.2f}")
    print(f"Promedio multiplicativo: {promedio_multiplicativo:.2f}")
    print(f"Potencia del mayor elevado al menor: {potencia:.2f}")
    print(f"Raíz cúbica del menor: {raiz_cubica:.2f}")
else:
  print("Error: Ingrses solo números reales.")
```
### Resultado
[![Captura-de-pantalla-2024-12-10-220515.png](https://i.postimg.cc/Kc7L2D55/Captura-de-pantalla-2024-12-10-220515.png)](https://postimg.cc/5j0j5vTH)</br></br>

6. Consultar qué es y cómo funciona *pip* en python.
*pip*(Pip installer packages) en python es un sistema de gestión de paquetes utilizado para instalar y administrar paquetes o modulos que se integran en python.
+ Para el uso de *pip* primeto se confirma que este instalado. </br>
```pip --version``` </br>
Si no, ejecutamos. </br>
```python get-pip.py``` </br>
+ Posteriormente, escogemos que modulo o paquete vamos a instalar. </br>
```pip install <nombre_del_paquete>``` </br>
Por otro lado, si queremos desinstalar un modulo o paquete. </br>
```pip uninstall <nombre_del_paquete>``` </br>
+ Para listar los modulos ya instalados utilizamos: </br>
```pip list``` </br>
+ Para actualizar un paquete utilizamos: </br>
```pip install --upgrade <nombre_del_paquete>``` </br>
+ La opción `requirements.txt` se utiliza para instalar una lista de modulos y sus versiones.  </br>
```pip install -r requirements.txt```  </br>
El cual instalará los paquetes `Flask`, `requests` y `numpy` con las versiones especificadas en el archivo.

8. Hacer un listado de módulos populares para python que se puedan instalar com *pip* y consultar cómo instalarlos.

1. **pandas**: Manejo de estructuras de datos como DataFrames y series.
   ```bash
   pip install pandas
   ```
2. **numpy**: Operaciones matemáticas avanzadas y manejo de matrices.
   ```bash
   pip install numpy
   ```
3. **scipy**: Herramientas para cálculos científicos y técnicos.
   ```bash
   pip install scipy
   ```
4. **matplotlib**: Creación de gráficos estáticos y personalizados.
   ```bash
   pip install matplotlib
   ```
5. **seaborn**: Visualización de datos estadísticos con gráficos atractivos.
   ```bash
   pip install seaborn
   ```
6. **bokeh**: Gráficos interactivos y dashboards.
   ```bash
   pip install bokeh
   ```
7. **scikit-learn**: Herramientas para machine learning y minería de datos.
   ```bash
   pip install scikit-learn
   ```
8. **tensorflow**: Framework para aprendizaje profundo (deep learning).
   ```bash
   pip install tensorflow
   ```
9. **torch (PyTorch)**: Framework flexible para deep learning.
   ```bash
   pip install torch torchvision
   ```
10. **flask**: Framework ligero para crear aplicaciones web.
   ```bash
   pip install flask
   ```
11. **requests**: Manejo sencillo de peticiones HTTP.
   ```bash
   pip install requests
   ```
12. **PyPDF2**: Lectura y manipulación de archivos PDF.
   ```bash
   pip install PyPDF2
   ```
13. **pyqt5**: Framework para crear interfaces gráficas.
   ```bash
   pip install pyqt5
   ```
### Referencias
+ Llamas, L. (2024, julio 24). Qué es y cómo usar pip en Python. Luis Llamas. https://www.luisllamas.es/python-como-usar-pip/
+ López, M. (2022, marzo 17). Librerías de Python, ¿qué son y cuáles son las mejores? IMMUNE Technology Institute. https://immune.institute/blog/librerias-python-que-son/

##Fin

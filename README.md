# Reto-08
## 1. De los retos anteriores selecione 3 funciones y escribalas en forma de lambdas.
```python
#Determinar si un número es positivo, negativo o cero.
es_positivo = lambda x: x > 0
es_negativo = lambda x: x < 0
es_cero = lambda x: x == 0

# Area de un triangulo.
area_triangulo = lambda b, h: (b * h) / 2
base = float(input("Ingrese la base: "))
altura = float(input("Ingrese la altura: "))
print(f"Área del triángulo: {area_triangulo(base, altura)}")

#Verificar si un número entero es código ASCII de una vocal minúscula
es_vocal_ascii = lambda n: chr(n) in "aeiou"
```

## 2. De los retos anteriores selecione 3 funciones y escribalas con argumentos no definidos (*args).
```python
#Suma de cuadrados del 1 al 100 (adaptación de Reto 6 - punto 1)
def suma_cuadrados(*args):
    return sum(x**2 for x in args)

#Suma de todos los números impares en un rango (Reto 6 - punto 2 adaptado)
def suma_impares(*args):
    return sum(x for x in args if x % 2 != 0)

#Mínimo o máximo entre varios números (útil en varios retos)
def minimo(*args):
    return min(args)

def maximo(*args):
    return max(args)
```

## 3. Escriba una función recursiva para calcular la operación de la potencia.
```python
def potencia(base: int, exponente: int) -> int:
  if exponente == 0:
    return 1
  return base * potencia(base, exponente - 1)

if __name__ == "__main__":
  b = int(input("Ingrese la base: "))
  e = int(input("Ingrese el exponente: "))
  print("Resultado:", potencia(b, e))
```

## 4. Utilice la siguiente plantilla de code para contar el tiempo:
```python
import time

start_time = time.time()
# instrucciones sobre las cuales se quiere medir tiempo de ejecución
end_time = time.time()

timer = end_time - start_time
print(timer)
```

Realice pruebas para calcular fibonacci con iteración o con recursión. Determine desde que número de la serie la diferencia de tiempo se vuelve significativa.
```python
import time

def fibonacci_iterativo(n):
    a, b = 0, 1
    for _ in range(n):
        a, b = b, a + b
    return a

def fibonacci_recursivo(n):
    if n <= 1:
        return n
    return fibonacci_recursivo(n - 1) + fibonacci_recursivo(n - 2)

# Cambiar este número para hacer pruebas
n = 33

# FIBONACCI ITERATIVO
start_time = time.time()
resultado_iter = fibonacci_iterativo(n)
end_time = time.time()
tiempo_iter = end_time - start_time
print(f"[ITERATIVO] Fibonacci({n}) = {resultado_iter}")
print(f"Tiempo iterativo: {tiempo_iter:.6f} segundos")

# FIBONACCI RECURSIVO
start_time = time.time()
resultado_rec = fibonacci_recursivo(n)
end_time = time.time()
tiempo_rec = end_time - start_time
print(f"[RECURSIVO] Fibonacci({n}) = {resultado_rec}")
print(f"Tiempo recursivo: {tiempo_rec:.6f} segundos")

# Pausar para que la consola no se cierre
input("\nPresiona ENTER para salir...")
```
Desde n = 35, la diferencia en tiempo frente al método iterativo se torna significativa, pasa de milisegundos a segundos


## 5. Crear cuenta en [stackoverflow](https://stackoverflow.com/) y adjuntar imagen en el repo
  <img width="1894" height="889" alt="image" src="https://github.com/user-attachments/assets/c8895f16-9616-4e4b-ae0a-822c4b7b19b8" />




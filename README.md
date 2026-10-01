Evaluación Práctica: Programación en Java - Estructuras de Control

Asignatura: Programación / Lógica de Programación  
Proyecto: PharmaSys - Control de Ventas de Farmacia  
Grupo: N° 2  

### Integrantes

| N° | Nombres y Apellidos | Rol / Aporte |
| :---: | :--- | :--- |
| 1 | Alex Cabrera | Integrante |
| 2 | Erick Cordónez | Análisis E-P-S y Prueba de Escritorio |
| 3 | Kevin Garcés | Algoritmo y Pseudocódigo |
| 4 | Cristian Gómez | Desarrollo de Código Java |
| 5 | Esteban Zambrano | Documentación y Repositorio GitHub |

Descripción del ejercicio
Basándonos en la imagen del enunciado, aquí tienes la descripción detallada del ejercicio para que la agregues a tu documentación (en el reporte o archivo README):   Descripción del Ejercicio: GRUPO 2 – PharmaSys: FarmaciaObjetivo principal: Desarrollar una solución funcional en Java que permita gestionar el registro de ventas de una farmacia aplicando estructuras de selección, ciclos, validación de datos, contadores y acumuladores.   Funcionamiento:El sistema solicita al usuario un número $N$ de ventas a procesar, validando que sea un valor entero mayor a cero.   Por cada iteración, el programa solicita los datos del producto: código, nombre, precio unitario, categoría (1: Genérico, 2: Comercial, 3: Especializado), cantidad y si requiere o no receta médica.   Validación de restricciones: Se evalúa mediante una estructura condicional que si el medicamento pertenece a la categoría Especializado y no cuenta con receta médica, la venta debe ser rechazada automáticamente, incrementando el contador de transacciones rechazadas.   Cálculos y Descuentos: Para las ventas aceptadas, se calcula el subtotal y se aplican descuentos basados tanto en la categoría del producto (mediante un selector switch) como en el volumen de compra por cantidad.   Resultados: Al finalizar el ciclo de las $N$ ventas, el sistema muestra en consola un resumen totalizador que incluye el monto total vendido, el total general descontado y la cantidad de ventas rechazadas.

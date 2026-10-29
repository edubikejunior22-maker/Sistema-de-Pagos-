# Sistema de pagos en C#

Programa de consola en C# que muestra el uso de **herencia y polimorfismo** con un sistema de pagos.

## Descripción

Se define una clase base `Pago` con un método virtual `Calcular(decimal monto)` que devuelve el monto. A partir de ella se crean distintos tipos de pago, cada uno con su propia forma de calcular el total a pagar. Los pagos se guardan en un arreglo de tipo `Pago` y se muestra el total.

## Clases

| Clase | Hereda de | Comportamiento |
|-------|-----------|----------------|
| `Pago` | — | Método virtual `Calcular(decimal monto)` que devuelve el monto sin cambios |
| `Efectivo` | `Pago` | Usa el cálculo de la clase base (sin comisión) |
| `Tarjeta` | `Pago` | Sobrescribe `Calcular()` y suma **3 %** de comisión |
| `Transferencia` (reto extra) | `Pago` | Sobrescribe `Calcular()` y suma **1 %** de comisión |

## Conceptos aplicados

- Herencia
- Métodos virtuales y `override`
- Polimorfismo (arreglo de `Pago` con objetos de distintas clases)
- Principio abierto/cerrado: `Transferencia` se agregó sin modificar las demás clases

## Requisitos

- [.NET SDK](https://dotnet.microsoft.com/download) 6.0 o superior

## Cómo ejecutarlo

```bash
dotnet new console -n SistemaPagos
cd SistemaPagos
# reemplaza el Program.cs generado por el de este proyecto
dotnet run
```

## Ejemplo de salida

<img width="768" height="153" alt="image" src="https://github.com/user-attachments/assets/61615ce7-3e5d-4663-bb77-5b927d6ee0d7" />


## Autor

Pedro Junior Hernández  
Ingeniería de Software, Universidad Central del Este (UCE)  
Matrícula: 2025-1422

Profesor : GAMALIER REYES

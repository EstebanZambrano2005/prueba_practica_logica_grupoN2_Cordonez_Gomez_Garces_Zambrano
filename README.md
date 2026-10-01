# prueba_practica_logica_grupoN2_Cordonez_Gomez_Garces_Zambrano
FARMACIA - PRUEBA PRACTICA
<div align="center">

<!-- BANNER DE BIENVENIDA CON EFECTO DE ANIMACIÓN DE TEXTO -->
<img src="https://demolab.com⚡+EXAMEN+PRÁCTICO+DE+SOFTWARE+⚡;✨+UNIVERSIDAD+TÉCNICA+DE+AMBATO+✨;🏥+SISTEMA+PHARMASYS+ACTIVADO+🏥" alt="Typing SVG" />

<p align="center">
  <img src="https://shields.io" />
  <img src="https://shields.io" />
</p>

---

<!-- EFECTO DE MOVIMIENTO CONTINUO (MARQUEE) -->
<marquee scrollamount="6" behavior="scroll" direction="left">
  <b>🚀 INTEGRANTES DEL GRUPO: Cristian Gómez • Esteban Zambrano • Erick Cordonez • Kevin Garcés 🚀</b>
</marquee>

</div>

---

## 📂 1. Estructura Dinámica del Repositorio

> 💡 *Haz clic en las secciones de abajo para desplegar el contenido de manera interactiva.*

<details>
<summary><b>📂 Ver Organización de Carpetas (Clic aquí)</b></summary>
<br>

```text
📁 prueba-practica-logica/
├── 📁 ejercicio-1/          → Código Fuente Ejercicio1.java
├── 📁 ejercicio-2/          → Código Fuente Ejercicio2.java (PharmaSys)
├── 📁 evidencia-manual/     → Escaneos (Análisis, Pseudocódigo, Escritorio)
└── 📁 capturas-ejecucion/   → Evidencias en VS Code
```
</details>

---

## 🏥 2. Ejercicio 2 – PharmaSys: Farmacia

### 📊 Flujo Metodológico

```mermaid
graph TD
    A[📥 Inicio: Ingreso de Datos] --> B{🔍 ¿Datos Válidos?};
    B -- NO --> C[❌ Venta Rechazada];
    B -- SI --> D{💊 Categoría Especial};
    D -- Requiere Receta y NO tiene --> C;
    D -- Con Receta / General --> E[⚙️ Procesar Switch de Descuentos];
    E --> F[💰 Calcular Total Neto];
    F --> G[📊 Reporte Final Impreso];
    style A fill:#00D2FF,stroke:#333,stroke-width:2px
    style C fill:#FF4B4B,stroke:#333,stroke-width:2px
    style G fill:#52FF52,stroke:#333,stroke-width:2px
```

<details>
<summary><b>💻 VER CÓDIGO FUENTE OPTIMIZADO (Clic aquí)</b></summary>
<br>

```java
package ejercicio_2;

import java.util.Scanner;

public class Ejercicio2 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        double totalVendido = 0, totalDescontado = 0;
        int ventasRechazadas = 0;
        
        System.out.print("Cantidad de ventas a procesar (N): ");
        int n = scanner.nextInt();
        
        int contador = 0;
        while (contador < n) {
            System.out.println("\n--- REGISTRO DE VENTA #" + (contador + 1) + " ---");
            scanner.nextLine(); 
            
            System.out.print("Producto: ");
            String producto = scanner.nextLine();
            System.out.print("Precio: ");
            double precio = scanner.nextDouble();
            System.out.print("Categoría (1=Gral, 2=Antibiótico, 3=Restringido): ");
            int categoria = scanner.nextInt();
            System.out.print("Cantidad: ");
            int cantidad = scanner.nextInt();
            System.out.print("¿Tiene receta? (S/N): ");
            char receta = scanner.next().toUpperCase().charAt(0);
            
            if (precio <= 0 || cantidad <= 0 || (categoria < 1 || categoria > 3)) {
                System.out.println("❌ Datos incorrectos.");
                ventasRechazadas++; contador++; continue;
            }
            if ((categoria == 2 || categoria == 3) && receta != 'S') {
                System.out.println("❌ Requiere receta.");
                ventasRechazadas++; contador++; continue;
            }
            
            double subtotal = precio * cantidad;
            double porcentajeDescuento = 0;
            
            switch (categoria) {
                case 1: if (cantidad > 5) porcentajeDescuento = 0.05; break;
                case 2: if (cantidad > 3) porcentajeDescuento = 0.10; break;
                case 3: porcentajeDescuento = 0.0; break;
            }
            
            double descuentoCalculado = subtotal * porcentajeDescuento;
            double totalPagar = subtotal - descuentoCalculado;
            
            totalVendido += totalPagar;
            totalDescontado += descuentoCalculado;
            
            System.out.printf("✅ Procesada. Total: \$.2f\n", totalPagar);
            contador++;
        }
        
        System.out.println("\n=================================");
        System.out.println("📊 REPORTE FINAL - PHARMASYS");
        System.out.println("=================================");
        System.out.printf("💰 Total Neto Vendido: \$.2f\n", totalVendido);
        System.out.printf("📉 Total Monto Descontado: \$.2f\n", totalDescontado);
        System.out.println("❌ Total Ventas Rechazadas: " + ventasRechazadas);
        
        scanner.close();
    }
}
```
</details>

---

## ⚡ 3. Tecnologías Empleadas

| Stack | Nivel de Implementación | Barra de Carga |
| :--- | :--- | :--- |
| **Java SE 17** | Avanzado / Estructuras de Control | `██████████████████▒ 90%` |
| **Markdown** | Interfaz Visual Interactiva | `████████████████████ 100%` |
| **VS Code** | Entorno de Compilación Oficial | `██████████████████▒ 95%` |

---

<div align="center">

### ✨ Entregable desarrollado con éxito por el equipo. ✨
*Haga clic en la estrella (Star) del repositorio si el resultado fue satisfactorio.*

</div>

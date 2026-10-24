# Conclusiones y recomendaciones — TechCore

> **Versión 2 (cifras corregidas).** La versión anterior (`versiones_anteriores/`) mostraba importes ×10 por un error de interpretación regional en el CSV transformado. Los porcentajes no cambiaron; los importes sí. Las cifras de este documento salen del modelo validado (`Total = Σ subtotales × (1 − descuento)`).

**Alcance:** 30.000 facturas · 60.059 renglones · 16.715 clientes · 6 sucursales · 4 ciudades · sep-2014 → sep-2025.
**Ventas netas:** $456.491.670.000 COP · **Descuentos otorgados:** $11.538.230.000 (2,5 % de la venta bruta).

## 1. Hallazgos

### 1.1 Concentración geográfica

| Ciudad | Ventas netas | Facturas | % |
|---|---:|---:|---:|
| Medellín | $203,9 mil M | 13.460 | 44,7 % |
| Bogotá | $139,6 mil M | 9.107 | 30,6 % |
| Pereira | $56,6 mil M | 3.723 | 12,4 % |
| Cali | $56,4 mil M | 3.710 | 12,4 % |

Medellín y Bogotá concentran el 75 % de las ventas. Medellín #1 es la sucursal líder ($112,8 mil M) y Cali, con una sola sucursal, vende lo mismo que Pereira.

### 1.2 Marcas y productos

| Marca | Ventas netas | Unidades |
|---|---:|---:|
| Lenovo | $114,9 mil M | 21.697 |
| HP | $94,4 mil M | 19.877 |
| Dell | $84,6 mil M | 16.189 |
| Apple | $76,1 mil M | 10.783 |
| Asus | $32,4 mil M | 8.097 |
| Acer | $21,5 mil M | 7.178 |
| Samsung | $12,5 mil M | 2.618 |
| MSI | $8,3 mil M | 1.374 |
| Microsoft | $8,0 mil M | 1.717 |
| Razer | $3,8 mil M | 482 |

* Producto de mayor ingreso: **Lenovo Legion 5 Pro** ($41,2 mil M). Más vendido en unidades: **HP Spectre x360** (7.726).
* Precio medio por unidad más alto: Razer ($7,96 M) y Apple ($7,05 M); el más bajo, Acer ($2,99 M).

### 1.3 Evolución temporal y sesgo de cobertura

* 2015-2024 es estable: entre $40,2 y $43,1 mil M por año.
* **2014 (desde septiembre) y 2025 (hasta el 3 de septiembre) son años parciales.** La "caída" que se ve en un gráfico anual simple es un artefacto del corte del dataset.
* Comparado de forma justa (mismo período), **2025 YTD crece +1,0 %** frente a 2024. El dashboard usa la medida `VentasAnioAnterior`, recortada a la última fecha con ventas, y una media móvil de 12 meses para evitar esa lectura errónea.
* No hay estacionalidad marcada: los meses oscilan entre $36 y $40 mil M y todos los días de la semana venden parecido.

### 1.4 Pagos y descuentos

* Tarjeta crédito 40,1 % · débito 20,4 % · transferencia 15,0 % · billetera digital 9,8 % · efectivo 9,8 % · **no especificado 4,8 %**.
* El 70,1 % de las facturas no lleva descuento; 14,8 % lleva 5 %, 10,1 % lleva 10 % y 5,0 % lleva 15 %.

### 1.5 Clientes

* Edad media 34,5 años; 64,5 % hombres, 35,5 % mujeres.
* Cada cliente compra 1,79 veces en promedio y **el 50,5 % es recurrente**.

## 2. Recomendaciones

1. **Capturar el método de pago de forma obligatoria** en caja: hoy 1 de cada 20 facturas queda sin dato.
2. **Revisar el plan de crecimiento regional:** Cali y Pereira rinden igual con 1 sucursal cada una frente a 2 de Bogotá y Medellín; evaluar una segunda sucursal en la plaza con mejor ticket.
3. **Programa de fidelización** para el 50 % de clientes de una sola compra, apalancando la billetera digital y la tarjeta (60 % del pago).
4. **Política de descuentos:** el descuento medio es bajo (2,5 %), pero el 30 % de las facturas lo recibe; medir si el 15 % aumenta el ticket o solo erosiona margen (falta costo para calcular margen).
5. **Portafolio:** Acer, Samsung, MSI, Microsoft y Razer suman menos del 12 % de las ventas; definir si son marcas de nicho o candidatas a racionalizar.
6. **Datos:** incorporar costo de producto para pasar de ventas a margen.

## 3. Trabajo futuro

* Margen y rentabilidad por producto.
* Cohortes de retención de clientes.
* Productividad por vendedor (ventas por factura y por sucursal).

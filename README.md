# Optimización de la Producción en una Fábrica de Productos Electrónicos

## Descripción del Proyecto

Este proyecto aborda un problema de optimización en una fábrica que produce 6 tipos de productos electrónicos: **ratones inalámbricos**, **teclados**, **altavoces**, **cargadores de móvil**, **cámaras web** y **auriculares**. El objetivo principal es maximizar el beneficio total de la producción, teniendo en cuenta las restricciones de capacidad de producción de cada tipo de producto, así como los beneficios individuales de cada uno.

El modelo está formulado como un **problema de programación lineal (PL)**, que busca determinar cuántas unidades de cada producto deben ser producidas para maximizar el beneficio total de la fábrica.

## Objetivo del Problema

El objetivo del problema es maximizar el beneficio total generado por la producción de los productos electrónicos. La función objetivo es la suma del beneficio de cada tipo de producto, determinado por su precio de venta. Las restricciones del problema incluyen límites en la capacidad de producción de cada tipo de producto y requisitos de producción mínima o máxima.

### Función Objetivo

La función objetivo se expresa como:

$$
f(x) = 20x_1 + 35x_2 + 25x_3 + 15x_4 + 50x_5 + 30x_6
$$

Donde:

- \( x_1 \) es el número de ratones inalámbricos.
- \( x_2 \) es el número de teclados.
- \( x_3 \) es el número de altavoces.
- \( x_4 \) es el número de cargadores de móvil.
- \( x_5 \) es el número de cámaras web.
- \( x_6 \) es el número de auriculares.


# Restricciones del Problema Primal

1. **Restricción 1**: La producción total de todos los productos no debe superar las 1000 unidades:

$$
x_1 + x_2 + x_3 + x_4 + x_5 + x_6 \leq 1000
$$

2. **Restricción 2**: La producción de ratones inalámbricos, teclados y auriculares no puede superar las 250 unidades:

$$
x_1 + x_2 + x_6 \leq 250
$$

3. **Restricción 3**: La producción de altavoces y cargadores de móvil no puede superar las 300 unidades:

$$
x_3 + x_4 \leq 300
$$

4. **Restricción 4**: La producción de cámaras web no puede superar las 100 unidades:

$$
x_5 \leq 100
$$

5. **Restricción 5**: Se deben producir al menos 50 unidades de ratones inalámbricos:

$$
x_1 \geq 50
$$

6. **Restricción 6**: La producción de teclados no debe superar las 200 unidades:

$$
x_2 \leq 200
$$


## Modelo Primal y Dual

El modelo se ha implementado utilizando **Pyomo**, una herramienta de optimización en Python. Se ha formulado tanto el modelo **primal** como el **dual** para resolver el problema y obtener una solución óptima. El modelo primal busca maximizar el beneficio bajo las restricciones mencionadas, mientras que el modelo dual proporciona información adicional sobre la sensibilidad de las restricciones.

### Variables de Decisión

Las variables de decisión representan el número de unidades de cada producto que deben ser producidas:

- \( x_1 \): Unidades de ratones inalámbricos.
- \( x_2 \): Unidades de teclados.
- \( x_3 \): Unidades de altavoces.
- \( x_4 \): Unidades de cargadores de móvil.
- \( x_5 \): Unidades de cámaras web.
- \( x_6 \): Unidades de auriculares.

### Restricciones

Las restricciones representan las limitaciones de capacidad de producción y los requisitos mínimos o máximos de producción para ciertos productos.

## Análisis de Sensibilidad

Se ha realizado un análisis de sensibilidad para observar cómo afectan las variaciones en los coeficientes de la función objetivo y las restricciones sobre la solución óptima. Esto es útil para entender la estabilidad del modelo ante posibles cambios en los datos de entrada, como variaciones en la demanda de productos o cambios en los costos de producción.

## Herramientas y Bibliotecas

- **Pyomo**: Para la formulación y resolución del modelo de programación lineal.
- **GLPK (GNU Linear Programming Kit)**: El solucionador utilizado para resolver el modelo de optimización.

## Resultados

Al resolver el modelo, se obtiene la cantidad óptima de unidades a producir para cada tipo de producto que maximiza el beneficio total. Además, se obtienen los valores de las variables duales, que proporcionan información sobre el impacto de las restricciones en el beneficio total.

## Conclusión

Este modelo de optimización permite a la fábrica determinar la cantidad óptima de productos a producir, maximizando el beneficio total bajo las restricciones de capacidad de producción y requisitos de los productos. El análisis de sensibilidad también ofrece una visión valiosa sobre la robustez del modelo y cómo las variaciones en los parámetros afectan la solución.

## Uso

Para ejecutar el modelo, asegúrate de tener **Python** instalado junto con las bibliotecas necesarias:

- Pyomo
- GLPK

Puedes instalar Pyomo usando pip:

```bash
pip install pyomo
```

## Información personal

Link al repositorio: https://github.com/Nachosanchezz/Investigacion-operativa.git
Usuario de Github: Nachosanchezz

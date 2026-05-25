
# 🧩 Práctica de Algoritmia: Modularidad y Funciones 🚀👩‍💻

**Objetivo:** 🎯 Desarrollar la capacidad de abstracción dividiendo problemas complejos en subrutinas independientes 🧩, utilizando el paso de parámetros 🔀 y el retorno de valores 📥.

## 🟢 Nivel Básico: Módulos de Acción (Sin Retorno) 🎬

### 🧾 Ejercicio 1: Estandarización de Tickets de Venta 🛍️

**Contexto:** 🏪 Administración de Emprendimiento local.

Una nueva cafetería ☕ y comercializadora de productos locales 🍯 necesita que todos los tickets de venta 🧾 impresos por su sistema de terminal de punto de venta (TPV) 💻 tengan exactamente el mismo formato visual en el encabezado y el pie de página, independientemente de qué cajero 🧑‍🍳 esté cobrando.

**Requerimientos del Sistema:**

1. 👥 El programa principal simulará el cobro de tres clientes diferentes, pidiendo al cajero el total a cobrar para cada uno 💵.

2. 🚧 **Restricción de Arquitectura:** Queda estrictamente prohibido 🚫 programar los textos del logotipo, dirección y mensaje de agradecimiento dentro del flujo principal.

3. 🛠️ Debes diseñar **dos submódulos independientes**: uno para el encabezado ⬆️ y otro para el pie de página ⬇️.

4. 🔄 El programa principal deberá **invocar** (llamar) estos módulos en el momento correcto (antes y después de mostrar el total cobrado) para ensamblar el ticket completo en la pantalla 🖥️.

**📤 Salida Esperada:** ✨

    =================================
    ☕ CAFETERÍA "EL BUEN GRANO" ☕
    📍 Portal Principal, Centro
    =================================
    Total a pagar: $150.50
    ---------------------------------
    ¡Gracias por apoyar el comercio local!
    Vuelva pronto.
    ---------------------------------

## 🟡 Nivel Intermedio: Paso de Parámetros y Retorno 🏓

### 📊 Ejercicio 2: Calculadora de Margen de Ganancia 💰

**Contexto:** 📈 Finanzas para Agroindustrias.

Los estudiantes 🧑‍🎓👩‍🎓 que están formulando su plan de negocios necesitan una herramienta rápida ⚡ que les indique si el precio al que planean vender su producto agroindustrial 🍓 (ej. mermelada artesanal) es financieramente viable 💹.

**Requerimientos del Sistema:**

1. 📝 El programa principal solicitará al usuario ingresar dos datos financieros: el **Costo de Producción** 🏭 (cuánto cuesta hacer el producto) y el **Precio de Venta** 🏷️ (a cuánto lo van a vender al público).

2. 🚧 **Restricción de Arquitectura:** El cálculo matemático 🧮 para descubrir el porcentaje de ganancia no puede estar en el bloque principal 🚫.

3. 🏗️ Debes construir un módulo independiente que **reciba** 📥 (como parámetros) el costo y el precio. Este módulo calculará el porcentaje de utilidad neta y **devolverá** 📤 ese valor numérico al sistema principal.

4. ⚖️ Una vez que el programa principal reciba el resultado, evaluará si el margen es menor al 30% 📉. Si es así, imprimirá una advertencia financiera ⚠️; de lo contrario, indicará que el precio es viable ✅.

**📤 Salida Esperada:** ✨

    --- 📈 SIMULADOR FINANCIERO ---
    Ingresa el costo de producción: 25.00
    Ingresa el precio de venta sugerido: 30.00

    >> Procesando viabilidad...
    >> Margen de ganancia calculado: 16.66%
    >> ⚠️ ADVERTENCIA: El margen es demasiado bajo (menor al 30%). Riesgo de quiebra.

## 🔴 Nivel Avanzado: Arreglos como Parámetros y Lógica Interna 🧠🔥

### 🍅 Ejercicio 3: Auditoría de Calidad en Empacadora 📦

**Contexto:** 🔬 Control de Calidad en exportación agrícola 🌍.

Una empacadora de tomates de invernadero 🍅 tiene estándares estrictos para la exportación 🚢. Una caja de producto (lote) se rechaza automáticamente ❌ si tan solo un tomate está por debajo del peso mínimo permitido (100 gramos) ⚖️.

**Requerimientos del Sistema:**

1. 📋 El programa principal generará un registro estructurado con los pesos individuales de 6 tomates seleccionados al azar 🎲 de la banda transportadora 🛤️.

2. 🚧 **Restricción de Arquitectura:** El programa principal debe delegar la decisión de exportación a un submódulo especializado en control de calidad 🕵️‍♂️.

3. 📦 Debes crear un módulo que reciba como parámetro **la estructura completa** (arreglo) con los pesos 📥.

4. 🔍 El módulo recorrerá los datos internamente, realizará las validaciones necesarias (que ninguna unidad pese menos de 100g) y devolverá una respuesta clara sobre su aprobación o rechazo (verdadero ✅ o falso ❌).

5. 📢 El sistema principal atrapará esta respuesta y emitirá el dictamen final para el operador 🧑‍🔧.

**📤 Salida Esperada:** ✨

    === 🍅 CONTROL DE CALIDAD - LÍNEA 1 🍅 ===
    Lote actual capturado: [105.2, 110.5, 98.4, 120.1, 108.0, 115.3]

    >> Evaluando métricas de exportación...
    >> ❌ LOTE RECHAZADO.
    >> Motivo: Se detectaron unidades por debajo del calibre mínimo (100g).
       Desviando lote a mercado nacional.

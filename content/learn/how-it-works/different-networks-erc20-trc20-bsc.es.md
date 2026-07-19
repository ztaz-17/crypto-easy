---
weight: 260
title: "Cómo NO Perder Dinero: Redes Diferentes (ERC20, TRC20, BSC)"
description: "El error #1 de los principiantes — enviar cripto a la red equivocada. Veamos por qué puedes perder dinero y cómo verificar la red"
category: "how-it-works"
translationKey: "different-networks-erc20-trc20-bsc"
slug: "diferentes-redes-erc20-trc20-bsc"
keywords:
  - ERC20
  - TRC20
  - BSC
  - red incorrecta
  - error de red
  - perder cripto
  - estándar de token
  - USDT red equivocada
  - recuperar fondos
---

## Enviaste USDT — y el Dinero Desapareció. ¿Cómo es Posible?

---

Compraste USDT en un exchange, copiaste la dirección de tu amigo e hiciste la transferencia.

Una hora después tu amigo te escribe: **"No hay dinero."**

Revisas la transacción en la [blockchain](/es/glossary/#blockchain) — estado: "Exitosa." Tu amigo revisa su saldo — cero. Como si el dinero se hubiera esfumado en el aire.

¿Te suena?

Felicidades — acabas de caer en **el error más común de los principiantes**: enviar cripto a la red equivocada.

Y aquí está el detalle:

> **El cripto no desapareció. Simplemente no está donde estás mirando.**

---

## El Error #1 de los Principiantes: Mismos Tokens, Redes Distintas

### Qué Significa "Red" en Cripto

Imagina un **sistema ferroviario**. Hay diferentes líneas:

- ERC20 — la red de Ethereum;
- TRC20 — la red de Tron;
- BSC (BEP-20) — la red de Binance Smart Chain;
- Solana, Polygon, Avalanche — y así sucesivamente.

Ahora imagina que USDT es un **contenedor de carga**. Puede viajar por cualquiera de esas líneas. Pero si envías el contenedor por la línea ERC20 y el destinatario está mirando la línea TRC20 — no verá la carga.

> **Un token — muchas redes.**

### Por Qué es Tan Peligroso

El problema es que USDT (Tether) vive en varias blockchains al mismo tiempo:

| Red | Estándar | Ejemplo de Dirección |
|-----|----------|---------------------|
| Ethereum | ERC20 | 0x... |
| Tron | TRC20 | T... |
| Binance Smart Chain | BEP-20 | 0x... |
| Solana | SPL | ... |
| Avalanche | C-Chain | 0x... |

Todo parece el mismo USDT. Pero técnicamente, son **[tokens](/es/glossary/#token) diferentes** en **blockchains diferentes**. No son compatibles entre sí.

👉 **ERC20 USDT** ≠ **TRC20 USDT** ≠ **BEP-20 USDT**

---

## Por Qué Puedes Perder Dinero

### Escenario 1: Enviado a la Red Equivocada (Fondos "Atascados")

El caso más común.

Estás retirando USDT de un exchange. El exchange te pide que elijas una red. Eliges una al azar o dejas la que viene por defecto.

Si la red de envío no coincide con la red del destinatario, **la transacción se va a un agujero negro**.

Técnicamente, los fondos llegan a la misma dirección (si el formato coincide), pero en una red diferente. El destinatario no puede verlos.

> **El dinero está en la blockchain — pero no puedes acceder a él.**

### Escenario 2: La Dirección Coincide, la Red No

Algunas redes (por ejemplo, Ethereum y BSC) comparten el mismo formato de dirección — `0x...`.

Copias la dirección, envías USDT por BSC, pero el destinatario espera ERC20.

Formalmente:
- la dirección coincide;
- la transacción se completó;
- pero el destinatario revisa su [cartera](/es/glossary/#wallet) ERC20 — vacía.

Los fondos **no se pierden para siempre**, pero tendrás que recuperarlos. Y eso es otra historia aparte.

### Escenario 3: El Exchange No Acepta Tokens en Otra Red

Algunos exchanges solo aceptan USDT en redes específicas. Si envías USDT por Solana a una [cartera](/es/glossary/#wallet) de exchange que solo acepta ERC20, **no acreditarán el depósito**.

El soporte del exchange puede ayudar, pero:

- llevará días o semanas;
- los exchanges cobran una tarifa de recuperación (a menudo hasta 100 USDT);
- no hay garantía de que te ayuden.

---

## Cómo Verificar la Red Antes de Enviar

Hay **reglas simples** que te ahorrarán dinero.

### Regla 1: Siempre Coincide la Red del Remitente y el Destinatario

Antes de presionar "Enviar":

1. Averigua qué red puede usar el destinatario.
2. En el exchange o en tu [cartera](/es/glossary/#wallet), selecciona **exactamente la misma red**.
3. Verifica dos veces.

> **Red del remitente = Red del destinatario.**

### Regla 2: Ignora la "Red por Defecto"

Los exchanges y las carteras suelen mostrar una red preseleccionada por defecto. Y puede que no sea la que necesitas.

Siempre verifica dos veces.

### Regla 3: Mantén una Red por Dirección

Si antes has enviado USDT a una dirección por TRC20 — la próxima vez envía también por TRC20.

No experimentes.

---

## Tabla: USDT en Diferentes Redes

Aquí tienes una referencia rápida de las redes USDT más populares:

| Red | Estándar | Dirección Empieza Con | Comisión de Transferencia | Velocidad |
|-----|----------|----------------------|--------------------------|-----------|
| Ethereum | ERC20 | 0x... | Alta ($3–20) | Media |
| Tron | TRC20 | T... | Baja ($0.5–2) | Rápida |
| Binance Smart Chain | BEP-20 (BSC) | 0x... | Baja ($0.1–0.5) | Rápida |
| Solana | SPL | Aleatoria | Muy baja ($0.01) | Muy rápida |
| Avalanche | C-Chain | 0x... | Baja | Rápida |

> ⚠️ **Importante:** Si ves una dirección que empieza con `0x`, podría ser Ethereum (ERC20), BSC (BEP-20) o Avalanche (C-Chain). ¡No las confundas! Siempre confirma la red.

---

## Qué Hacer Si Ya Enviaste a la Red Equivocada

### No Entres en Pánico

Lo primero y más importante. El cripto no se ha ido a ninguna parte — está en la [blockchain](/es/glossary/#blockchain). En casi todos los casos, puedes recuperar el acceso.

### Si Enviaste desde un Exchange a una Cartera Externa

Este es el caso más sencillo.

Los exchanges tienen una función de **Reclamación** o "Solicitud de Recuperación". Algunos exchanges (por ejemplo, Binance, Bybit) pueden recuperar fondos enviados a la red equivocada si:

- enviaste los fondos a **tu propia dirección** en esa misma red;
- o a una dirección que también te pertenece.

Si la dirección pertenece a otro exchange o servicio — contacta con su soporte.

### Si Enviaste de Cartera a Cartera

Esto es más complicado. Si enviaste tokens en la red equivocada pero tienes la [clave privada](/es/glossary/#private-key) de la dirección receptora, puedes:

- importar tu [frase semilla](/es/glossary/#seed-phrase) / clave privada en una cartera que soporte la red correcta;
- o usar una cartera multired (por ejemplo, MetaMask con la red BSC agregada).

### Si Enviaste a un Exchange en la Red Equivocada

Este es el peor escenario.

Enviaste USDT por ERC20, pero el exchange solo acepta TRC20.

Qué hacer:

1. Abre un ticket de soporte con el exchange.
2. Proporciona el TXID (hash de la transacción).
3. Explica la situación.
4. Espera.

> **El exchange puede devolver tus fondos, pero cobra una comisión por ello.** Generalmente de 10 a 100 USDT.

Y sí:

> **Cuanto antes te comuniques — mayor será la probabilidad.**

### Cuándo la Recuperación es Imposible

Lamentablemente, hay casos en los que no puedes recuperar el dinero:

- lo enviaste a la dirección de otra persona que no controlas;
- la red es tan oscura que nadie puede acceder a ella;
- lo enviaste a un contrato inteligente que no tiene función de reembolso.

Pero estos casos son raros. En el 90% de las situaciones, el dinero se puede recuperar.

---

## Cómo No Meterse Nunca en Esta Situación

### Usa Carteras Multimoneda

Las carteras modernas (Trust Wallet, MetaMask, Coinbase Wallet) soportan múltiples redes. Al enviar USDT, **elige la red que soporte tu destinatario**.

### Verifica Tres Veces

Una regla simple pero efectiva:

1. Revisa la red del remitente.
2. Revisa la red del destinatario.
3. Asegúrate de que coincidan.

### Envía una Transacción de Prueba

Si vas a enviar una cantidad grande (> $100) a una dirección nueva, primero envía **una pequeña transacción de prueba** ($1–5). Espera a que se complete. Si todo está bien — envía el resto.

> **Esta regla cuesta $1–5. Romperla puede costarte $500+.**

---

## Conclusión

Las criptos te dan **libertad**. Pero con esa libertad viene **responsabilidad**.

El error de red es el más común entre los principiantes. También es el más prevenible.

Recuerda la regla de oro:

> **Revisa siempre la red antes de enviar. Un segundo de atención te ahorra horas de estrés y cientos de dólares.**

Y si enviaste a la red equivocada — no te desesperes. En la mayoría de los casos, el dinero se puede recuperar. La clave es actuar rápido y mantener la calma.

---

## FAQ

### ¿Qué pasa si envío USDT en la red equivocada?

La transacción aparecerá como "exitosa", pero el destinatario no verá los fondos. Se pueden recuperar, pero lleva tiempo y generalmente implica una comisión.

### ¿Puedo perder mi USDT para siempre?

En la mayoría de los casos — no. Si lo enviaste a tu propia dirección o a la de un exchange, la recuperación es posible. La pérdida permanente es rara.

### ¿Por qué existen diferentes redes para el mismo token?

Cada [blockchain](/es/glossary/#blockchain) es un sistema independiente. USDT se emite en muchas blockchains para que los usuarios puedan elegir la red con las comisiones y la velocidad que más les convengan.

### ¿Qué red es mejor para USDT?

Para cantidades pequeñas — TRC20 o BSC (comisiones bajas). Para cantidades grandes — ERC20 (alta seguridad, pero cara).

### ¿Cómo saber qué red usar?

Pregunta al destinatario: "¿Qué red usas para recibir?" O revisa su historial de transacciones anterior.

---
weight: 6
title: "Cómo Verificar una Transacción en la Blockchain"
description: "Cómo verificar cualquier transacción cripto usando Etherscan y herramientas similares: qué mirar, cómo leer el estado y las confirmaciones"
category: "practice"
translationKey: "check-transaction"
slug: "como-verificar-transaccion-en-blockchain"
keywords:
  - Etherscan
  - explorador de blockchain
  - verificar transacción
  - estado de transacción
  - TxID
  - seguimiento de wallets
prev: "/es/practice/first-transaction-without-mistakes"
next: "/es/exchanges"
---

## Cómo Verificar una Transacción en la Blockchain: Todo lo Que Necesitas Saber

---

Enviaste algo de cripto. El dinero salió de tu wallet. ¿Pero realmente llegó al destinatario?

En el mundo bancario, solo esperas un SMS o una notificación push. En cripto, las cosas son mucho más transparentes:

> **Cada transacción es un registro público que cualquiera puede verificar.**

Y no necesitas soporte bancario ni acceso a la cuenta de otro. Solo necesitas una herramienta — un **explorador de blockchain**.

En este artículo cubriremos:
- cómo encontrar cualquier transacción por su ID;
- qué significan los estados Éxito, Pendiente y Fallido;
- cómo leer los detalles: bloque, comisión, de dónde a dónde;
- qué exploradores funcionan para diferentes redes;
- cómo configurar el monitoreo de wallets.

---

## ¿Qué Es un Explorador de Blockchain y Para Qué Lo Necesitas?

Un **explorador de blockchain** es como el "Google de la blockchain." Un sitio web público que muestra todo lo que sucede en la red:

- cada transacción;
- cada wallet y su saldo;
- cada bloque y su contenido.

A diferencia de un banco donde solo ves tu propia actividad, en la blockchain **todo es visible**. Los datos solo están codificados en direcciones — sin vínculo con tu identidad.

Necesitas un explorador cuando:

| Situación | Por qué revisarlo |
|-----------|-------------------|
| Enviaste dinero, el destinatario dice "no lo recibí" | Muestra el TxID — prueba de envío |
| Una transacción está atascada | Revisa el estado y el número de confirmaciones |
| Quieres verificar que una dirección sea correcta | Mira el historial y saldo de la wallet |
| Un estafador envió una transferencia falsa | Verifica si la transacción realmente existe en la blockchain |

---

## Etherscan: El Explorador Principal de Ethereum

**Etherscan** ([etherscan.io](https://etherscan.io)) es el explorador de blockchain más popular. Funciona para la red Ethereum y todos los tokens del estándar ERC-20.

### Hash de Transacción (TxID)

Veamos un ejemplo al azar. Encontré una transacción interesante — la usaremos para desglosar todos los detalles:  
`TxID: 0x6f6fd3e8018516ff5e60bfcc2c4fd01be74a877f6b4fac1705651623ad7d70cd`

1. Ve a [etherscan.io](https://etherscan.io).
2. **Pega el TxID** en la barra de búsqueda (centro superior de la página).
3. Presiona Enter.

En menos de un segundo verás todos los detalles de la transacción.

Piénsalo como un "número de recibo." Cópialo y envíalo al destinatario — es la prueba oficial de la transferencia.

### Lo Que Muestra Etherscan

Esto es lo que verás en la página de la transacción:

#### Estado

| Estado | Qué significa |
|--------|---------------|
| ✅ **Éxito** | Transacción ejecutada, fondos acreditados |
| ⏳ **Pendiente** | Esperando — aún no incluida en un bloque |
| ❌ **Fallido** | Error — la transacción no se completó (comisión de gas quemada) |

> **Importante:** Fallido ≠ dinero perdido. Si la transacción falló, los fondos vuelven al remitente (menos la comisión de gas).

#### Bloque

El número de bloque donde se incluyó la transacción.  
Por ejemplo:  
`Block: `**`25093288`**` 22 Block Confirmations`

Cuantos más bloques **confirmados**, más segura es la transacción:

| Red | Confirmaciones mínimas para seguridad |
|-----|---------------------------------------|
| Bitcoin | 3–6 |
| Ethereum | 12–32 |
| Solana | 1 (finalización muy rápida) |

#### De / Para

- **De (From)** — la dirección del remitente.  
`From: 0x56Eddb7aa87536c09CCc2793473599fD21A8b17F (Binance 17)`
- **Para (To)** — la dirección del destinatario (o dirección del contrato).  
`To: 0x42008C6392F552fcFF9abbf310E4421eEd22fAF9`

> \* *Binance 17* — **Etherscan** identificó la dirección de la wallet como perteneciente al exchange Binance. Esta información no está en la blockchain en sí, pero los análisis del sitio hacen esa conexión.

Haz clic en cualquier dirección — verás su historial completo y saldo.

#### Valor

El monto de la transferencia: `0 ETH ($0.00)` porque fue una transferencia de token (ERC-20): `6,000,000.25342 ($5,997,252.25) Tether USD (USDT)`.

#### Comisión de Transacción (Gas Fee)

La comisión pagada por la transacción. Muestra dos números:

- **Transaction Fee** — cuánto gas se usó realmente;  
`Transaction Fee: 0.000063066067464358 ETH ($0.14)`
- **Gas Price** — el precio por unidad de gas (en Gwei);  
`Gas Price: 1.367404598 Gwei (0.000000001367404598 ETH)`

Ahí lo tienes. Enviaste $6,000,000 y pagaste $0.14 en comisiones.

#### Límite de Gas

El gas máximo que estabas dispuesto a pagar y cuánto se usó realmente.  
`Gas Limit & Usage by Txn: 220,436 | 46,121 (20.92%)`

---

## Lista de Exploradores

Cada red blockchain tiene su propio explorador. Estos son los más populares:

### Ethereum (ERC-20)

- **Etherscan** — [etherscan.io](https://etherscan.io) — el explorador principal de Ethereum.
- **Etherscan para testnet Sepolia** — [sepolia.etherscan.io](https://sepolia.etherscan.io) (útil para practicar).

### BNB Chain (BEP-20)

- **BscScan** — [bscscan.com](https://bscscan.com) — el equivalente completo de Etherscan para Binance Smart Chain.  
La interfaz es casi idéntica — mismos estados, bloques, comisiones.

### Solana

- **Solscan** — [solscan.io](https://solscan.io) — el explorador principal de Solana.

Particularidad de Solana: las transacciones se confirman en **milisegundos**. El estado Pendiente aquí prácticamente no existe.

### TRON (TRC-20)

- **Tronscan** — [tronscan.org](https://tronscan.org) — el explorador oficial de la red Tron.  
Popular para USDT — mucha gente usa Tron por sus comisiones bajas.

### Bitcoin

- **Blockchain.com** — [blockchain.com/explorer](https://www.blockchain.com/explorer) — el explorador BTC más conocido.
- **Mempool.space** — [mempool.space](https://mempool.space) — explorador avanzado con visualización de la cola de transacciones (mempool).

### Búsqueda Universal

- Bitcoin y Litecoin — [bitaps.com](https://bitaps.com/) — un explorador alternativo.

---

## Cómo Monitorear una Wallet: Alertas y Notificaciones

No tienes que revisar cada transacción manualmente. Los exploradores pueden notificarte sobre la actividad de una wallet.

### Configuración en Etherscan

1. Regístrate en [etherscan.io](https://etherscan.io) (gratis).
2. Ve a **"Watch List"** → **"Add Address"**.
3. Pega la dirección de la wallet que quieres rastrear.
4. Configura las notificaciones:
   - **Email** — recibe un correo por cada transacción entrante o saliente;
   - **Telegram** — a través del Etherscan Alert Bot.

### Funciones Similares en Otros Exploradores

- **BscScan** — mismo sistema de Watch List, notificaciones por email.
- **Solscan** — haz clic en **"Subscribe"** en la página de la dirección.
- **Tronscan** — el botón **"Follow"** en la página de la wallet.

### Servicios de Monitoreo de Terceros

- **Dextools** ([dextools.io](https://dextools.io)) — rastrea transacciones por token y pool de liquidez.
- **Nansen** ([nansen.ai](https://nansen.ai)) — herramienta profesional de análisis de wallets (de pago).
- **Bots de Telegram** — un montón de bots rastrean "ballenas" y grandes transacciones en tiempo real.

> Consejo: si esperas una transferencia importante, configura una alerta en el explorador. Recibirás la notificación **antes** de que el destinatario diga "llegó."

---

## Cómo Verificar una Transacción en un Exchange (CEX)

Si estás moviendo cripto **desde un exchange** a una wallet externa o viceversa, el proceso es ligeramente diferente:

1. Encuentra el **TxID** en el historial de transacciones del exchange (normalmente en "Historial" → "Depósitos/Retiros").
2. Copia el TxID.
3. Abre el explorador de la red correspondiente y pega el TxID.

> **Importante:** Los exchanges a menudo muestran su propio TxID interno para transferencias dentro de la plataforma. Si enviaste **entre usuarios del mismo exchange** — no hay transacción en la blockchain, es solo una entrada en la base de datos del exchange.

### Cómo Distinguir una Transferencia Interna de una Transacción en Blockchain

| Tipo de transferencia | ¿Tiene TxID? | ¿Se puede verificar en un explorador? |
|-----------------------|--------------|---------------------------------------|
| Dentro del exchange (Usuario A → Usuario B en Binance) | Sí, pero interno | ❌ No |
| Del exchange a wallet externa | Sí, un TxID real | ✅ Sí |
| De wallet al exchange | Sí | ✅ Sí |

---

## Qué Hacer Si una Transacción se Atasca

El estado **Pendiente** puede durar desde unos segundos hasta varios días. Esto es lo que está pasando y lo que puedes hacer.

### Por Qué se Atascan las Transacciones

- **Comisión de gas baja.** En redes como Ethereum, los mineros procesan primero las transacciones con comisiones más altas. Si pusiste el gas demasiado bajo — la transacción se queda en la cola.
- **Congestión de la red.** En momentos de furor (como un lanzamiento popular de NFT), la cola se vuelve enorme.
- **Problemas de nodo.** Raro, pero a veces un validador específico ralentiza las cosas.

### Qué Puedes Hacer

1. **Espera.** Si la red no está críticamente congestionada, la transacción se completará — solo que lentamente.
2. **Acelérala (Replace-by-Fee).** Algunas wallets (MetaMask, Trust Wallet) tienen una opción **"Speed Up"** — reenvías la misma transacción con una comisión más alta.
3. **Cancela.** Si tu wallet soporta **"Cancel"**, puedes reemplazar la transacción atascada con una vacía usando un gas más alto.

> **Si la transacción sigue Pendiente después de 24 horas** — lo más probable es que "se caiga" (nunca entre en un bloque), y los fondos regresarán.

### Cuándo Preocuparse (Spoiler: Casi Nunca)

| Estado | ¿Deberías preocuparte? |
|--------|------------------------|
| Pendiente (hasta 30 min) | No, es normal |
| Pendiente (1–6 horas) | Vale la pena revisar el gas y la red |
| Pendiente (más de 24 horas) | Probablemente no se completará — los fondos volverán |
| Éxito | ✅ La transferencia está completa |
| Fallido | ❌ Fondos devueltos (menos la comisión de gas) |

---

## Lista de Verificación: Qué Revisar Después de Enviar

Cuando hayas enviado cripto, repasa esta lista:

| # | Paso | Qué buscar |
|---|------|------------|
| 1 | Copia el TxID desde tu wallet | Asegúrate de que no sea una cadena vacía |
| 2 | Abre un explorador (Etherscan, etc.) | Pega el TxID en la búsqueda |
| 3 | Revisa el estado | ✅ Éxito = listo |
| 4 | Verifica el monto (Valor) | ¿Coincide con lo que enviaste? |
| 5 | Revisa la dirección del destinatario (To) | ¿Lo enviaste al lugar correcto? |
| 6 | Mira el número de confirmaciones | Cuantas más — más seguro |
| 7 | Envía el TxID al destinatario | Esto es la prueba de la transferencia |

---

## Preguntas Frecuentes

### ¿Puedo verificar una transacción sin un TxID?

Sí, si conoces la **dirección del remitente o del destinatario**. Pega la dirección en la búsqueda del explorador — verás **todas sus transacciones** y podrás encontrar la correcta por monto, fecha o hash.

### ¿Cómo verifico si un estafador envió una transferencia real?

Los estafadores suelen enviar capturas de pantalla o PDFs con "prueba" de una transferencia. La única forma de verificarlo:

1. Pide el TxID.
2. Pégalo en un explorador.
3. Si no hay transacción — es falso.

### ¿Qué son las confirmaciones?

Cada nuevo bloque añadido después del bloque que contiene tu transacción da **+1 confirmación**. Cuantas más confirmaciones, más difícil es revertir la transacción.
- Para cantidades pequeñas: 1–3 confirmaciones son suficientes.
- Para cantidades grandes: 6+ confirmaciones.
- Para Bitcoin, los exchanges suelen esperar 3–6 confirmaciones.

### ¿Por qué se cobró la comisión aunque la transacción falló?

El gas es un pago por **cómputo**, no por éxito. Si una transacción falló (ej., saldo de token insuficiente), el minero igual ejecutó el código y ganó la comisión. Los fondos **vuelven** a tu wallet, pero el gas se quema.

### ¿Puedo cancelar una transacción que ya se envió?

No. Si una transacción está confirmada (Éxito), queda **permanentemente** registrada en la blockchain. Nadie — ni el desarrollador, ni un minero, ni un gobierno — puede deshacerla.

---

## Resumen

Verificar una transacción en la blockchain es un superpoder que las finanzas tradicionales no te dan:

- Puedes ver **cada** operación de forma pública y transparente.
- No necesitas llamar a soporte ni esperar una respuesta.
- El TxID es una prueba legalmente significativa de una transferencia.
- Puedes rastrear cualquier wallet en tiempo real.

Solo recuerda tres cosas:

1. **TxID = número de recibo.** Guárdalo después de cada envío.
2. **Los exploradores son gratuitos.** Etherscan, BscScan, Solscan, Tronscan — cualquiera de ellos al alcance de tu mano.
3. **Estado Éxito = el dinero llegó.** Si el estado es Éxito, nada más importa.

Las cripto te dan **control total y transparencia total**. Verificar una transacción es el primer paso para sentirte seguro en este mundo.

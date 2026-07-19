---
weight: 220
title: "Por qué una transferencia de cripto puede costar $30"
description: "Desglosando las comisiones de transacciones cripto: gas, mempool, tarifa prioritaria y cómo evitar pagar de más"
category: "how-it-works"
translationKey: "why-transaction-costs-30"
slug: "por-que-transferencia-puede-costar-30"
keywords:
  - comisión de gas
  - tarifa de transacción
  - mempool
  - tarifa prioritaria
  - gas de Ethereum
  - comisión de Bitcoin
  - costos cripto
---

## Por qué una transferencia de cripto puede costar $30

---

Abres tu wallet, quieres enviarle 50 USDT a un amigo. Ingresas la dirección, revisas el monto — y ves una comisión de **$29.84**.

No por $5,000. No por $100,000. Por $50.

¿De dónde salen estas cifras? Y más importante aún — **¿por qué la misma operación cuesta $0.03 en otro momento?**

---

## ¿A quién le estamos pagando realmente?

El cripto no es "gratis". Cada transacción requiere que alguien reciba un pago por el trabajo de la red. Dependiendo de la [blockchain](/es/glossary/#blockchain), ese alguien es:

- **Miners** (Bitcoin) — resuelven problemas matemáticos para confirmar [bloques](/es/glossary/#block);
- **Validadores** (Ethereum, Solana) — verifican y confirman transacciones.

Ninguno de los dos lo hace por altruismo. Se ganan una **comisión** por cada transferencia que incluyen en un [bloque](/es/glossary/#block).

> Cuando pagas una comisión, no estás pagando por "enviar dinero" — estás pagando por **un lugar en un bloque**.

Una [blockchain](/es/glossary/#blockchain) es una cadena de bloques, y cada bloque tiene un tamaño limitado. Cuando hay más personas que quieren enviar transacciones que lugares disponibles en un bloque, comienza una subasta.

---

## Cómo funcionan las comisiones en Ethereum: el Gas

Ethereum (y todas las redes EVM) tiene el modelo de comisiones más transparente. Esta es la fórmula:

> **Comisión = límite de gas × precio del gas**

### Límite de Gas

Cada operación en la red requiere poder de cómputo:

- Una transferencia simple de ETH — **21,000 de gas**;
- Una llamada a un contrato inteligente complejo — **100,000 a 500,000+ de gas**.

Piénsalo como combustible: ir a la tienda de la esquina gasta menos gasolina que un viaje por carretera.

### Precio del Gas

El precio del gas es cuánto estás dispuesto a pagar por una unidad de trabajo. Se mide en **gwei** (1 gwei = 0.000000001 ETH).

Y aquí es donde ocurre la magia del mercado.

---

## El Mempool: la batalla por un lugar en el bloque

Cuando envías una transacción, no llega a un bloque de inmediato. Primero va al **mempool** — una sala de espera para transacciones no confirmadas.

Todas las transacciones sin confirmar de toda la red se acumulan en una sola fila.

En cualquier momento, el mempool puede contener:
- 50,000 transacciones en un día tranquilo;
- 200,000+ durante horas pico.

**Los miners y validadores eligen qué transacciones incluir en un bloque.** Y eligen las que pagan las comisiones más altas.

> Quien paga más, sale de la fila más rápido.

---

## La subasta de comisiones

Imagina un minibús lleno de gente en hora pico. Hay 20 asientos, pero 100 personas quieren subir. El conductor acepta a quien pague más.

La blockchain funciona igual.

Bitcoin usa un **tamaño de bloque fijo** (1–4 MB). Ethereum tiene un límite de gas objetivo (30 millones de gas). Los bloques de Solana también son limitados, pero su arquitectura puede manejar muchas más transacciones por segundo.

Cuando la red está congestionada:

1. Envías una transacción con una comisión "normal";
2. Llega al mempool, pero los lugares del siguiente bloque ya están ocupados por transacciones que pagan más;
3. Después de 5–10 bloques, tu comisión sigue siendo demasiado baja;
4. Se queda esperando horas — o incluso días — hasta que los precios del gas bajen o alguien la cancele.

En Ethereum (EIP-1559), se ve así:

- **Tarifa base** — se quema, se calcula automáticamente según la congestión de la red;
- **Tarifa prioritaria** (propina para el validador) — lo que agregas adicional para que te tomen más rápido.

> Podrías fijar tu comisión en **solo $2**, pero si la tarifa base ya es de $28, tu total será de $30.

---

## Lo que realmente cuestan las transferencias en distintas redes

Estos son rangos aproximados de comisiones para una transferencia simple (al momento de escribir esto):

| Red          | Comisión normal | Horas pico    |
|--------------|----------------|---------------|
| Bitcoin      | $1–$5          | $10–$50+      |
| Ethereum     | $2–$10         | $30–$100+     |
| Solana       | $0.01–$0.05    | $0.10–$0.50   |
| TRON (USDT)  | $1–$3          | $5–$15        |
| BNB Chain    | $0.05–$0.20    | $0.50–$2      |
| Litecoin     | $0.01–$0.10    | $0.30–$1      |

¿Ves la diferencia? Enviar USDT en la red ERC-20 (Ethereum) puede costar $30, mientras que el mismo monto en TRC-20 (TRON) cuesta $1.

> **No es la criptomoneda la que determina el costo de la transferencia — es la red en la que opera.**

---

## Por qué $30 está bien (a veces)

Cuando estás enviando **$50,000**, una comisión de $30 equivale a **0.06%**. Es más barato que cualquier transferencia bancaria (SWIFT: $20–$50 + comisiones de conversión + cargos ocultos).

El detalle es que la comisión **no escala con el monto de la transferencia**. Pagas por complejidad computacional y por un lugar en el bloque, no por la cantidad de ceros en la pantalla.

Entonces:

- Enviar $50,000 → $30 de comisión es **genial**;
- Enviar $50 → $30 de comisión es **un sinsentido**.

---

## Cómo no pagar de más

Aquí tienes algunas reglas simples:

### 1. Revisa la congestión de la red antes de enviar

Sitios como [Etherscan Gas Tracker](https://etherscan.io/gastracker) o [mempool.space](https://mempool.space) muestran las comisiones actuales. Si el gas está alto — **espera**.

Las comisiones suelen bajar 2 o 3 veces durante la noche o los fines de semana.

### 2. Elige la red correcta

El mismo USDT se puede enviar a través de:

- **ERC-20** (Ethereum) — cara pero ampliamente aceptada;
- **TRC-20** (TRON) — barata y rápida;
- **BEP-20** (BNB Chain) — casi gratis;
- **Solana** — centavos.

👉 Solo asegúrate de que **el destinatario soporte esa red**.

### 3. Ajusta las comisiones manualmente

Las wallets avanzadas (ej. MetaMask) te permiten elegir un modo:

- **Lento** — más barato pero más lento;
- **Mercado** — velocidad promedio;
- **Rápido** — instantáneo pero costoso.

"Lento" suele retrasarse solo 1–2 bloques (2–5 minutos), mientras te ahorra entre un 30 y 50%.

### 4. Usa redes de Capa 2

En Ethereum:

- **Arbitrum** — $0.10–$0.50 de comisión;
- **Optimism** — $0.10–$0.50;
- **Base** — $0.05–$0.20;
- **zkSync** — $0.05–$0.30.

El mismo dinero, los mismos contratos inteligentes — pero comisiones 50 a 100 veces más bajas.

### 5. No envíes montos pequeños en horas pico

Si el mempool está saturado (ej. durante un lanzamiento popular de [NFT](/es/glossary/#nft) o una oleada de memecoins), solo espera unas horas.

---

## Una historia real

Una vez le envié $200 en USDT a un amigo por su cumpleaños a través de la red Ethereum. Era viernes por la noche — horario estelar para la actividad cripto.

Configuré la comisión estándar: $3.

Pasó una hora — la transacción seguía pendiente. Dos horas — todavía pendiente. Empecé a ponerme nervioso, mi amigo me escribe: "¿Dónde está el dinero?"

Reviso Etherscan — el mempool está atascado, la tarifa base se ha triplicado en los últimos 30 minutos. Mi transacción está en el último lugar de la fila.

Tuve que hacer un **replace-by-fee** — reenviar la misma transacción con una comisión de $18. Se confirmó en 2 minutos.

Total final: $200 enviados, $18 perdidos en comisiones. **El 9% del monto.**

Si solo hubiera esperado hasta el sábado por la mañana — habría pagado $4.

---

## Resumen

Las comisiones cripto son el pago por **un lugar en un espacio de bloque limitado**, no por la transferencia en sí.

- En Ethereum, la comisión se compone de gas, tarifa base y tarifa prioritaria;
- En Bitcoin, depende del tamaño de la transacción en bytes y de la congestión del mempool;
- En Solana, las comisiones son significativamente más bajas debido a una arquitectura diferente.

**Conclusiones clave:**

- $30 por una transferencia es mucho para $50, pero calderilla para $50,000;
- La comisión no depende del monto — depende de la congestión de la red;
- Puedes controlar la comisión: elige tu red, el momento y el nivel de tarifa;
- Las redes de Capa 2 resuelven el problema: la misma seguridad que Ethereum, pero con comisiones de $0.10.

El cripto te da libertad — pero tendrás que aprender cómo funcionan las comisiones. Igual que en la vida real.

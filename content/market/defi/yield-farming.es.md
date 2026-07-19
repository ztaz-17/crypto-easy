---
weight: 140
title: "Yield Farming: Cómo ganar en DeFi"
description: "Yield farming en DeFi: cómo funciona, de dónde vienen las ganancias, los riesgos y si los principiantes deberían probarlo"
category: "defi"
translationKey: "yield-farming"
slug: "yield-farming"
keywords:
  - yield farming
  - rentabilidad DeFi
  - minería de liquidez
  - APY
  - pérdida impermanente
  - riesgos del farming
---

## Yield Farming: Cómo ganar en DeFi

---

Seguro que has visto los anuncios: "¡1000% APY!", "¡Gana cripto sin esfuerzo!", "¡[DeFi](/es/glossary/#defi) es el nuevo petróleo!"

Suena demasiado bueno para ser verdad. Pero detrás de esos números hay un mecanismo real — **Yield Farming**. Y sí, hay gente que de verdad gana dinero.

Pero ojo: cuanto más alto es el rendimiento, mayor es el riesgo.

En este artículo vamos a ver:

> - qué es el yield farming y cómo funciona;
> - de dónde salen esas tasas de interés tan locas;
> - qué riesgos debes conocer antes de meter tu primer dólar.

---

## ¿Qué es Yield Farming?

**Yield Farming** (también llamado **[minería](/es/glossary/#mining) de [liquidez](/es/glossary/#liquidity)**) consiste en prestar tus criptoactivos a pools de liquidez en protocolos descentralizados ([DEX](/es/glossary/#dex), plataformas de préstamo) a cambio de recompensas.

En términos simples:

> le das tus tokens a un protocolo como "alquiler" y él te paga intereses.

Las ganancias se miden en **APY** (Rendimiento Porcentual Anual) — la tasa de interés anual con capitalización incluida. Cuanto más alto es el APY, más puedes ganar potencialmente.

---

## Cómo funciona

### 1. Eliges un protocolo

Por ejemplo, **Uniswap**, **Curve**, **Aave**, **Compound** o **PancakeSwap**. Cada uno ofrece pools para distintos pares de [tokens](/es/glossary/#token).

### 2. Depositas liquidez

Supongamos que hay un pool de ETH/USDT. Necesitas depositar **un valor igual de ambos tokens** (50% ETH, 50% USDT). A cambio recibes **LP tokens** (tokens de proveedor de liquidez) — tu recibo por una parte del pool.

### 3. El protocolo te paga

Tus ganancias vienen de dos fuentes:

- **comisiones del protocolo** — cada intercambio en el pool cobra una comisión (normalmente 0.1–0.3%), que se reparte entre todos los proveedores de liquidez;
- **tokens de gobernanza** — muchos protocolos también reparten sus tokens nativos (CRV, UNI, CAKE) como bonus.

### 4. Retiras tu ganancia

Los LP tokens se pueden canjear para recuperar tus activos originales más las comisiones que hayas ganado.

---

## ¿De dónde sale el 1000% APY?

Aquí la cosa se pone interesante. Ese rendimiento **no sale de la nada**.

Se compone de tres elementos:

| Componente | Descripción |
|---|---|
| Comisiones del pool | Comisiones reales de trading cobradas a los traders |
| Tokens de recompensa | El protocolo imprime sus propios tokens y se los da a los proveedores de liquidez |
| [Inflación](/es/glossary/#inflation) | Cuantos más tokens se emiten, más alto es el APY (pero el precio del token puede bajar) |

> **Importante:** El APY alto suele estar impulsado por emisiones agresivas de tokens. Si el precio del token cae más rápido de lo que ganas, sigues estando en números rojos.

---

## Tipos de Yield Farming

### Clásico (Minería de Liquidez)

Depositas un par de tokens en un pool DEX (Uniswap, PancakeSwap) y ganas comisiones más tokens del protocolo.

### Préstamos

Prestas activos a través de Aave o Compound y ganas intereses. Menos riesgoso, pero los rendimientos son más bajos.

### Farming Apalancado

Pides un préstamo dentro de un protocolo y lo depositas en otro pool. Esto multiplica tanto la ganancia como el riesgo. **No para principiantes.**

### Auto-Farming (Agregadores de Rendimiento)

Servicios como Yearn Finance buscan automáticamente los mejores rendimientos y mueven tus fondos. Tú solo depositas — ellos hacen el resto.

---

## Riesgos del Yield Farming

### 1. Pérdida Impermanente

Este es el riesgo más común y más traicionero.

Cuando el precio de un token en un pool cambia en relación al otro, pierdes parte de tu capital comparado con simplemente mantener los tokens.

> Ejemplo: depositas 1 ETH ($2000) + 2000 USDT. ETH sube a $3000. Si solo hubieras mantenido el ETH, tendrías $5000. Pero si retiras del pool, tendrás ~$4800. Esos $200 de diferencia son la **pérdida impermanente**.

¿Por qué se llama "impermanente"? Porque si el precio vuelve, la pérdida desaparece. Pero si retiras mientras el precio sigue desviado, la pérdida se vuelve real.

**Cuándo es especialmente peligrosa la IL:**

- alta volatilidad;
- un pool que combina una [stablecoin](/es/glossary/#stablecoin) con un activo volátil;
- mantener la posición durante mucho tiempo.

### 2. Rug Pull

Los desarrolladores crean un pool, atraen usuarios con rendimientos altísimos, luego retiran la liquidez — y todo desaparece. No queda nada de dinero.

**Cómo protegerte:**

- revisa el código del smart contract;
- verifica si tiene una auditoría;
- no te metas en proyectos nuevos que prometen 10,000% APY.

### 3. Bugs en Smart Contracts

Incluso los protocolos auditados pueden tener fallos. Ejemplos: el hack de Nomad Bridge ($190M), incidentes con Cream Finance.

### 4. Caída del Precio del Token

Te pagan en los tokens nativos del protocolo. Si su precio se desploma un 90%, tu rendimiento real podría ser negativo.

### 5. Comisiones de Gas Altas (en Ethereum)

En Ethereum, cada operación (depositar, retirar, reinvertir) cuesta gas. Con farming activo, las comisiones pueden comerse todas tus ganancias.

---

## Comparativa de rendimientos y riesgos

| Tipo de Farming | APY | Riesgo | Complejidad |
|---|---|---|---|
| Stablecoins | 2–10% | Muy bajo | Baja |
| Préstamos (Aave, Compound) | 5–30% | Bajo | Baja |
| Pools DEX con pares fuertes (ETH/USDC) | 10–80% | Medio (IL) | Media |
| Nuevos tokens con APY alto | 100–1000+% | Muy alto | Alta |
| Farming apalancado | 200–2000+% | Extremo | Extrema |

---

## Estrategias para principiantes

Empieza con las opciones más simples y seguras:

1. **Prestar stablecoins** (USDC/USDT/DAI en Aave o Compound) — un 3–8% estable al año sin pérdida impermanente.
2. **Pool LP de stablecoins** (Curve 3pool) — 5–15% con IL mínima.
3. **Auto-farming** (Yearn Finance) — depositas tus fondos y todo se automatiza.

**Lo que NO debes hacer:**

- meterte en un pool con un token que no entiendes;
- perseguir APY por encima del 500%;
- pedir préstamos para farmear cuando estás empezando;
- invertir dinero que no puedas permitirte perder.

---

## Cómo elegir un pool

Una lista de verificación antes de depositar:

- [ ] ¿El protocolo tiene auditoría? (de CertiK, Trail of Bits, OpenZeppelin)
- [ ] ¿Cuánto tiempo lleva el proyecto funcionando?
- [ ] ¿Cuánta liquidez hay en el pool? ([TVL](/es/glossary/#tvl) — valor total bloqueado)
- [ ] ¿Cuál es el volumen de trading?
- [ ] ¿Quién está en el equipo del proyecto? ¿Hay información sobre ellos?
- [ ] ¿Qué parte del APY viene de tokens de recompensa vs comisiones reales?

---

## Conclusión

El Yield Farming es una forma real de ganar en DeFi. Te da acceso a rendimientos que no puedes obtener en las finanzas tradicionales. Pero no va a convertir $100 en $1000 en un mes sin riesgo.

> Cuanto más alto es el rendimiento prometido, mayor es la probabilidad de perder tu capital.

El farming exitoso no es cuestión de codicia. Se trata de:

- entender los mecanismos;
- diversificar;
- hacer cálculos fríos y precisos;
- estar preparado para perder lo que inviertes.

---

## FAQ

### ¿Cuánto se puede ganar con yield farming?
Depende de tu capital, estrategia y las condiciones del mercado. Ganancias conservadoras: 5–15% anual en stablecoins. Estrategias agresivas: 50% hasta ilimitado (con el riesgo correspondiente).

### ¿Qué es la pérdida impermanente en términos simples?
Es la ganancia no realizada cuando un token en un pool sube (o baja) bruscamente de precio. Ganas menos que si simplemente hubieras mantenido el activo.

### ¿El yield farming es ingreso pasivo?
Más o menos. Requiere monitorear tus posiciones, rastrear comisiones y reinvertir. Un enfoque de "configurar y olvidar" solo funciona con agregadores como Yearn Finance.

### ¿Qué pasa con los impuestos en yield farming?
En la mayoría de los países, cada operación (depósito, cobro de recompensas, retiro) es un evento imponible. Se recomienda rastrear todo con herramientas como Koinly, CoinTracker o Accointing.

### ¿Por dónde debería empezar un principiante?
Abre Aave o Compound, deposita USDC al 4–8% APY. Entiende los mecanismos. Solo después pásate a los pools DEX.

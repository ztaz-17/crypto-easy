---
weight: 130
title: "Préstamos Sin Banco: Cómo Funciona el Crédito DeFi"
description: "Cómo funcionan los préstamos cripto sin banco a través de DeFi: garantía, liquidación, riesgos. Aave, Compound"
category: "defi"
translationKey: "crypto-loans"
slug: "prestamos-sin-banco-defi"
keywords:
  - préstamos DeFi
  - crédito cripto
  - Aave
  - Compound
  - garantía
  - liquidación
  - sobregarantía
---

## Préstamos DeFi: Cómo Pedir Prestado Sin Banco Ni Historial Crediticio

---

Imagina esto: necesitas dinero urgente, pero el banco te rechaza por mal historial crediticio. O quizás quieres pedir un préstamo pero no te apetece pasar por [KYC](/es/glossary/#kyc) ni llenar formularios interminables.

En [DeFi](/es/glossary/#defi), eso no es un problema.

> **Un préstamo cripto** es dinero que pides prestado dejando tus criptos como garantía — sin que nadie pregunte por tu historial crediticio.

Nada de comprobantes de ingresos, llamadas del banco ni esperas de aprobación. El código lo maneja todo.

En este artículo veremos:

> - cómo funcionan los préstamos DeFi;
> - por qué tienes que poner más garantía de la que pides prestada;
> - qué es la liquidación y cómo evitarla;
> - los principales riesgos;
> - ejemplos reales: Aave, Compound, MakerDAO.

---

## Cómo Funciona un Préstamo DeFi

En el mundo tradicional, obtener un préstamo funciona así:

- demuestras al banco que puedes pagar el dinero;
- el banco revisa tu historial crediticio y tus ingresos;
- si todo está en orden — te dan el efectivo.

[DeFi](/es/glossary/#defi) funciona de una forma completamente distinta:

> **no demuestras que eres solvente — depositas una garantía.**

El proceso es simple:

1. Depositas cripto (por ejemplo, ETH) en un contrato inteligente;
2. El contrato inteligente te permite pedir prestada otra [criptomoneda](/es/glossary/#cryptocurrency) (como USDC);
3. Usas los fondos prestados;
4. Cuando devuelves el préstamo más los intereses — tu garantía se libera.

> La diferencia clave: **el préstamo no lo concede una persona ni una empresa, sino el código.**

Nadie pregunta dónde trabajas ni cuánto ganas. Solo conecta tu [cartera](/es/glossary/#wallet) y deposita la garantía.

---

## Sobregarantía: Por Qué Necesitas Poner Más de lo que Pides Prestado

En DeFi no hay cobradores ni tribunales. Si un prestatario no paga, un contrato inteligente no puede llevarlo a juicio.

Por eso el sistema funciona de otra manera:

> **la garantía debe valer más que el monto del préstamo.**

Esto se llama **sobregarantía** (overcollateralization).

Así se ve en la práctica:

- quieres pedir prestado $1,000 en USDC;
- el protocolo exige al menos $1,500 de garantía (150%);
- depositas $1,500 en ETH;
- recibes $1,000.

¿Por qué exactamente 150%? Es un colchón contra la volatilidad. Si ETH cae un 30%, todavía queda suficiente garantía para cubrir el préstamo.

### Niveles Típicos

| Protocolo  | Préstamo máximo (LTV)         | Ejemplo                            |
|------------|-------------------------------|-------------------------------------|
| Aave       | 50–75% de la garantía        | Con $100 ETH puedes pedir $50–75  |
| Compound   | 50–75%                        | Similar                            |
| MakerDAO   | 66% (150% sobregarantía)     | Con $100 ETH puedes crear ~$66 DAI |

Cuanto más volátil es el activo — menor es el LTV (loan-to-value, relación préstamo-valor), es decir, menos puedes pedir prestado contra él.

---

## Liquidación: Cuando tu Garantía Pierde Valor

Lo más importante que debes saber sobre los préstamos DeFi:

> **si el precio de tu garantía cae demasiado — la pierdes.**

Esto se llama **liquidación**.

### Cómo Funciona

Digamos que depositaste $1,500 en ETH y pediste prestado $1,000 USDC. Tu factor de salud es 1.5.

Si el precio de ETH baja:

- $1,500 → $1,300 — todavía seguro;
- $1,300 → $1,100 — el factor de salud está bajando;
- $1,100 → $1,050 — umbral crítico.

En cuanto el factor de salud llega a 1 (o menos, según el protocolo), se activa una **liquidación automática**:

> el contrato inteligente vende parte de tu garantía para cubrir la deuda.

Se añade una **penalización** al monto liquidado — normalmente del 5–15%. Es la comisión de riesgo que se paga a los liquidadores (generalmente bots que monitorean las posiciones).

### Cómo Evitar la Liquidación

1. **No pidas el máximo.** Si puedes pedir $75 por cada $100 — pide $40–50. Cuanto menor la deuda, mayor tu margen de seguridad.
2. **Vigila el precio.** En días volátiles, revisa tu factor de salud cada pocas horas.
3. **Añade más garantía.** Si ETH baja — agrega más ETH (o [stablecoins](/es/glossary/#stablecoin)) para subir tu factor de salud.
4. **Usa alertas.** Hay servicios que te notifican cuando tu factor de salud está bajo (por ejemplo, DeBank o las notificaciones integradas de Aave).

---

## Ejemplos de Protocolos

### Aave

**[Aave](https://aave.com)** — el protocolo de préstamos DeFi más grande.

Lo destacado:

- puedes pedir prestado contra más de 20 activos (ETH, USDC, DAI, WBTC, MATIC y otros);
- las tasas de interés pueden ser **estables** (stable rate) o **variables** (variable rate);
- los **préstamos flash** están disponibles — préstamos instantáneos sin garantía (pero deben devolverse en la misma transacción);
- la salud de tu posición se muestra como un factor de salud: >1 significa que está bien, =1 significa liquidación.

### Compound

**[Compound](https://compound.finance)** — uno de los primeros protocolos DeFi, lanzado en 2018.

Lo destacado:

- funciona de forma similar a Aave, pero sin tasas estables;
- utiliza tasas de interés ajustadas algorítmicamente;
- se integra con muchas [carteras](/es/glossary/#wallet) y servicios.

### MakerDAO

**[MakerDAO](https://makerdao.com)** — un modelo ligeramente diferente.

Aquí no solo tomas un préstamo — **creas la stablecoin DAI** bloqueando ETH (u otros activos) como garantía. Es básicamente lo mismo que un préstamo: bloqueas ETH, obtienes DAI, y cuando devuelves el DAI más los intereses — tu garantía se libera.

> MakerDAO es la columna vertebral de todo el ecosistema DeFi. Cientos de protocolos usan DAI.

---

## Préstamo DeFi vs. Préstamo Bancario: Comparativa

| Criterio              | Préstamo Bancario                      | Préstamo DeFi                             |
|-----------------------|----------------------------------------|-------------------------------------------|
| Historial crediticio  | Obligatorio                            | No es necesario                           |
| Tiempo de aprobación  | Días a semanas                         | Segundos                                  |
| Garantía              | Generalmente no necesaria (préstamos personales) | Obligatoria (150%+ del monto del préstamo) |
| Interés               | 5–30% TAE (según crédito)             | 1–15% TAE (según oferta y demanda)        |
| Acceso                | Pasaporte, [KYC](/es/glossary/#kyc), +18                    | Conexión a internet, cualquier edad       |
| Liquidación           | Tribunal, embargos, impagos            | Automática, gestionada por bots           |
| Geografía             | Solo el país del banco                 | Global                                    |
| Horario               | Horario laboral                        | 24/7, sin días festivos                   |

> La diferencia principal: un banco confía en ti por tu pasado. DeFi confía en ti por tu garantía actual.

---

## Riesgos de los Préstamos DeFi

Los préstamos DeFi no son solo libertad — también conllevan riesgos serios.

### 1. Volatilidad y Liquidación

Las [criptomonedas](/es/glossary/#cryptocurrency) son de los activos más volátiles del mundo. ETH puede caer un 20–30% en un solo día. Si tu factor de salud ya estaba bajo — la liquidación es inevitable.

> Recomendación: mantén tu factor de salud por encima de 1.5–2.0 en días tranquilos y de 2.5–3.0 en días volátiles.

### 2. Errores en Contratos Inteligentes

Los protocolos DeFi son software. El software tiene errores. Si un hacker encuentra una vulnerabilidad en el contrato inteligente de Aave o Compound — todos los depósitos de los usuarios podrían ser robados.

> Ejemplo: el hack de Cream Finance (2021) — $130 millones. Ni los protocolos grandes y auditados son inmunes.

### 3. Problemas con los Oráculos

Los oráculos son servicios que proporcionan datos de precios a los contratos inteligentes (Chainlink, por ejemplo). Si un oráculo reporta un precio incorrecto — la liquidación puede ocurrir por error.

> En 2022 hubo un incidente con el protocolo Mango Markets donde la manipulación de oráculos permitió a atacantes drenar $114 millones del protocolo.

### 4. Incapacidad de Devolver el Préstamo

Si pierdes el acceso a tu cartera o simplemente no tienes fondos para devolver el préstamo — tu garantía se liquida. Nadie puede ayudarte, y no hay un banco que restaure tu acceso.

### 5. Activos de Garantía «Basura»

Algunos protocolos permiten depositar [tokens](/es/glossary/#token) oscuros con baja [liquidez](/es/glossary/#liquidity) como garantía. Una caída brusca de ese activo puede liquidar toda tu posición en cuestión de minutos.

> Usa solo activos confiables con alta liquidez (ETH, WBTC, USDC, DAI).

---

## Cuándo Tiene Sentido un Préstamo DeFi

Un préstamo DeFi no es para comprar un coche o una casa. Es una herramienta para:

- **obtener [liquidez](/es/glossary/#liquidity)** sin vender tus activos (no quieres vender ETH pero necesitas USDC);
- **arbitraje y trading** (pedir prestado a una tasa baja, invertir en un pool de alto rendimiento);
- **apalancamiento** (aumentar tu posición sin vender tus tenencias);
- **préstamos flash** (estrategias complejas ejecutadas en una sola transacción).

> Si necesitas una hipoteca o un préstamo personal — DeFi no te servirá. Pero si tienes ETH y quieres obtener USDC sin pagar impuestos sobre ganancias de capital — es perfecto.

---

## Resumen

Los préstamos DeFi son una revolución en las finanzas:

| Ventajas                           | Desventajas                              |
|------------------------------------|------------------------------------------|
| Aprobación instantánea             | Riesgo de liquidación en caída del mercado |
| Sin historial crediticio           | Riesgo de errores en contratos inteligentes |
| Accesible desde cualquier parte del mundo | Requiere monitoreo activo de la posición  |
| Transparencia (todo en cadena)     | Volatilidad de las criptomonedas         |
| Tasas de interés a menudo más bajas que los bancos | Pérdida de la garantía durante la liquidación |

> Un préstamo DeFi no es dinero gratis. Es una herramienta que te da libertad — pero exige responsabilidad.

Si decides probarlo:

1. Empieza con poco — $50–100;
2. Usa un protocolo probado (Aave, Compound);
3. Mantén tu factor de salud por encima de 2.0;
4. Mantente alerta — vigila el mercado.

---

## Preguntas Frecuentes

### ¿Puedo obtener un préstamo DeFi sin garantía?

Generalmente no. Los préstamos DeFi requieren sobregarantía. La excepción son los **préstamos flash** (flash loans), pero deben devolverse en la misma transacción. Para el usuario promedio, los préstamos flash no son muy prácticos.

### ¿Cuáles son las tasas de interés de los préstamos DeFi?

Depende de la oferta y la demanda. En Aave, las tasas de USDC pueden ser del 2–10% TAE. En periodos de alta demanda — hasta el 20–30%.

### ¿Qué pasa si no devuelvo el préstamo?

Nadie te llamará ni te amenazará. El contrato inteligente simplemente liquidará tu garantía, cubrirá la deuda y enviará los fondos sobrantes de vuelta a tu cartera. Pero perderás la penalización por liquidación (normalmente del 5–15%).

### ¿Cómo sé si mi posición está cerca de la liquidación?

Tanto Aave como Compound tienen un indicador de **factor de salud**. Mientras esté por encima de 1 — tu posición está segura. Cuando se acerca a 1 — es momento de añadir más garantía o devolver parte de la deuda.

### ¿Qué criptos puedo usar como garantía?

ETH, WBTC, USDC, DAI, MATIC, LINK y muchas otras. Cuanto más líquido es el activo, mayor es el LTV (más puedes pedir prestado contra él).

### ¿Tengo que pagar impuestos por un préstamo DeFi?

En la mayoría de los países — no, porque un préstamo no se considera ingreso. Sin embargo, si tu garantía se liquida, eso puede tratarse como un evento imponible (una venta del activo). Consulta con un asesor fiscal local.

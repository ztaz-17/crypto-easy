---
weight: 155
title: "Contratos Inteligentes: Qué Son y Cómo Funcionan"
description: "Contratos inteligentes explicados de forma sencilla: qué son, dónde se usan, cómo funcionan en Ethereum y cuáles son los riesgos"
category: "basis"
translationKey: "what-are-smart-contracts"
slug: "que-son-los-contratos-inteligentes"
keywords:
  - smart contracts
  - contratos inteligentes
  - Ethereum
  - DeFi
  - dApps
  - aplicaciones descentralizadas
  - programación blockchain
  - Solidity
  - cripto para principiantes
---

## ¿Qué es un contrato inteligente?

Un contrato inteligente (smart contract) es un programa que vive en la blockchain y funciona **automáticamente**, sin intervención humana. Tú estableces las reglas — y se ejecutan sin jueces, abogados ni intermediarios.

Imagina una máquina expendedora. Metes una moneda, presionas un botón — recibes un refresco. Nadie verifica tu identidad, nadie firma un contrato. La máquina simplemente ejecuta su programa.

Un contrato inteligente funciona igual — pero en lugar de refrescos, maneja dinero, tokens y activos digitales.

> **En resumen:** un contrato normal = papel + firma + juzgado.  
> Un contrato inteligente = código + blockchain + ejecución automática.

## Cómo funciona un contrato inteligente — ejemplo sencillo

Digamos que quieres apostar $100 con un amigo a que mañana llueve.

**La forma habitual:**  
Se lo dicen verbalmente. Mañana alguien pierde pero «se olvida» de pagar. Vas a juicio — lleva meses. Al final gastas más en abogados de lo que ganaste.

**Con un contrato inteligente:**  
1. Ambos envían $100 a la dirección del contrato inteligente.
2. Mañana el contrato consulta los datos meteorológicos (a través de un **oráculo** — un mecanismo que trae datos del mundo real a la blockchain).
3. Si llovió — el contrato envía los $200 completos a quien apostó por la lluvia. Si no — al otro.
4. Nadie puede «cambiar de opinión» ni negarse a pagar. El código se ejecuta automáticamente.

Este es un ejemplo simplificado, pero la idea es la misma: **los contratos inteligentes reemplazan la confianza con código**.

## ¿Dónde se usan los contratos inteligentes?

Los contratos inteligentes son la base de toda la industria cripto más allá de las transferencias simples. Aquí es donde realmente funcionan:

### DeFi (Finanzas Descentralizadas)

El uso más extendido. Los protocolos DeFi son conjuntos de contratos inteligentes que reemplazan a los bancos:

- **Intercambio de divisas** — intercambias USDT por ETH en Uniswap sin intermediario. El contrato encuentra la tasa y ejecuta la operación.
- **Préstamos** — envías ETH como garantía, el contrato te presta USDC. Si la garantía baja de precio — el contrato la vende automáticamente (liquidación).
- **Yield farming** — bloqueas tokens en un pool de liquidez, el contrato acumula intereses cada segundo.

En las finanzas tradicionales, todo esto lo manejan personas: gerentes, cajeros, abogados. En DeFi — contratos inteligentes.

### NFTs (Tokens No Fungibles)

Cada NFT es un registro en un contrato inteligente. Cuando compras un NFT, el contrato:
1. Verifica que tienes fondos suficientes
2. Transfiere el pago al vendedor
3. Te registra como nuevo propietario
4. Paga regalías al creador (un porcentaje de la reventa)

### DAOs (Organizaciones Autónomas Descentralizadas)

Los contratos inteligentes gestionan el tesoro de la organización sin un CEO. Los miembros votan con tokens y el contrato ejecuta automáticamente la decisión:

- «Se votó asignar 10 000 USDT para marketing» → el contrato envía los fondos
- «Se votó cambiar la tasa de interés» → el contrato ajusta los parámetros del protocolo

### Tokens

Cuando creas un nuevo token (USDT, UNI, SHIB o cualquier otro), no es magia — es un contrato inteligente que sigue el estándar ERC-20 (en Ethereum) o BEP-20 (en BSC). El contrato almacena los saldos de todos los titulares y autoriza las transferencias.

> Dato: el contrato inteligente más popular es USDT Tether. Procesa miles de millones de dólares cada día.

## Contratos inteligentes en Ethereum

Ethereum fue la primera plataforma en popularizar los contratos inteligentes. Bitcoin solo permite enviar monedas. Ethereum permite programar cualquier regla.

**La idea clave de Ethereum:** no solo «Alicia envió 5 ETH a Bob», sino «SI se cumple la condición, ENTONCES ejecuta la acción».

Los contratos inteligentes de Ethereum se escriben en **Solidity**, un lenguaje similar a JavaScript pero que funciona en la blockchain. Cualquiera puede leer el código del contrato — todos los contratos inteligentes son de código abierto por defecto.

### Gas: por qué cada operación cuesta dinero

Cada acción de un contrato inteligente requiere recursos computacionales. Todas las computadoras de la red (nodos) deben ejecutar el código y verificar el resultado. Pagas por esto con **gas** — una tarifa en ETH.

Una operación compleja (como un swap en Uniswap) cuesta más que una simple (enviar ETH). Cuanta más gente usa la red, más alto es el gas.

## Ventajas de los contratos inteligentes

**Transparencia** — el código del contrato es visible para todos. Puedes verificar qué pasará con tu dinero antes de enviarlo.

**Inmutabilidad** — una vez publicado en la blockchain, el contrato no se puede modificar. Nadie puede añadir reglas retroactivamente.

**Sin intermediarios** — no se necesitan bancos, abogados ni notarios. El contrato ejecuta las condiciones por sí mismo.

**Disponibilidad 24/7** — el contrato funciona las 24 horas, sin fines de semana ni descansos. Nadie puede decir «vuelva mañana» o «el cajero se fue a almorzar».

**Automatización** — pagos, acumulación de intereses, distribución de ingresos — todo puede funcionar automáticamente.

## Riesgos de los contratos inteligentes

Los contratos inteligentes no son perfectos. Estos son los principales riesgos:

### Errores en el código

Los humanos escriben código — los humanos se equivocan. Si un contrato tiene un error, un hacker puede explotarlo.

**Ejemplo:** el hackeo de The DAO en 2016. Un hacker encontró una vulnerabilidad en el código y drenó 3.6 millones de ETH (~$50 millones en ese momento). Esto obligó a Ethereum a hacer un hard fork — dividiéndose en Ethereum y Ethereum Classic.

Hay miles de casos así. Cada mes se hackean protocolos por millones de dólares — casi siempre debido a errores en contratos inteligentes.

### Inmutabilidad — un arma de doble filo

Si cometiste un error en el contrato, no puedes simplemente «pedir que lo arreglen». El contrato vive su propia vida. Por eso los contratos pasan por **auditorías** — revisiones de código por expertos en seguridad — antes del lanzamiento.

### Oráculos — el eslabón débil

Un contrato inteligente no puede consultar el precio de Bitcoin o el clima por sí solo. Estos datos provienen de **oráculos** — servicios externos. Si un oráculo envía datos incorrectos (o es hackeado), el contrato ejecuta condiciones basadas en información falsa.

### Frontrunning

Cuando envías una transacción de un contrato inteligente, entra al mempool (la cola de transacciones no confirmadas). Los bots pueden detectarla, pagar más gas y ejecutar su propia transacción antes que la tuya. Esto se llama frontrunning — y es legal.

## Cómo verificar un contrato inteligente antes de usarlo

1. **Busca una auditoría** — los protocolos confiables publican auditorías de firmas como Trail of Bits, OpenZeppelin o Certik. ¿Sin auditoría? No envíes dinero.
2. **Verifica la antigüedad del contrato** — si un contrato tiene un mes, millones en TVL y no tiene auditoría — es una bandera roja.
3. **Lee el código** — si puedes, revisa el código en Etherscan. Si no, quédate con proyectos que la comunidad respalda.
4. **Revisa los permisos** — cuando firmas una transacción con un contrato inteligente, a menudo le das permiso para gastar tus tokens. Usa [permisos de tokens](/es/security/permisos-de-tokens-que-son/) — revoca los permisos de los contratos que ya no uses.

## El futuro de los contratos inteligentes

Los contratos inteligentes no son solo un truco cripto. Son una nueva forma de acuerdo digital que está entrando gradualmente al mundo real:

- **Seguros** — un contrato paga automáticamente una compensación cuando tu vuelo se retrasa.
- **Bienes raíces** — los contratos inteligentes pueden gestionar compraventas de propiedades sin notario.
- **Regalías** — los músicos reciben pagos automáticos cada vez que se reproduce su canción.
- **Votación** — los contratos pueden proporcionar un recuento de votos transparente sin fraude.

La mayoría de estas aplicaciones aún son experimentales. Pero la tecnología avanza, y en 5-10 años los contratos inteligentes podrían ser tan comunes como el correo electrónico.

## Ideas clave

- Un contrato inteligente es un programa en la blockchain que funciona sin intervención humana
- Impulsan DeFi, NFTs, DAOs y tokens
- Ethereum es la plataforma principal para contratos inteligentes
- El mayor riesgo son los errores en el código y las vulnerabilidades
- Siempre verifica las auditorías y los permisos antes de usar cualquier dApp (aplicación descentralizada)

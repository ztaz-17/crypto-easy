---
weight: 30
title: "Permisos de Tokens: Qué Son y Por Qué Son Peligrosos"
description: "Qué son los permisos de tokens, por qué las aprobaciones ilimitadas son un riesgo de seguridad y cómo revocar el acceso a tus tokens"
category: "security"
translationKey: "token-allowances"
slug: "permisos-de-tokens-que-son"
keywords:
  - permiso de token
  - aprobación de token
  - revocar aprobación
  - riesgo de smart contract
  - aprobación Ethereum
  - aprobación ERC20
  - allowance
---

## Permisos de Tokens: Qué Son y Por Qué Son Peligrosos

---

**"Confirma el acceso a tus USDT"** — seguramente has visto este mensaje al conectar tu wallet a un nuevo servicio [DeFi](/es/glossary/#defi), un [DEX](/es/glossary/#dex) (Uniswap, PancakeSwap) o un marketplace de [NFT](/es/glossary/#nft).

Mucha gente le da a "Confirmar" sin leerlo siquiera. Y eso puede costarte absolutamente todos los tokens de tu wallet.

En este artículo veremos:

>- qué son los permisos de tokens;
>- por qué las **aprobaciones ilimitadas** son uno de los agujeros de seguridad más grandes que existen;
>- cómo revisar qué dApps tienen acceso a tus tokens;
>- cómo revocar una aprobación si diste una sin querer.

---

## ¿Qué Es un Permiso de Token?

### Cómo Funcionan los Tokens ERC-20

Para entender los permisos, primero tienes que entender cómo funcionan los tokens en realidad.

El estándar **ERC-20** (y sus primos BEP-20, TRC-20, etc.) es un smart contract con dos funciones clave:

- `transfer(from, to, amount)` — mueve tokens;
- `approve(spender, amount)` — permite que otra dirección gaste tus tokens.

Con una transferencia normal, tú firmas la transacción. Pero cuando interactúas con una app DeFi, el contrato necesita **sacar** tokens de tu cuenta por su cuenta.

Así funciona por debajo:

1. Tú llamas a `approve(contrato_DEX, 1000 USDT)`;
2. Ahora el contrato DEX puede llamar a `transferFrom(tu_dirección, pool, 1000 USDT)`;
3. El swap ocurre sin que tengas que firmar cada paso.

👉 **Eso es un permiso de token** — le das a un smart contract permiso para mover tus tokens.

---

### Una Analogía de la Vida Real

Imagina que le das las llaves de tu piso a tu vecino para que le dé de comer a tu gato mientras estás de viaje.

Un permiso de token es exactamente lo mismo, pero en versión virtual. Dejas que un contrato tome una cantidad específica de tokens (o todos ellos) y haga lo que quiera con ellos.

---

## Por Qué Es Peligroso

### Aprobaciones Ilimitadas

El problema más grande: la mayoría de las [dApps](/es/glossary/#dapp) no te piden una aprobación **limitada** — te piden una ilimitada:

```
approve(DEX, MAX_UINT_256)
```

`MAX_UINT_256` es el número más grande de Ethereum (2²⁵⁶ − 1). Prácticamente infinito.

¿Por qué hacen esto las dApps?

- **comodidad** — no hay que confirmar cada intercambio individual;
- **más barato** — una sola transacción `approve` en lugar de varias;
- **es el estándar de facto** en DeFi.

Pero el precio de esa comodidad es que **tus tokens quedan secuestrados**.

---

### Lo Que Puede Salir Mal

Si un contrato al que le diste aprobación ilimitada:

- **es hackeado** — el atacante puede drenar hasta el último token;
- **es actualizado** — los dueños del contrato pueden añadir una función que se lleve todo;
- **resulta ser malicioso** — tus fondos desaparecen al instante.

Ejemplos reales:

- **Poly Network Hack** — pérdidas de $610 millones por explotación de un puente cross-chain
- **BadgerDAO** — pérdidas de $120 millones por phishing: aprobaron en un contrato malicioso
- **Curve Finance Hack** — pérdidas de $570,000 por manipulación de permisos vía DNS

> **Importante:** un atacante no necesita tu seed phrase ni tu clave privada. Solo necesita que en algún momento hayas firmado un `approve` en un contrato malicioso — y ya está, tus tokens son suyos.

---

### No Recuerdas a Quién Le Diste Acceso

Si eres activo en DeFi, con los meses y años acumularás una docena o más de permisos: Uniswap, OpenSea, 1inch, alguna dApp de prueba random de la que ya te olvidaste.

La pregunta es: ¿de verdad recuerdas a qué contratos aprobaste?

Si dijiste "no" — no eres el único. Y es totalmente normal. Pero **esos permisos \"olvidados\" son exactamente lo que buscan los hackers**.

---

## Cómo Revisar Qué dApps Tienen Acceso a Tus Tokens

### Etherscan

La forma más directa:

1. abre [Etherscan.io](https://etherscan.io);
2. pega la dirección de tu wallet;
3. ve a la pestaña **"Token Approvals"** (o solo "Approvals");
4. verás una lista de contratos y cuánto pueden gastar.

Para BSC, usa [BscScan.com](https://bscscan.com) — la interfaz es la misma.

---

### Revoke.cash

Una opción más cómoda es [Revoke.cash](https://revoke.cash):

1. conecta tu wallet (MetaMask, WalletConnect);
2. el sitio te mostrará **todas tus aprobaciones activas** en cada red;
3. por cada aprobación verás: el contrato, el token y el límite.

El servicio no guarda tus datos y no cobra comisión — simplemente firmas las transacciones de revocación desde tu propia wallet.

---

### Otras Herramientas

- **Zapper.xyz** — panel con una sección "Approvals";
- **DeBank.com** — muestra las aprobaciones en tu perfil de wallet;
- **Rabby Wallet** — detector de aprobaciones incorporado;
- **Token Approval Checker** — un verificador simple para un solo token.

---

## Cómo Revocar una Aprobación

### Con Revoke.cash

1. abre [Revoke.cash](https://revoke.cash);
2. selecciona la red (Ethereum, Arbitrum, Optimism, BSC, etc.);
3. haz clic en **"Revoke"** junto a la aprobación que quieras eliminar;
4. confirma la transacción en tu wallet.

Listo. El contrato ya no puede gastar tus tokens.

---

### Con Etherscan

1. encuentra el token cuya aprobación quieres revocar;
2. abre el contrato del token en Etherscan;
3. ve a **"Contract" → "Write Contract"**;
4. conecta tu wallet;
5. localiza la función `approve` y establece:
   - `spender` — la dirección del contrato que aprobaste;
   - `amount` — **0** (resetea el permiso);
6. firma la transacción.

👉 **Consejo:** usa Revoke.cash — es más sencillo y seguro (menos probabilidad de equivocarte con una dirección).

---

### Cosas Importantes al Revocar

- cada `approve` a 0 es una **transacción de gas** — tendrás que pagar la comisión;
- si revocas una aprobación de un DEX en el que operas activamente, tendrás que volver a aprobar la próxima vez que hagas un swap;
- después de revocar, tus tokens se quedan en tu wallet — no se pierde nada.

---

## Buenas Prácticas: Cómo Mantenerte Seguro

### Aprueba Solo Lo Que Necesitas

En lugar de una aprobación ilimitada, especifica la **cantidad exacta** que vas a intercambiar o usar.

La mayoría de las wallets y dApps te permiten cambiar el monto en la ventana de confirmación:

- **MetaMask:** antes de firmar el `approve`, toca el monto e ingresa un **número específico**;
- **Rabby Wallet:** sugiere automáticamente una aprobación limitada.

👉 **Revisa siempre cuánto estás dejando gastar a un contrato.**

---

### Usa una Wallet Separada para DeFi

Crea una wallet "caliente" que tenga:

- solo la cantidad que estés dispuesto a arriesgar;
- no más del 5–20% de tu cartera total.

Guarda tus fondos principales en una **cold wallet** (Ledger, Trezor) o en una dirección aparte a la que las dApps no tengan acceso.

---

### Revisa Tus Aprobaciones Regularmente

Acostúmbrate a hacer esto una vez al mes:

1. ve a [Revoke.cash](https://revoke.cash);
2. revisa qué contratos tienen acceso;
3. revoca todo lo que no estés usando activamente.

Si no has tocado una dApp en 3 meses o más — revoca la aprobación.

---

### Ten Cuidado con dApps Nuevas

Antes de dar una aprobación:

- revisa el contrato en [DexScreener](https://dexscreener.com) o [Dune Analytics](https://dune.com);
- mira cuánto tiempo lleva el proyecto activo;
- busca una auditoría de smart contract;
- busca en [Twitter/X](https://x.com) opiniones de otros usuarios.

Si una dApp te pide que apruebes **todos tus tokens** de inmediato y no te deja operar sin hacerlo — eso es una **señal de alerta**.

---

### Resumen

Los permisos de tokens son un mecanismo central de DeFi — sin ellos, los swaps, los pools de liquidez y los marketplaces de NFT no funcionarían.

Pero también son **el vector de ataque más popular**:

>- las aprobaciones ilimitadas son la norma, no la excepción;
>- los permisos olvidados son una bomba de tiempo;
>- un solo clic equivocado en "Confirmar" y todos tus tokens van directo a un atacante.

Las reglas de seguridad son simples:

>- aprueba solo la cantidad que necesitas;
>- usa una wallet separada para DeFi;
>- revisa tus aprobaciones una vez al mes en [Revoke.cash](https://revoke.cash);
>- no firmes un `approve` sin mirarlo.

**Crypto te da el control sobre tu dinero. Pero hay que ejercer ese control — no repartirlo a diestra y siniestra.**

---

## FAQ

### ¿Qué es un permiso de token en lenguaje sencillo?
Es el permiso que le das a un smart contract para gastar tus tokens. Piensa en ello como entregar las llaves de tu caja fuerte — el contrato puede tomar todo lo que le hayas permitido.

### ¿Por qué es peligrosa una aprobación ilimitada?
Si el contrato es hackeado o resulta ser malicioso, el atacante puede drenar **todos** tus tokens con un solo clic.

### ¿Cómo revoco una aprobación?
La forma más fácil es a través de [Revoke.cash](https://revoke.cash) — conecta tu wallet y dale a "Revoke" en las aprobaciones que no necesites.

### ¿Necesito revocar la aprobación después de cada intercambio?
No necesariamente — pero si no planeas usar esa dApp de nuevo, es buena idea revocarla.

### ¿Voy a perder mis tokens al revocar una aprobación?
No. Los tokens se quedan en tu wallet. Revocar solo elimina el permiso del contrato para moverlos.

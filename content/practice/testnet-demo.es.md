---
weight: 3
title: "Modo Demo en Crypto: Testnet"
description: "Cómo probar crypto sin riesgo: testnets, faucets para monedas de prueba gratis y aprendizaje práctico seguro"
category: "practice"
translationKey: "testnet-demo"
slug: "testnet-demo-practice-without-risk"
keywords:
  - testnet
  - faucet
  - Goerli
  - Sepolia
  - ETH de prueba
  - modo demo crypto
  - aprendizaje seguro
prev: "/es/practice/seed-phrase-mistakes"
next: "/es/practice/buy-first-crypto"
---

## Modo Demo en Crypto: Testnet — Pruébalo Sin Riesgo

---

Has oído hablar de crypto. Quieres probarlo — pero tienes miedo de perder dinero.

Es totalmente normal.

Enviar a la dirección equivocada. Hacer clic en el botón incorrecto. Escribir mal una dirección. Y así, tu dinero desaparece para siempre. Crypto no tiene un botón "deshacer" ni un equipo de soporte que pueda revertir una transacción.

Pero aquí están las buenas noticias:

> **Puedes practicar gratis, con cero riesgo y cero inversión.**

Las criptomonedas tienen un "modo demo" incorporado — **testnets**. Son copias exactas de blockchains reales, excepto que las monedas no tienen valor real. Puedes obtenerlas gratis, enviarlas, desplegar contratos y cometer errores — todo sin consecuencias financieras.

En este artículo cubriremos:

>- qué es un testnet y para qué sirve;
>- dónde obtener monedas de prueba gratis (faucets);
>- cómo evitar confundir un testnet con la red real;
>- algunas cosas que un principiante puede probar.

---

## ¿Qué es un Testnet?

Un **testnet** es una copia completa de la red principal (mainnet), con una diferencia crucial:

> **Las monedas en un testnet no tienen valor.**

Los desarrolladores usan testnets para que los programadores puedan probar aplicaciones, contratos inteligentes y actualizaciones antes de lanzarlos en la red real. Pero cualquiera puede usarlos — incluidos los principiantes.

Así se ve en la práctica:

- Ethereum tiene varios testnets: **Sepolia**, **Goerli** (en proceso de desactivación), **Holesky**.
- Polygon tiene **Amoy** (anteriormente Mumbai).
- BNB Smart Chain tiene **BSC Testnet**.
- Bitcoin tiene **Testnet** (sí, Bitcoin también tiene un testnet).

Cada una de estas redes sigue las mismas reglas que la principal. Creas una wallet, obtienes una dirección, envías monedas y pagas comisiones (también de prueba). Solo hay una diferencia:

> **Si te equivocas — no pierdes nada.**

---

## Dónde Obtener Monedas de Prueba: Faucets

Para empezar a trabajar en un testnet, necesitas monedas de prueba. Sitios web especiales llamados **faucets** las reparten gratis.

Así funciona:

1. Ve a un sitio faucet.
2. Ingresa tu dirección de wallet de testnet.
3. Haz clic en "Solicitar" (o "Envíame ETH de prueba").
4. Unos segundos después, las monedas llegan a tu wallet.

### Faucets para Ethereum Testnet (Sepolia)

Los más populares:

- **[Google Cloud Faucet](https://cloud.google.com/application/web3/faucet/ethereum/sepolia)** — no necesitas registrarte en plataformas de terceros; puedes obtener ETH, tokens (PYUSD, WBTC, etc.) y NFTs. Solo necesitas una cuenta de Google.
- **sepoliafaucet.com** — uno de los más confiables.
- **infura.io/faucet/sepolia** — requiere una cuenta de Infura, pero da gotas regulares.
- **alchemy.com/faucets/ethereum-sepolia** — de Alchemy, también tras registro.
- **faucet.quicknode.com/ethereum/sepolia** — de QuickNode.

> 💡 Algunos faucets requieren una cuenta en la plataforma (Alchemy, Infura) o inicio de sesión con GitHub — es normal, así evitan bots.

En Google Cloud Faucet puedes solicitar ETH + tokens (ej. PYUSD y WBTC) al mismo tiempo. Si obtuviste tokens, tendrás que añadirlos a MetaMask (consulta la sección de importación de tokens abajo).

### Faucets para Otras Redes

| Red | Faucet | Moneda |
|-----|--------|--------|
| Polygon Amoy | faucet.polygon.technology | test MATIC |
| BSC Testnet | testnet.bnbchain.org/faucet-smart | test BNB |
| Bitcoin Testnet | bitcoinfaucet.energy o coinfaucet.eu | test BTC |

> **Importante:** todas las monedas de prueba existen solo dentro de su propio testnet. No puedes enviarlas a una wallet real ni cambiarlas por dinero real.

---

## Cómo Configurar MetaMask para un Testnet

Ya tienes MetaMask instalado (consulta el [artículo anterior](/es/practice/create-wallet-in-5-minutes/) para la configuración). Cambiar a un testnet solo toma un par de clics.

1. Abre MetaMask.
2. Haz clic en el menú de la derecha **&rarr;** Redes.
3. En la lista, activa **Mostrar redes de prueba**.
> ![Activando redes de prueba en MetaMask](/images/metamask-show-testnet.jpg)

4. En el selector de redes, en la pestaña **Personalizada**, elige **Sepolia**.
5. Listo — estás en un testnet.

### Obtén Monedas Gratis

Ahora consigamos algunas monedas en tu wallet crypto:

1. Copia tu dirección `ETH` de la parte superior de la wallet: `0x56f218c5aaE76128131A901F4E5cd3B9565bf014` (¡usa la tuya, por supuesto!)
2. Ve a **[Google Cloud Faucet](https://cloud.google.com/application/web3/faucet/ethereum/sepolia)**. Ingresa tu dirección y selecciona **Ethereum Sepolia**.
> ![Google Cloud Faucet — ingresando tu dirección](/images/google-cloud-faucet-input.jpg)
3. Espera a que se actualice tu saldo.
> ![Saldo de MetaMask después de reclamar](/images/metamask-balance-updated.jpg)

### ¡Dame Más! Consigamos USD

Ethereum es una blockchain que se hizo popular gracias a los contratos inteligentes.

En términos simples, un contrato inteligente es un programa que puede emitir cualquier tipo de token, NFT, definir su economía, reglas, etc. Y todo funciona con gas (Gwei — el combustible del sistema Ethereum).

> ¡Importante! Solo confía en contratos oficiales. Cualquier hacker script kiddie puede crear una moneda y enviarte millones de `USD`, atrayéndote a su sitio donde — tras saltar obstáculos — podrías darles acceso a tu wallet y perder monedas reales.

Así que asegúrate de leer las secciones de **[Seguridad](/es/security/)** y **[Bonus](/es/bonus/)** — hay mucha información útil allí. Te salvará de errores de principiante.

Bueno... ¡queremos USD!

#### Importar Tokens en MetaMask
1. Vuelve a **[Google Cloud Faucet](https://cloud.google.com/application/web3/faucet/ethereum/sepolia)**
2. Selecciona **PayPal USD (PYUSD)** y reclama monedas a tu wallet crypto
3. MetaMask te protege de los **dust tokens** y no mostrará esos tokens por defecto. Tienes dos opciones:
> - permitir que se muestren todos los tokens (no seguro)
> - añadir la dirección del contrato inteligente a tu wallet — entonces solo aparecerán esos tokens y podrás transferirlos
4. Añadamos nuestro contrato a la wallet. Puedes encontrar su dirección en la blockchain:
> - abre el explorador de bloques [sepolia.etherscan.io](https://sepolia.etherscan.io/tx/0x51ffec256bf03a539fb8b435d3b4ee0057cfd6781c452fb2321074caae25dbd9)
> - pega tu dirección de wallet `0x56f218c5aaE76128131A901F4E5cd3B9565bf014` (¡usa la tuya!)
> - ve a la pestaña **Token Transfers (ERC-20)**
> - encuentra tu transacción y copia la dirección del contrato inteligente para **ERC-20: PayPal USD (PYUSD)**
> `0xCaC524BcA292aaade2DF8A05cC58F0a65B1B3bB9`
> - en MetaMask, ve a **...** **&rarr;** **Importar tokens** **&rarr;** pega la dirección del contrato inteligente

¡Listo! Ahora tenemos **100 USD** 🎉

### Qué Puedes Probar en un Testnet

Tienes monedas de prueba. ¿Y ahora qué? Aquí tienes algunas ideas para un principiante.

#### 1. Enviar una Transferencia a una Nueva Cuenta (Tokens)

Intenta enviar ETH y tokens de una cuenta a otra:

1. En MetaMask haz clic en **&or;** junto al nombre de la cuenta **&rarr;** **+ Añadir cuenta** — aparecerá una segunda wallet con una nueva dirección.
2. Copia la dirección de la segunda cuenta.
3. Vuelve a la primera cuenta, selecciona la red **Sepolia**.
4. En la pestaña **Tokens**, selecciona PYUSD (o cualquier token que hayas recibido) **&rarr;** haz clic en **Enviar** **&rarr;** pega la dirección de la segunda cuenta **&rarr;** ingresa un monto (ej. 10 PYUSD).

Observa cómo se deduce la comisión de gas y cómo aparece la transacción en el explorador de bloques: **[sepolia.etherscan.io](https://sepolia.etherscan.io/address/0xd36D4Ed7d4Ed7414190cCDF3159E7eF561683128#tokentxns)**.

#### 2. Enviar una Transferencia a un Amigo

Pide a un amigo que te envíe algunas monedas de prueba.  
O envía algunas al autor a esta dirección: `0xd36D4Ed7d4Ed7414190cCDF3159E7eF561683128` desde tu wallet.

No olvides ver cómo se ve la transacción en el explorador de bloques: **[sepolia.etherscan.io](https://sepolia.etherscan.io/address/0xd36D4Ed7d4Ed7414190cCDF3159E7eF561683128#tokentxns)**.

#### 3. Verificar una Transacción en el Explorador

Después de cada operación, abre **[sepolia.etherscan.io](https://sepolia.etherscan.io/)**, pega el hash de la transacción y mira:

- cuánto gas pagaste;
- cuántos bloques confirmaron la transacción;
- el estado (success o failure).

Esto te enseñará a "leer" la blockchain.

#### 4. Probar una App DeFi (Con Cuidado)

Algunos protocolos (Uniswap, Aave) tienen versiones de prueba. Puedes intentar intercambiar un token por otro o prestar monedas — todo con fondos de prueba.

> 🔍 Asegúrate de que el sitio realmente ofrezca una versión de prueba. La mayoría de las dApps funcionan con la red principal por defecto.

---

## Por Qué es Seguro

La mayor ventaja de los testnets:

> **Los errores no cuestan dinero.**

Puedes:

- enviar monedas a la dirección equivocada (y no perder nada);
- perder la frase semilla de tu wallet de prueba (solo crea una nueva);
- hacer clic en un enlace de phishing (las monedas de prueba no valen nada de todos modos);
- desplegar un contrato roto (práctica gratuita).

En un testnet, construyes las habilidades que luego llevarás al mundo real — pero con dinero real.

---

## Cómo No Confundir un Testnet con Mainnet

Este es el consejo práctico más importante.

Si estás trabajando en Ethereum Mainnet y envías monedas a una dirección de testnet — **tu dinero se pierde para siempre**. Técnicamente son dos redes diferentes, pero las direcciones se ven idénticas.

Cómo mantenerse seguro:

| ✅ Haz Esto | ❌ Evita Aquello |
|-------------|-----------------|
| Siempre verifica el nombre de la red en MetaMask (junto al logo) | No tengas activos reales en la misma wallet que las monedas de prueba |
| Usa una wallet separada solo para pruebas | No cambies de red sin pensar en una sola wallet |
| Pon un tema o etiqueta diferente para tu perfil de prueba | No guardes frases semilla de prueba y reales juntas |
| Pausa antes de cada envío — verifica la red | No uses direcciones de testnet en transacciones reales |

> **Regla de oro:** antes de cualquier transacción, pausa y verifica el nombre de la red. Tres segundos — y tu dinero está seguro.

---

## Conclusión

Los testnets son la mejor manera de empezar a explorar crypto sin ningún riesgo.

Te dan lo esencial:

- **un entorno seguro** para aprender;
- **monedas gratis** para cualquier experimento que puedas imaginar;
- **total tranquilidad** — comete todos los errores que quieras.

Dedica una hora: instala MetaMask, cambia a Sepolia, obtén algo de ETH de prueba de un faucet, envía una o dos transacciones. Observa cómo aparecen en el explorador de bloques.

> **Esa hora de práctica podría ahorrarte dinero real en el futuro.**

Un testnet es tu campo de entrenamiento personal. Cero riesgo. Solo práctica.

---

## Preguntas Frecuentes

### ¿Puedo cambiar monedas de prueba por dinero real?

No. Las monedas de prueba existen solo dentro del testnet y no tienen valor en el mundo real.

### ¿Con qué frecuencia puedo solicitar monedas de prueba?

Cada faucet tiene sus propios límites — normalmente una vez cada 24 horas. Algunos dan más después del registro.

### ¿Qué pasa si un faucet no funciona?

Prueba con otro — hay docenas. O pide a un amigo que te envíe algunas monedas de prueba (son gratis, después de todo).

### ¿Puedo perder dinero real en un testnet?

No. Si solo trabajas con el testnet — no hay monedas reales allí. El peligro solo viene de confundir redes (consulta la sección anterior).

### ¿Por qué existen los testnets?

Para probar contratos inteligentes y dApps antes del lanzamiento. Un error en un contrato de mainnet puede costar millones de dólares. En un testnet — nada.

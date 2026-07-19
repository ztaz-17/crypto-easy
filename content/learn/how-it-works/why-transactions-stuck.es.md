---
weight: 240
title: "Por qué se atascan las transacciones y qué hacer al respecto"
description: "Por qué se atascan las transacciones crypto: comisiones bajas, congestión de red. Cómo acelerar o cancelar una transacción atascada"
category: "how-it-works"
translationKey: "why-transactions-stuck"
slug: "por-que-se-atascan-transacciones"
keywords:
  - transacción atascada
  - transacción pendiente
  - replace-by-fee
  - RBF
  - aceleración de transacciones
  - Bitcoin atascado
  - Ethereum atascado
---

## Por qué se atascan las transacciones y qué hacer al respecto

---

Envías algo de crypto. El monto está bien, la dirección es correcta, le das a enviar.

Y en la pantalla aparece — "Pendiente." Una hora. Dos. Cinco.

Los fondos se descontaron, pero el destinatario no los ve. La transacción está atascada en un limbo de "esperando confirmación" y no pasa nada.

¿Te suena familiar?

> **Una transacción atascada** — uno de los problemas más comunes para quienes empiezan en crypto. Pero casi siempre tiene solución.

En este artículo veremos:

> - por qué se atascan las transacciones;
> - cómo distinguir entre "está atascada" y "solo espera un poco más";
> - qué puedes hacer ahora mismo: acelerar, cancelar o reemplazar;
> - y cómo evitar terminar en esta situación en el futuro.

---

## Por qué se atascan las transacciones

### 1. Comisión demasiado baja

Esta es la razón número uno.

Cada transacción en blockchain es una solicitud para ocupar un lugar en un bloque. El espacio en los bloques es limitado. Los mineros (Bitcoin) o validadores (Ethereum) eligen qué transacciones incluir primero.

La regla es simple: **el que paga más, va primero.**

Si configuras tu comisión por debajo de la tarifa actual del mercado — tu transacción se queda en el mempool, esperando a que la red se despeje.

Aprende más sobre cómo se determinan las comisiones: [Por qué enviar crypto a veces cuesta $30](/es/learn/how-it-works/por-que-cuestan-30-las-comisiones).

---

### 2. Congestión de la red (mempool saturado)

Incluso con una comisión decente, tu transacción puede atascarse en horas pico.

Cuando miles de transacciones se envían al mismo tiempo (por ejemplo, durante un ciclo de hype de memecoins, un NFT mint o un evento importante), el mempool se inunda. El tamaño del bloque sigue siendo el mismo, pero la cantidad de personas tratando de entrar es 10 veces mayor de lo normal.

En esos momentos, los mineros solo eligen las transacciones más jugosas — todos los demás esperan.

> El mempool de Bitcoin puede alcanzar **más de 300,000 transacciones sin confirmar**. La cola de Ethereum es más pequeña, pero durante horas pico la comisión base puede dispararse 5–10x.

---

### 3. Atascada por un error de la wallet

A veces el problema no es la red — es tu wallet:

- el gas se calculó mal (en Ethereum — límite de gas por debajo de 21,000);
- la wallet no actualizó el estado de la transacción;
- estás conectado a un nodo desactualizado o roto.

En estos casos, la transacción puede mostrarse como "enviada" incluso después de haberse confirmado. Revisa en un explorador de bloques — probablemente esté todo bien.

---

### 4. Una transacción de baja prioridad fue eliminada

Si el mempool está saturado y tu comisión es bajísima, algunos nodos pueden simplemente eliminar la transacción del pool. No desaparece para siempre — si nunca se retransmite, se "evapora" y los fondos se quedan en tu dirección.

Pero hasta que envíes una nueva transacción, tus fondos están efectivamente "congelados": la red ignora la anterior, y no puedes enviar una nueva porque tu wallet cree que esos fondos ya no están.

---

## Cómo saber si una transacción está realmente atascada

Antes de entrar en pánico, revisa el estado de la transacción en un explorador de bloques:

**Bitcoin** — [mempool.space](https://mempool.space)
**Ethereum** — [etherscan.io](https://etherscan.io)
**Solana** — [solscan.io](https://solscan.io)
**TRON** — [tronscan.org](https://tronscan.org)
**BNB Chain** — [bscscan.com](https://bscscan.com)

Pega el hash de tu transacción (TXID) y verás el estado:

- **Pendiente / En Mempool** — la transacción está en la cola, aún no está en un bloque.
- **Confirmada / Éxito** — todo está bien, tu wallet solo es lenta en actualizarse.
- **Eliminada / Reemplazada** — la transacción fue reemplazada o eliminada del mempool.

> Si el estado es "Confirmada" pero tu wallet dice "Pendiente" — es un problema de la wallet, no de la red. Actualiza o reinicia la aplicación.

---

## Qué hacer si tu transacción está atascada

Tienes varias opciones. Cuál elegir depende de la red, tu wallet y qué tan paciente te sientas.

---

### 1. Reemplazar la transacción mediante RBF (Replace-by-Fee)

**Funciona en:** Bitcoin (y algunas otras cadenas basadas en UTXO)
**Requiere:** una wallet que soporte RBF

Replace-by-Fee es un mecanismo que te permite reenviar exactamente la misma transacción (mismos inputs) pero con una comisión más alta. Le estás diciendo a la red: "Olvida la transacción anterior — aquí está la nueva con un aumento."

Cómo hacerlo:

1. Abre tu wallet y encuentra la transacción atascada.
2. Busca **"Aumentar comisión"** o **"Replace-by-Fee"** (el nombre depende de tu wallet).
3. Establece una nueva comisión — normalmente la tarifa actual del mercado es suficiente.
4. Confirma — y la nueva transacción reemplaza a la anterior.

**Importante:** RBF debe estar habilitado antes de enviar la primera transacción. Si enviaste una transacción sin la marca RBF — no puedes reemplazarla mediante este mecanismo.

Wallets que soportan RBF:

- Electrum — soporte completo;
- Bitcoin Core — sí;
- BlueWallet — sí;
- Exodus — sí;
- Trust Wallet — no (hasta ahora).

> Si tu wallet no soporta RBF — prueba la opción 2 o 3.

---

### 2. Usar un Acelerador de Transacciones

**Funciona en:** Bitcoin (limitado)

Algunos pools de minería ofrecen servicios de aceleración de transacciones. Envías el hash de tu transacción atascada, pagas una comisión — y el pool la incluye en el siguiente bloque que minen.

Servicios populares:

- [Viabtc Accelerator](https://www.viabtc.com/tools/txaccelerator) — gratis hasta 100 transacciones por hora, pero no garantiza inclusión;
- [BTC.com Accelerator](https://pushtx.btc.com/) — gratis.

**Desventajas:**

- no siempre funcionan;
- los espacios gratis se llenan rápido;
- las versiones de pago cuestan dinero (a menudo más que una comisión normal).

Úsalo solo si RBF no está disponible y no puedes esperar más.

---

### 3. Cancelar mediante Doble Gasto (Child-Pays-For-Parent / CPFP)

**Funciona en:** Bitcoin, Ethereum y otras redes

CPFP es un mecanismo donde envías una **nueva transacción** que gasta los outputs (UTXOs) de la transacción atascada. La nueva lleva una comisión más alta — los mineros toman ambas, porque sin la primera la segunda no es válida.

Cómo hacerlo:

1. Encuentra la transacción atascada en tu wallet.
2. Si tu wallet soporta CPFP — elige **"Acelerar con transacción hija"**.
3. Establece la comisión para la transacción hija.
4. Confirma.

**Para Ethereum (MetaMask):**

1. En MetaMask, abre la transacción atascada.
2. Haz clic en **"Acelerar"** — la wallet reenvía la misma transacción con una comisión más alta.
3. O haz clic en **"Cancelar"** — MetaMask envía una transacción "en blanco" (0 ETH) que reemplaza a la anterior.

> **Importante:** cancelar en Ethereum también es una transacción con comisión. Pagas para reemplazar la atascada.

---

### 4. Solo esperar

Sí, también es una opción.

En Bitcoin, las transacciones con comisión baja pueden quedarse colgadas horas o incluso días. Pero tarde o temprano — cuando la red se despeje o alguien aumente la comisión en ese bloque — tu transacción se incluye.

Tiempos de espera estimados:

- **Bitcoin:** de 1 hora a 3–7 días en casos extremos (si el mempool está lleno y tu comisión es mínima).
- **Ethereum:** de 1 minuto a unas pocas horas.
- **Solana / TRON:** rara vez se atascan, pero si lo hacen — hasta una hora.

> Si han pasado más de 3 días y la transacción sigue "Pendiente" — prueba cualquiera de los métodos anteriores.

---

### 5. Reenviar después de que la transacción salga del mempool

Si la transacción fue eliminada del mempool (generalmente después de 2–7 días en Bitcoin, antes en otras redes) — los fondos vuelven automáticamente a tu dirección.

Simplemente puedes enviar una nueva transacción — con una comisión razonable y en un periodo tranquilo.

Hay un detalle: no todas las wallets muestran correctamente la devolución. Puede que aún parezca que tus fondos están "bloqueados." Revisa tu saldo en un explorador de bloques — si la transacción ya no está en el mempool, los fondos son tuyos nuevamente.

---

## Referencia rápida: qué hacer en cada situación

**Comisión baja, RBF habilitado** → Bitcoin: **RBF** — reemplazar con aumento | Ethereum: **Acelerar** en MetaMask | Otras redes: Depende de la wallet
**Comisión baja, RBF deshabilitado** → Bitcoin: **CPFP** o acelerador | Ethereum: **Cancelar** + nueva transacción | Otras redes: Enviar nueva con nonce más alto
**Congestión de red** → Bitcoin: Esperar o acelerador | Ethereum: Esperar — el gas bajará | Otras redes: Esperar
**Transacción eliminada del mempool** → Bitcoin: Reenviar | Ethereum: Reenviar | Otras redes: Reenviar
**La wallet muestra estado incorrecto** → Bitcoin: Revisar explorador | Ethereum: Revisar explorador | Otras redes: Revisar explorador
**Necesito que se haga ya** → Bitcoin: Acelerador (de pago) | Ethereum: Acelerar con gas alto | Otras redes: Aumentar comisión

---

## Cómo prevenir transacciones atascadas en el futuro

### 1. Revisa el mempool antes de enviar

Antes de transmitir una transacción, verifica la congestión de la red:

- Bitcoin: [mempool.space](https://mempool.space)
- Ethereum: [etherscan.io/gastracker](https://etherscan.io/gastracker)

Si el mempool está lleno — espera una hora o dos, o sube la comisión.

### 2. Configura tu comisión ligeramente por encima del promedio

Las wallets avanzadas ofrecen tres niveles de comisión:

- **Lenta** — ahorras dinero, pero el riesgo de atasco es mayor;
- **De mercado / Normal** — un equilibrio razonable;
- **Rápida** — pagas de más, pero la transacción se incluye en el siguiente bloque.

Para la mayoría de los casos, elige **De mercado**. La diferencia entre Lenta y De mercado suele ser de $0.50–$2, pero el tiempo de espera es 3–5 veces menor.

### 3. Habilita RBF de antemano

Si tu wallet soporta RBF — **actívalo en la configuración antes de enviar.** No cambia la comisión de la primera transacción, pero te da la opción de reemplazarla si algo sale mal.

### 4. Elige la red adecuada

Bitcoin y Ethereum no son las únicas opciones. Si no los necesitas específicamente:

- **Litecoin** — bloques cada 2.5 minutos, comisiones de centavos;
- **Solana** — instantáneo, costo casi nulo;
- **TRON** — barato y rápido para USDT;
- **Lightning Network** — Bitcoin, pero confirmación en segundos.

> Solo asegúrate de que el destinatario soporte la red que elijas.

### 5. Usa redes de Capa 2

Si estás en Ethereum:

- Arbitrum;
- Optimism;
- Base;
- zkSync.

Las comisiones son 50–100 veces más bajas que en la red principal de Ethereum, y la seguridad es la misma.

---

## Una historia real

Hace un tiempo estaba comprando un dominio por 0.5 ETH. Ingresé la dirección, la verifiqué dos veces, le di a enviar. La comisión la puse en "Lenta" — pensé que me ahorraría $3.

Pasaron 15 minutos. La transacción estaba Pendiente.

30 minutos — Pendiente.

Una hora — Pendiente.

Empecé a sudar: el dominio podía ser comprado por otro si no pagaba pronto. Revisé Etherscan — el mempool estaba lleno (había una venta de NFT en curso) y la comisión base se había duplicado. Mi transacción estaba al final de la cola.

Tuve que usar "Acelerar" con una comisión de $22 en lugar de los $4 que había planeado.

**Conclusión:** conseguí el dominio, pero tratar de ahorrar $3 terminó costándome $18 extra. Si hubiera puesto una comisión razonable desde el principio, la transacción se habría confirmado en 2 minutos.

> Desde entonces, nunca pongo la comisión mínima cuando el tiempo importa. Ahorrar $2 no vale una hora de estrés.

---

## Resumen

Una transacción atascada es molesta, pero casi siempre tiene solución.

**Puntos clave:**

- la razón #1 — comisión baja y mempool congestionado;
- primero, revisa el estado en un explorador de bloques — puede que la transacción ya esté confirmada;
- usa RBF (Bitcoin) o Acelerar (Ethereum) para acelerar;
- si RBF no está disponible — prueba CPFP o un acelerador;
- como último recurso — solo espera, la transacción no desaparecerá (los fondos volverán);
- de ahora en adelante — pon una comisión razonable, vigila el mempool y activa RBF con anticipación.

Crypto no es "enviar y olvidar." Se trata de entender cómo funciona la red. Y cuanto mejor lo entiendas — menos veces verás "Pendiente" en tu pantalla.

> Como dice el dicho: "No tus llaves, no tus monedas. No confirmada, no tu transacción."

---

## FAQ

### ¿Por qué mi transacción está atascada en Pendiente?

Tu transacción está en el mempool pero aún no ha sido incluida en un bloque. La causa es una comisión baja, congestión de la red, o ambas.

### ¿Cuánto tiempo puede estar atascada una transacción?

Bitcoin — de 1 hora a 3–7 días. Ethereum — de 1 minuto a varias horas. Solana, TRON — rara vez más de una hora.

### ¿Puedo cancelar una transacción atascada?

Sí, si aún no ha sido confirmada. En Bitcoin — mediante RBF (reemplazar) o CPFP. En Ethereum — mediante "Cancelar" en MetaMask. En otras redes — enviando una transacción con un nonce más alto.

### ¿Perderé mi dinero si la transacción se atasca?

No. Si la transacción no llega a un bloque, eventualmente será eliminada del mempool y los fondos volverán a tu dirección. Si la transacción ya está en un bloque — el dinero está con el destinatario (no se puede cancelar).

### ¿Qué hago si mi wallet no soporta RBF?

Usa CPFP (Child-Pays-For-Parent) o servicios de aceleración de transacciones (Viabtc, BTC.com). O simplemente espera.

### ¿Cómo sé si RBF está habilitado en mi wallet?

Abre la configuración de envío de transacciones. Si ves "Activar RBF" o "Replace-by-Fee" — actívalo. Si no lo ves, probablemente tu wallet no lo soporta. Electrum y Bitcoin Core definitivamente lo tienen.

### ¿Por qué MetaMask muestra "Pendiente" incluso después de la confirmación?

Esto es un problema de la wallet, no de la red. Revisa el hash de la transacción en Etherscan — si el estado es "Éxito", todo está bien. Actualiza MetaMask o reinicia la extensión.

### ¿Puedo acelerar una transacción en un exchange?

Generalmente no. Los exchanges usan sus propias wallets internas y deciden cuándo transmitir la transacción. Si un exchange está demorando un retiro — contacta a su soporte.

### ¿Qué hago si mi transacción lleva una semana atascada?

Revisa si ha sido eliminada del mempool. Si es así — reenvía con una comisión razonable. Si no — prueba RBF, CPFP o un acelerador. Después de una semana, solo quedan en el mempool transacciones "muertas" — casi nadie las recoge.

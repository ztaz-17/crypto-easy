---
weight: 4
title: "Qué hacer si te hackean la wallet de cripto"
description: "Pasos de emergencia cuando te hackean la wallet cripto: cómo salvar tus activos, qué acciones tomar en los primeros minutos"
category: "security"
translationKey: "hacked-what-to-do"
slug: "que-hacer-si-te-hackean-wallet"
keywords:
  - wallet hackeada
  - robo de cripto
  - respuesta de emergencia
  - cripto robado
  - revocar accesos
  - mover fondos
prev: "/es/security/permisos-de-tokens-que-son"
next: "/es/security/common-mistakes"
---

## Qué hacer si te hackean la wallet de cripto

---

Abres tu app de wallet — y no reconoces tu saldo.

Los tokens que estaban en tu cuenta ya no están. O ves un par de transacciones raras que nunca hiciste.

Podría ser peor: estás viendo cómo alguien vacía tus fondos en este mismo momento.

> **En cripto, nadie te va a devolver el dinero robado.**

Ni un banco. Ni la policía. Ni los desarrolladores de la blockchain.

Pero eso no significa que no puedas hacer nada. Este artículo te da un plan de acción claro para los primeros minutos después de descubrir el hackeo.

---

## Los primeros segundos: no entres en pánico

Tu peor enemigo en esta situación es el pánico. Es lo que te hace cagarla:

- mover tus fondos restantes a una wallet "segura" que en realidad pertenece al estafador;
- hacer clic en links de mensajes turbios de "recupera tus fondos";
- pagar "comisiones de gas" para recuperar tu dinero robado;
- darle tu frase semilla al "equipo de soporte."

Todo esto son trampas que solo van a empeorar las cosas.

> **Regla #1: Para. Mira a tu alrededor. Sigue el plan.**

---

## Paso 1. Aísla la wallet

En el momento en que notes actividad sospechosa, tu objetivo es **cortar el acceso** del atacante a tus fondos.

Si se comprometió una wallet caliente (MetaMask, Trust Wallet, Phantom, etc.):

1. **Apaga el internet** del dispositivo (modo avión) si ves una transacción que todavía no se confirmó. Esto no ayuda si la frase semilla ya está expuesta, pero puede comprarte unos segundos.
2. **Crea una wallet nueva de inmediato** — en otro dispositivo o en otra app.
3. **Genera una frase semilla nueva.** Nunca reutilices la anterior.

> **Tu wallet vieja nunca volverá a ser segura. Nunca.**

---

## Paso 2. Rescata lo que quede

Si todavía hay fondos en la wallet — actúa rápido:

- Abre una wallet nueva y limpia (frase semilla nueva, dirección nueva).
- Transfiere **todos los tokens restantes** a ella.
- Empieza por los activos de mayor valor.
- Asegúrate de que la wallet vieja no tenga tokens reclamables (staking, recompensas de farming).

Importante: el estafador pudo haber puesto un script que intercepta transferencias entrantes automáticamente. Así que:

> **No le mandes nada a la dirección comprometida.**

Aunque recibas un mensaje que diga "envía 0.001 ETH a la dirección anterior para recuperar tus fondos" — es una estafa.

---

## Paso 3. Revoca los permisos de tokens

A menudo un hackeo no ocurre por robo de frase semilla, sino por **permisos de tokens** maliciosos.

Esto es lo que pasa:

- una vez firmaste una transacción que le dio acceso a un contrato inteligente a tus tokens;
- el atacante usa ese acceso y vacía tus fondos.

Incluso después de mover tus fondos restantes a una wallet nueva, **los permisos en la dirección anterior podrían usarse de nuevo** si alguna vez llega algo allí.

Qué hacer:

1. Ve a [Revoke.cash](https://revoke.cash) o un servicio similar.
2. Conecta la wallet **comprometida** (solo lectura, no firmes ninguna transacción).
3. Busca tokens con permisos sospechosos.
4. Revócalos.

> **Revisa los permisos en cada dirección donde hayas tenido activos.**

---

## Paso 4. Cambia todas las contraseñas y frases semilla

Si un atacante entró a una cuenta, puede haber comprometido otras también:

- tu contraseña del exchange;
- tu correo electrónico (mediante una simulación de cambio de contraseña);
- tu Google Authenticator / 2FA.

Así que:

1. Cambia la contraseña en **cada exchange** donde tengas cuenta.
2. Actualiza el 2FA — genera llaves nuevas.
3. Verifica si cambiaron tu correo o número de teléfono.
4. Si usas la misma contraseña en varios servicios — **cámbialas todas**.

> **Usa un gestor de contraseñas. Una contraseña, un servicio.**

---

## Paso 5. Regenera tu frase semilla por completo

Si sospechas que tu frase semilla está comprometida, **no intentes "arreglarla"**.

Crea una wallet completamente nueva desde cero:

1. Instala una app de wallet nueva (o usa un navegador/dispositivo limpio).
2. Crea una wallet nueva — **genera una frase semilla completamente nueva**.
3. Escríbela en papel. Nunca la almacenes digitalmente.
4. Transfiere los fondos desde tus otras direcciones a la wallet nueva.

¿La frase semilla anterior? Tírala. Está comprometida.

---

## Paso 6. Contacta al soporte del exchange

Si el atacante logró mover los fondos a un exchange centralizado (Binance, Bybit, Kraken, OKX), hay una posibilidad de que el exchange pueda **congelar la cuenta del estafador**.

Qué hacer:

1. Contacta al equipo de soporte del exchange lo más rápido que puedas.
2. Proporciona:
   - tu dirección de wallet comprometida;
   - el hash de la transacción donde robaron los fondos;
   - la dirección de destino (si la conoces);
   - la fecha y hora del incidente.
3. Pídeles que congelen la cuenta del destinatario.

Las probabilidades no son altas, pero no son cero — sobre todo si la cantidad es grande y actúas rápido.

> **Cuanto más rápido actúes, mejores serán tus posibilidades.**

---

## Paso 7. Advierte a la comunidad

Si fuiste víctima de una estafa específica, un sitio de phishing o una dApp maliciosa:

- repórtalo en [Scam Sniffer](https://scamsniffer.io) (una base de datos de estafas conocidas);
- publica en X (Twitter) etiquetando al proyecto o wallet involucrado;
- advierte a otros en chats de Telegram o Discord.

Así ayudas a que la próxima persona no caiga en la misma trampa.

---

## Lo que NO debes hacer

Algunas cosas **solo empeorarán la situación**:

- ❌ Pagar "gas" o una comisión para recuperar tus fondos — 100% estafa.
- ❌ Usar "servicios de recuperación de cripto" — todos son fraudulentos.
- ❌ Descargar software recomendado por desconocidos en redes sociales.
- ❌ Decir tu frase semilla a nadie, ni siquiera a "representantes de la wallet."
- ❌ Intentar "revertir" una transacción en la blockchain — es imposible.

> **Si alguien te promete recuperar tu dinero robado a cambio de una comisión — te está estafando.**

---

## Prevención para el futuro

Una vez que hayas manejado la emergencia, vale la pena repensar tus hábitos de seguridad:

- ✅ Usa una **wallet de hardware** (Ledger, Trezor) para guardar cantidades grandes.
- ✅ Pon **límites de transacción** en tu wallet.
- ✅ Revisa los permisos de tokens una vez al mes.
- ✅ No firmes transacciones que no entiendas.
- ✅ Usa wallets separadas para distintos propósitos (una para el día a día, otra para ahorros).
- ✅ Guarda tu frase semilla **físicamente** (papel, metal) donde nadie más pueda acceder.

> **Cripto te da libertad. Pero la libertad viene con responsabilidad.**

---

## FAQ

### ¿Puedo recuperar mis fondos robados?
En la mayoría de los casos — no. La blockchain es irreversible. La excepción es si los fondos terminaron en un exchange centralizado y lo reportaste a tiempo.

### ¿Qué pasa si robaron mi frase semilla pero mis fondos todavía están ahí?
Crea una wallet nueva de inmediato y transfiere todo. La frase semilla anterior ahora está comprometida.

### ¿Debo pagar "comisiones de gas" para recuperar mis fondos?
No. Eso es una estafa. Los fondos robados no se devuelven pagando una comisión.

### ¿La policía va a ayudar?
Casi nunca. Cripto no tiene un "emisor" que pueda revertir una transacción. Ir a la policía solo tiene sentido para cantidades muy grandes y si puedes proporcionar datos del sospechoso.

### ¿Qué hago si me hackearon la wallet de un exchange?
Contacta al soporte del exchange de inmediato, cambia tu contraseña, revoca todas las claves API y activa el 2FA (si no lo habías hecho ya). Los exchanges pueden congelar retiros mientras investigan.

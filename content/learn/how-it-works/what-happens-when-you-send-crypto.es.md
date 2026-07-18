---
weight: 1
title: "Qué ocurre cuando envías cripto"
description: "Detrás de escena de una transacción cripto: creación, firma, difusión en la red y confirmación — explicado de forma sencilla"
category: "how-it-works"
translationKey: "what-happens-when-you-send-crypto"
slug: "que-ocurre-cuando-envias-crypto"
keywords:
  - transacción cripto
  - cómo funciona cripto
  - transacción blockchain
  - firma de transacción
  - minería
  - confirmación
  - difusión en la red
prev: "/es/learn/basis/clave-privada"
next: "/es/learn/how-it-works/por-que-transferencia-puede-costar-30"
---

## Qué ocurre cuando envías cripto

---

Abres tu cartera, pones la dirección del destinatario, introduces el importe — y pulsas «Enviar».

¿El dinero ya se fue? Todavía no.

Aparece un mensaje en tu pantalla: «Transacción enviada. Esperando confirmación...»

Y ahí es donde empieza la verdadera acción.

Lo que sucede a continuación es un intrincado baile entre tu cartera, miles de ordenadores en todo el mundo y las matemáticas que mantienen el sistema honesto.

> En este artículo, desglosaremos cada etapa: desde el momento en que pulsas «Enviar» hasta que las monedas aterrizan en la cartera del destinatario.

Veamos qué pasa realmente cuando envías cripto.

---

## Etapa 1: Creación de la transacción

Todo empieza con tu cartera recopilando datos. Construye un «paquete» digital — una transacción. Dentro de este paquete:

- **desde** — tu dirección pública;
- **hasta** — la dirección del destinatario;
- **importe** — cuánto estás enviando;
- **comisión** — lo que pagas a la red por procesarlo.

La transacción aún no se ha enviado. Es solo un borrador — un conjunto de datos que solo existe en tu dispositivo.

### Lo que es importante saber

Tu cartera no «saca» dinero de una cuenta. En cambio, revisa todo el historial de transacciones anteriores que alguna vez llegaron a tu dirección y selecciona los saldos no gastados.

Piensa que es como tener varios billetes diferentes en el bolsillo, y eliges con cuál pagar. En cripto, esos «billetes» son registros en la blockchain.

> Para más información sobre cómo funcionan las direcciones y las claves, consulta el glosario: [dirección pública](/es/glossary/#direccion-publica), [clave privada](/es/glossary/#clave-privada).

---

## Etapa 2: Firma de la transacción

Ahora viene la parte más importante.

Tu cartera toma los datos de la transacción y los firma con tu **clave privada**. Es como poner tu sello digital personal — uno que no se puede falsificar.

### Por qué las firmas no se pueden falsificar

Tu clave privada es una larga cadena aleatoria de caracteres. Solo tú la conoces. La red solo conoce tu dirección pública — un derivado de esa clave.

Cuando firmas una transacción:

1. Tu cartera aplica una fórmula matemática a los datos de la transacción y a tu clave.
2. El resultado es una **firma digital** — una cadena única de caracteres.
3. Cualquier participante de la red puede verificar esta firma usando tu dirección pública.
4. Pero nadie puede reconstruir tu clave privada a partir de la firma.

> **Importante:** tu clave privada nunca se envía a ningún lado. Se queda en tu dispositivo. La red verifica la firma sin ver nunca la clave en sí.

Si alguien intenta cambiar el importe de una transacción firmada — la firma se invalida. La red la rechaza de inmediato.

Esa es la magia: demuestras que eres dueño de los fondos sin revelar tu secreto.

---

## Etapa 3: Difusión por la red

La transacción está firmada. Ahora necesita llegar a la red.

Tu cartera envía la transacción a uno o más nodos de la red — **nodos**. Un nodo es un ordenador que ejecuta un cliente completo de blockchain. Almacena todo el historial de transacciones y verifica las nuevas.

### Lo que comprueba un nodo

Cuando un nodo recibe tu transacción, verifica:

- la firma es correcta;
- tienes fondos suficientes;
- no estás intentando gastar las mismas monedas dos veces (doble gasto).

Si todo está en orden — el nodo añade la transacción al **mempool** (abreviatura de memory pool, grupo de memoria). Esta es el área de espera para transacciones no confirmadas.

### El mempool — una sala de espera

Piensa en una estación de tren. Tu transacción es un pasajero esperando subir a un tren (un bloque). Hay muchos pasajeros, el tren sale solo cada 10 minutos (en el caso de Bitcoin), y los asientos son limitados.

¿Quién sube al tren? Los que pagaron un boleto — es decir, la comisión. Cuanto más alta sea la comisión, antes será seleccionada tu transacción para un bloque.

> Si la comisión es demasiado baja, tu transacción podría esperar horas o incluso días. En cualquier momento, el mempool puede contener decenas de miles de transacciones no confirmadas.

Después de la verificación, el nodo **retransmite** (difunde) la transacción a sus vecinos. Ellos la retransmiten a los suyos. En cuestión de segundos, la transacción se extiende por todo el mundo.

---

## Etapa 4: Confirmación en un bloque

La transacción está en el mempool. Ahora necesita ser confirmada por un **minero** (en Bitcoin) o un **validador** (en Ethereum y otras redes PoS).

### Cómo eligen los mineros las transacciones

Los mineros recogen transacciones del mempool y las empaquetan en un bloque. La prioridad depende de la comisión — cuanto más alta es la comisión, mayor es la prioridad.

Una vez montado el bloque, el minero empieza a resolver un rompecabezas matemático (Prueba de Trabajo) para sellar el bloque. Esto requiere una potencia de cálculo masiva. Quien lo resuelva primero recibe:

- la recompensa del bloque (monedas recién acuñadas);
- todas las comisiones de las transacciones incluidas.

En cuanto se encuentra un bloque, el minero lo difunde a todos los nodos. Los nodos verifican el bloque y, si todo es correcto, lo añaden a su cadena.

### Cuánto esperar para la confirmación

Para Bitcoin, una confirmación significa que tu transacción ha entrado en un bloque. Pero la gente suele esperar varias confirmaciones (cuantas más, más seguro):

| Red | Tiempo por bloque | Cuántas esperar |
|---------|-----------|-----------------|
| Bitcoin | ~10 minutos | 3 bloques (~30 min) |
| Ethereum | ~12 segundos | 12–30 bloques (~2–6 min) |
| Solana | ~400 ms | 1 bloque (instantáneo) |

> ¿Por qué no solo una confirmación? Porque en teoría, un minero podría producir un bloque alternativo (una bifurcación). Cuantos más bloques vengan después del tuyo, más difícil será revertir la transacción. Tras 6 confirmaciones en Bitcoin, una reversión es prácticamente imposible.

---

## Tabla resumen: etapas de una transacción

Aquí está el recorrido completo que hace una transacción desde que pulsas «Enviar» hasta la confirmación final:

| Etapa | Qué sucede | Quién participa | Tiempo |
|-------|-------------|---------------|------|
| 1. Creación | La cartera prepara los datos: desde, hasta, importe | Tu cartera | Instantáneo |
| 2. Firma | La transacción se firma con tu clave privada | Tu cartera | Instantáneo |
| 3. Difusión | La transacción se envía a los nodos, llega al mempool | Nodos, mempool | Segundos–minutos |
| 4. Confirmación | El minero/validador añade la transacción a un bloque | Mineros/validadores | Minutos–horas |
| 5. Finalización | El bloque se añade a la cadena, la transacción está completa | Todos los nodos de la red | Unos bloques más |

---

## ¿Y las comisiones?

La comisión es el pago por un sitio en un bloque. Tiene dos partes:

- **comisión base** — la tarifa de referencia fijada por la red;
- **comisión prioritaria** — lo que añades voluntariamente para acelerar las cosas.

En Bitcoin, la comisión no se basa en el importe que envías — se basa en el **tamaño de la transacción en bytes**. Cuanto más compleja es la transacción (muchas entradas y salidas), más «pesada» y cara resulta.

En Ethereum, la comisión depende de la complejidad de la operación (gas). Una transferencia sencilla cuesta unos 21.000 gas. Interactuar con un contrato inteligente puede costar cientos de miles.

> Más información: [comisión de red](/es/glossary/#comision-de-red), [gas](/es/glossary/#gas).

---

## ¿Qué ve el destinatario?

El destinatario puede ver la transacción en cuanto se difunde — incluso antes de la confirmación.

Su cartera puede mostrar un estado de «Pendiente». Las monedas aún no han llegado, pero está claro que una transferencia está en camino.

Tras la primera confirmación, el saldo se actualiza. Los exchanges y servicios suelen acreditar los fondos después de un cierto número de confirmaciones — por seguridad.

---

## ¿Qué puede salir mal?

### Transacción atascada

Si la comisión es demasiado baja, los mineros pueden ignorar tu transacción. Se queda en el mempool esperando.

En Bitcoin, estas transacciones pueden quedarse ahí durante días. En Ethereum, existe el mecanismo Replace-by-Fee — puedes reenviar la misma transacción con una comisión más alta.

### Transacción rechazada

Si la red está congestionada y tu comisión es mínima, la transacción puede ser «expulsada» del mempool y devuelta sin gastar. Tu dinero no desaparece — vuelve a tu dirección.

### Transacción cancelada

No puedes cancelar una transacción firmada y enviada. Así es la naturaleza de la blockchain — el registro es inmutable. Si enviaste a la dirección equivocada, solo el destinatario puede devolver las monedas.

> Revisa siempre la dirección antes de enviar. Como mínimo, los primeros 4 y los últimos 4 caracteres.

---

## Conclusión

Cuando pulsas «Enviar», se desencadena toda una cadena de eventos:

1. **Creación** — tu cartera prepara los datos.
2. **Firma** — tu clave privada demuestra que es tu dinero.
3. **Difusión** — la transacción viaja por la red hasta el mempool.
4. **Confirmación** — un minero la incluye en un bloque.
5. **Finalización** — el bloque se convierte en parte permanente de la blockchain.

Todo este sistema funciona sin bancos, sin intermediarios, sin una sola autoridad central. Solo matemáticas, miles de ordenadores independientes y tu clave privada.

> El cripto no va de magia. Va de matemáticas — del tipo que te da control sobre tu propio dinero.

---

## Preguntas frecuentes

### ¿Puedo cancelar una transacción después de enviarla?
No. Una vez que una transacción se firma y se envía a la red, no se puede cancelar. Solo el destinatario puede devolver los fondos. Verifica siempre la dirección.

### ¿Por qué unas transacciones se procesan en minutos y otras tardan horas?
Todo se reduce a la comisión y la congestión de la red. En horas punta, los mineros eligen las transacciones con las comisiones más altas. Si la tuya es baja — toca esperar.

### ¿Qué ocurre si envío monedas a una dirección que no existe?
Lo más probable es que la red rechace la transacción. Pero si la dirección existe y simplemente no pertenece a nadie (o pertenece a otra persona), las monedas llegarán allí sin posibilidad de recuperarlas.

### ¿Qué es el doble gasto?
Es un intento de enviar las mismas monedas a dos destinatarios diferentes. La blockchain lo impide mediante el consenso: la primera transacción confirmada se considera válida y la segunda se rechaza.

### ¿Cómo puedo comprobar el estado de mi transacción?
Usa un explorador de blockchain. Para Bitcoin — [mempool.space](https://mempool.space), para Ethereum — [etherscan.io](https://etherscan.io). Pega el hash de tu transacción y verás todo: desde el mempool hasta la confirmación final.

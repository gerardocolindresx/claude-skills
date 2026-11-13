---
name: anti-ai-slop
description: Escribe o revisa textos para que no suenen a IA. Aplica una lista de estructuras de frase, expresiones, palabras y formatos que delatan un texto generado (el «no es X, es Y», los «¿El resultado? X», la negrita por todas partes, los emojis al principio de cada línea, las rayas largas, «crucial», «navegar», «en el mundo actual»...) y devuelve el texto limpio, o un informe de lo que falla si se lo pides. Funciona en español y en inglés. Úsala cuando digas "que no suene a IA", "quita el AI slop", "revisa este texto", "humaniza esto", "anti AI slop", "/anti-ai-slop", o antes de publicar un post, un artículo, un email o el copy de una web.
version: '1.0.0'
license: MIT
---

# Anti AI slop

Los lectores notan cuándo un texto lo ha escrito una IA. En cuanto ven una frase de IA, dejan de fiarse del resto. Esta skill sirve para escribir como una persona lista que le escribe a un amigo: palabras de diario, frases cortas, ejemplos concretos y números reales.

Habla en el idioma del usuario. Las listas están en dos archivos:
- `references/lista-es.md` para textos en español.
- `references/lista-en.md` para textos en inglés.

Si el texto está en otro idioma, usa la inglesa y busca los equivalentes.

## Qué hacer

Primero averigua cuál de estos tres casos es. Si no está claro, pregunta en una línea.

1. **Escribir un texto nuevo.** Escríbelo aplicando las listas desde el principio y repásalo antes de entregarlo (ver «Repaso final»).
2. **Limpiar un texto que te pasan** (es el caso por defecto). Revisa cada línea contra las listas. Si una línea contiene algo de ellas, reescríbela con palabras normales o quítala. Devuelve solo el texto limpio, sin explicar qué has quitado.
3. **Auditar un texto** («dime si suena a IA», «¿cumple la lista?»). No reescribas. Devuelve:
   - lo que está bien;
   - cada frase que falla, citada, con el patrón en el que cae;
   - el recuento de negritas, emojis y rayas largas;
   - una propuesta de reescritura por frase.
   Al final, pregunta si aplicas los cambios.

## Reglas
- Revisa las variantes cercanas además de lo literal: otro tiempo verbal, plural o un pequeño cambio de redacción cuentan igual.
- Conserva el contenido: datos, nombres, enlaces y la estructura del autor. Cambia la forma, no lo que dice.
- No inventes datos para sustituir una frase vacía. Si al quitar una frase falta información, márcalo con `[AÑADIR DATO]`.
- Si el autor tiene una guía de voz propia que choca con la lista (por ejemplo, usa emojis a propósito), díselo y pregúntale cuál manda. No la ignores en silencio.
- Las notas internas, instrucciones o borradores de trabajo no se tocan salvo que lo pida. La lista es para lo que se publica.

## Formato (vale para cualquier idioma)
- Sin rayas largas (—).
- Sin emojis, tampoco al principio de las líneas.
- Sin negrita, salvo que el autor la pida.
- Sin hashtags.
- Sin títulos de sección en textos cortos (posts, emails). En artículos largos sí se usan.
- No empieces dos frases seguidas con las mismas palabras.
- No repitas la misma plantilla en cada bloque (por ejemplo, terminar cada punto con la misma coletilla).

## Repaso final (antes de entregar)
1. Busca `—`, `**`, `#` y emojis.
2. Lee los comienzos de frase uno detrás de otro.
3. Busca las negaciones con giro («no es», «sino», «not», «isn't»), las preguntas que se responden solas (`¿...? X.` / `...? X.`) y las palabras de la lista.
4. Lee el texto entero en voz alta, mentalmente. Si una frase no la dirías en un mensaje a un amigo, cámbiala.

## Origen
Basada en una lista que circula como imagen («Copy this image into ChatGPT or Claude», autor desconocido), adaptada al español y ampliada por Gerardo Colindres.

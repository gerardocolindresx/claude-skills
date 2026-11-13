# claude-skills

Skills para Claude Code de creación de contenido: las que uso en mi día a día de growth, producto y escritura. Las comparto tal cual las uso, en español.

Una skill es una carpeta con instrucciones (`SKILL.md`) que Claude lee y aplica cuando la tarea lo pide. No hace falta saber programar para usarlas.

## Skills

| Skill | Qué hace |
|---|---|
| [`anti-ai-slop`](anti-ai-slop/SKILL.md) | Escribe o revisa textos para que no suenen a IA. Aplica una lista de estructuras de frase, expresiones, palabras y formatos que delatan un texto generado y te devuelve el texto limpio, o un informe de lo que falla. En español y en inglés. |
| [`substack-research`](substack-research/SKILL.md) | Enriquece el borrador de tu próximo artículo de Substack (o de cualquier newsletter o blog): te entrevista, cruza la idea con lo que ya publicaste y con tus archivos, hace un research web ligero y te entrega un dossier por secciones. No reescribe tu borrador. |

## Cómo instalar una skill

1. Descarga el repositorio (botón **Code → Download ZIP**) o clónalo:
   ```bash
   git clone https://github.com/gerardocolindresx/claude-skills.git
   ```
2. Copia la carpeta de la skill en tu carpeta de skills de Claude Code:
   ```bash
   cp -R claude-skills/anti-ai-slop ~/.claude/skills/
   ```
   Cambia `anti-ai-slop` por el nombre de la skill que quieras.
3. Abre una sesión nueva de Claude Code y llámala por su nombre (`/anti-ai-slop`) o pídelo con tus palabras: "quita lo que suene a IA de este texto".

`substack-research` te preguntará la primera vez dónde tienes tus artículos publicados, tu guía de voz y tus casos. Si no tienes nada de eso, funciona igual con tu borrador y la web.

## Qué necesitas

- [Claude Code](https://claude.com/product/claude-code).
- Para el research web, una herramienta de búsqueda conectada (la búsqueda web de Claude Code o un conector como Firecrawl).

## Autor

Gerardo Colindres · Growth Product Manager. Escribo sobre producto, growth e IA en [Archivo.md](https://gerardocolindres.substack.com).

## Licencia

[MIT](LICENSE). Úsalas, cámbialas y compártelas.

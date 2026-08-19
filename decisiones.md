# Decisiones — TP1

## 1. Por qué Git no pudo resolver el conflicto solo

Git no pudo resolver el conflicto automáticamente porque las dos ramas habían modificado la misma línea del README de maneras diferentes (la rama A cambió el título a "versión A" y la rama B lo cambió a "versión B"). Como Git no puede decidir cuál de las dos versiones es la correcta —ninguna tiene más validez que la otra desde el punto de vista del historial—, hubo que resolver el conflicto manualmente eligiendo qué contenido dejar. Esto no hubiera pasado si las ramas no hubieran tocado la misma línea, o si se hubiera integrado una de las dos ramas a main antes de crear la segunda.

## 2. Problemas encontrados y cómo los solucioné

- **"Require approvals" tildado por defecto**: al activar la protección de rama, GitHub tilda automáticamente la casilla de "Require approvals" con el valor 1. Al principio no tenía claro por qué había que destildarlo para poder continuar; lo resolví entendiendo que, al ser un TP individual, GitHub no permite que el autor de un PR apruebe su propio PR, así que con esa casilla tildada nunca hubiera podido mergear nada.
- **Nombres automáticos de rama**: GitHub les puso nombres automáticos a las ramas (como `julietamelinsky01-patch-1`) en vez de usar la convención `feature/...` sugerida por la guía. Al principio pensé que estaba haciendo algo mal, pero entendí que pasa cuando se crea la rama desde el editor web en vez de por consola, y que no afecta el funcionamiento del TP.
- **Terminal que parecía trabada**: en algunos momentos, al pegar varios comandos juntos, la terminal parecía quedarse esperando sin dar respuesta. Lo solucioné con Ctrl+C para cancelar y volviendo a correr los comandos de a uno, esperando la respuesta de cada uno antes de seguir con el siguiente.

## 3. Declaración de uso de IA

Utilicé Claude (Anthropic) como asistente durante todo el desarrollo del TP1, guiándome paso a paso en la configuración de GitHub (protección de rama, creación de Pull Requests, resolución del conflicto de merge, tag y release).

Fui verificando las indicaciones a medida que avanzaba: ejecuté yo misma cada comando y miré el resultado que aparecía en la terminal antes de seguir con el siguiente paso. También revisé en GitHub que se hubieran creado las ramas, los cambios, los commits y los pull requests correctamente. Además, fui comparando lo que hacía con el enunciado del TP para asegurarme de que los pasos que estaba siguiendo cumplían con lo pedido.

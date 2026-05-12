# Paso 10. Medalla final container foundations

## Objetivo de aprendizaje

Este paso introduce un control de Container Security y debe dejar un cambio comprensible en docs/container-findings.md.

## Que vas a cambiar y por que

Actualiza docs/container-findings.md para que el control de "medalla final container foundations" quede explícito y revisable.

## Archivo y seccion que debes modificar

- Archivo objetivo: `docs/container-findings.md`.
- Aplícalo en la parte del archivo que corresponde al título del paso.
- Si el archivo aún no existe, créalo con este contenido inicial y luego evoluciona desde ahí en los siguientes pasos.

## Cambio base recomendado

Este bloque no es para pegar a ciegas: úsalo como punto de partida y ajústalo al contexto del repositorio.

```markdown
## Imagen analizada
## CVEs principales
## Riesgo operativo
## Siguiente accion
```

## Como adaptarlo correctamente

- Mantén el cambio pequeño y centrado en una sola idea por paso.
- Usa nombres claros para secciones, reglas o jobs.
- Evita añadir configuración que no esté relacionada con el objetivo del paso.

## Que deberia verse al terminar

- La intención del cambio se entiende leyendo el archivo.
- El archivo muestra el control sin depender de comentarios ambiguos.
- Los marcadores esperados del paso aparecen de forma natural en la configuración.

## Que valida el workflow automaticamente

- `validate-steps.yml` se ejecuta con `push`, `pull_request` y `workflow_dispatch`.
- `scripts/validate-step-10.py` comprueba este paso contra el archivo configurado.
- El workflow busca `## Imagen analizada` dentro de `docs/container-findings.md`.
- El workflow busca `## CVEs principales` dentro de `docs/container-findings.md`.
- El workflow busca `## Riesgo operativo` dentro de `docs/container-findings.md`.
- El workflow busca `## Siguiente accion` dentro de `docs/container-findings.md`.

## Criterio de finalizacion

El paso 10 queda completado cuando el workflow de GitHub Actions valida este cambio sin errores.

Este es el ultimo paso del tutorial.

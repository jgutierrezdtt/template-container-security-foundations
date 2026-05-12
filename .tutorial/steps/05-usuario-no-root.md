# Paso 5. Usuario no root

## Objetivo de aprendizaje

Ejecutar el contenedor como root amplía el impacto de cualquier compromiso del proceso. Este paso reduce privilegios en runtime.

## Que vas a cambiar y por que

Crea un usuario dedicado y cambia el `Dockerfile` para que la aplicación se ejecute con ese usuario no privilegiado.

## Archivo y seccion que debes modificar

- Archivo objetivo: `Dockerfile`.
- Aplícalo en la parte del archivo que corresponde al título del paso.
- Si el archivo aún no existe, créalo con este contenido inicial y luego evoluciona desde ahí en los siguientes pasos.

## Cambio base recomendado

Este bloque no es para pegar a ciegas: úsalo como punto de partida y ajústalo al contexto del repositorio.

```dockerfile
FROM python:3.11-slim
WORKDIR /app
COPY . .
RUN adduser --disabled-password --gecos "" appuser
USER appuser
CMD ["python", "app.py"]
```

## Como adaptarlo correctamente

- Crea el usuario después de copiar dependencias y antes del `CMD` final.
- Asegúrate de que el directorio de trabajo sigue siendo accesible para ese usuario.
- No mezcles este paso con hardening de imagen base; aquí el foco es el usuario efectivo del proceso.

## Que deberia verse al terminar

- El `Dockerfile` crea un usuario propio.
- La imagen termina con `USER appuser` o equivalente.
- No hay un retorno posterior a root en líneas siguientes.

## Que valida el workflow automaticamente

- `validate-steps.yml` se ejecuta con `push`, `pull_request` y `workflow_dispatch`.
- `scripts/validate-step-05.py` comprueba este paso contra el archivo configurado.
- El workflow busca `FROM python:3.11-slim` dentro de `Dockerfile`.
- El workflow busca `WORKDIR /app` dentro de `Dockerfile`.
- El workflow busca `USER appuser` dentro de `Dockerfile`.

## Criterio de finalizacion

El paso 5 queda completado cuando el workflow de GitHub Actions valida este cambio sin errores.

Siguiente paso: Paso 6.

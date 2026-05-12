# Container Security Foundations

Tutorial de fundamentos de seguridad en contenedores.

## Objetivo

Aprender los conceptos y herramientas esenciales para asegurar imágenes y workloads de contenedores: escaneo de vulnerabilidades, configuración segura, gestión de secretos y validación automatizada.

## Audiencia

Desarrolladores, ingenieros DevOps y equipos de plataforma que quieran incorporar seguridad en sus flujos de trabajo con contenedores desde el principio.

## Requisitos previos

- Conocimientos básicos de Git y GitHub.
- Nociones de Docker y contenedores.

## Herramientas utilizadas

- Trivy o herramienta de escaneo de imágenes equivalente
- GitHub Actions
- Scripts de validación del curso

## Inicio del tutorial

[![Empezar tutorial](https://img.shields.io/badge/Empezar%20tutorial-0b69ff?style=for-the-badge&logo=github&logoColor=white)](https://github.com/jgutierrezdtt/template-container-security-foundations/fork)

## Acceso al repositorio

- [Crear mi repositorio desde este template](https://github.com/new?template_name=template-container-security-foundations&template_owner=jgutierrezdtt)
- [Volver al portal general](https://github.com/jgutierrezdtt/security-learning-portal)

## Gestión del progreso

- [Validar progreso](../../actions/workflows/validate.yml)
- [Probar integridad del tutorial](../../actions/workflows/test-tutorial.yml)
- [Ejecutar tests funcionales del tutorial](../../actions/workflows/functional-tests.yml)
- [Reiniciar tutorial](../../actions/workflows/reset-tutorial.yml)
- [Ver pasos del tutorial](./.tutorial/steps/)

## Tabla de pasos

| Paso | Tema |
| --- | --- |
| 0 | Introducción |
| 1 | Imagen base insegura |
| 2 | Primer escaneo de imagen |
| 3 | Interpretación de CVE en imagen |
| 4 | Imagen base segura |
| 5 | Usuario no root |
| 6 | Gestión de secretos en contenedor |
| 7 | Dockerfile con buenas prácticas |
| 8 | Integración en GitHub Actions |
| 9 | Reporting básico |
| 10 | Medalla final Container Foundations |

## Paso 0

El paso 0 describe el entorno, permisos y limitaciones del laboratorio. No bloquea el flujo: el botón principal abre directamente el paso 1.

## Actualización desde template

Este repositorio incluye `.template-version` y workflow de actualización para revisar cambios del template sin sobrescribir trabajo del usuario.

## Badge final

Al cerrar el curso se generan artefactos de finalización en:

- `.tutorial/badges/completion-badge.md`
- `.tutorial/badges/completion-badge.svg`
- `.tutorial/evidence/completion.json`

## Referencias

- [Trivy](https://trivy.dev/)
- [GitHub Actions](https://docs.github.com/actions)
- [Docker security](https://docs.docker.com/engine/security/)

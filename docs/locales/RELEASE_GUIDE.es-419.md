# Guía de PCssak 0.8.0: acceso anticipado gratuito sin firma

[English README](../../README.md) · [Limitaciones conocidas](../KNOWN-LIMITATIONS.md) ·
[Estándar de archivos](../RELEASE_ASSET_STANDARD.md) · [Soporte](../../SUPPORT.md)

## Estado

Este cambio de documentación no publica etiquetas, Releases, ejecutables ni archivos
comprimidos. Cuando esté lista, la primera prueba pública aparecerá como GitHub
Prerelease para Windows x64.

- Versión: `0.8.0`
- Paquete: `PCSSAK_0.8.0_x64_Portable.zip`
- Formato: ZIP portátil sin instalador
- Firma: sin firma de forma intencional durante el acceso anticipado gratuito

Windows puede mostrar Editor desconocido, SmartScreen o alertas del antivirus. La firma,
la verificación del editor, la revisión legal externa, la reputación de SmartScreen y la
matriz completa de Windows están aplazadas y no son `PASS`.

## Antes de ejecutarlo

1. Descarga únicamente desde la página oficial Releases de este repositorio.
2. Confirma el nombre exacto y compara el SHA-256 con `SHA256SUMS.txt`.
3. No ejecutes archivos ausentes, renombrados o con un hash diferente.
4. Analiza el ZIP y la carpeta extraída; extrae solo en una carpeta de tu usuario.
5. Detente y reporta cualquier alerta o comportamiento cuyo origen no puedas verificar.

La búsqueda de actualizaciones se inicia solo cuando la solicitas y abre la página
oficial. PCssak no descarga, ejecuta, instala ni revierte el paquete automáticamente.

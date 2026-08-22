# Guía de PCssak 0.8.0: acceso anticipado gratuito sin firma

[English README](../../README.md) · [Limitaciones conocidas](../KNOWN-LIMITATIONS.md) ·
[Estándar de archivos](../RELEASE_ASSET_STANDARD.md) · [Soporte](../../SUPPORT.md)

## Estado

La primera prueba pública ya está disponible como GitHub Prerelease inmutable
[v0.8.0](https://github.com/pcssakinc/pcssak-pc-optimizer-releases/releases/tag/v0.8.0)
para Windows x64.

- Versión: `0.8.0`
- Paquete: `PCSSAK_0.8.0_x64_Portable.zip`
- Formato: ZIP portátil sin instalador
- Firma: sin firma de forma intencionada durante el acceso anticipado gratuito
- SHA-256: `88d9e2012b329242ab2903268f46ec5b4a6f69d06582d262cf706704cd0406aa`

Windows puede mostrar Editor desconocido, SmartScreen o avisos del antivirus. La firma,
la verificación del editor, la revisión jurídica externa, la reputación de SmartScreen y
la matriz completa de Windows están aplazadas y no son `PASS`.

## Antes de ejecutarlo

1. Descargue únicamente desde la página oficial Releases de este repositorio.
2. Confirme el nombre exacto y compare el SHA-256 con `SHA256SUMS.txt`.
3. No ejecute archivos ausentes, renombrados o con un hash diferente.
4. Analice el ZIP y la carpeta extraída; extraiga solo en una carpeta de su usuario.
5. Deténgase e informe de avisos o comportamientos cuyo origen no pueda verificar.

Cuando el usuario pulsa **Buscar actualizaciones**, PCssak muestra el estado. Si existe
una versión nueva, el usuario puede pulsar por separado el botón de la página oficial
de descarga. La página no se abre automáticamente y PCssak no descarga, ejecuta,
instala ni revierte el paquete automáticamente.

Comunique defectos reproducibles que no sean de seguridad mediante
[GitHub Issues](https://github.com/pcssakinc/pcssak-pc-optimizer-releases/issues),
después de eliminar datos privados. Para vulnerabilidades explotables, utilice la
[vía de seguridad privada](../../SECURITY.md), no un Issue público.

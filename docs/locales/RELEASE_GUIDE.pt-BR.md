# Guia do PCssak 0.8.0: acesso antecipado gratuito sem assinatura

[English README](../../README.md) · [Limitações conhecidas](../KNOWN-LIMITATIONS.md) ·
[Padrão de arquivos](../RELEASE_ASSET_STANDARD.md) · [Suporte](../../SUPPORT.md)

## Status

Esta alteração de documentação não publica tag, Release, executável nem arquivo
compactado. Quando estiver pronto, o primeiro teste público será disponibilizado como
GitHub Prerelease para Windows x64.

- Versão: `0.8.0`
- Pacote: `PCSSAK_0.8.0_x64_Portable.zip`
- Formato: ZIP portátil sem instalador
- Assinatura: intencionalmente sem assinatura no acesso antecipado gratuito

O Windows pode mostrar Editor desconhecido, SmartScreen ou alertas do antivírus. A
assinatura, a validação do editor, a revisão jurídica externa, a reputação do SmartScreen
e a matriz completa do Windows foram adiadas e não são `PASS`.

## Antes de executar

1. Baixe somente pela página oficial Releases deste repositório.
2. Confirme o nome exato e compare o SHA-256 com `SHA256SUMS.txt`.
3. Não execute arquivo ausente, renomeado ou com hash diferente.
4. Verifique o ZIP e a pasta extraída; extraia somente em uma pasta do seu usuário.
5. Interrompa e informe alertas ou comportamentos cuja origem não possa ser verificada.

Quando o usuário pressiona **Verificar atualizações**, o PCssak mostra o status. Se
houver uma versão nova, o usuário poderá pressionar separadamente o botão da página
oficial de download. A página não abre automaticamente e o PCssak não baixa, executa,
instala nem reverte o pacote automaticamente.

Relate defeitos reproduzíveis que não sejam de segurança por meio do
[GitHub Issues](https://github.com/pcssakinc/pcssak-pc-optimizer-releases/issues),
depois de remover dados privados. Para vulnerabilidades exploráveis, use o
[canal de segurança privado](../../SECURITY.md), não uma Issue pública.

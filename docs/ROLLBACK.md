# Rollback

## Antes da Fase 1

Existe backup completo do Home Assistant concluído antes das alterações do projeto.

## Rollback simples

Se Codex Assist causar problema:

1. Remover Codex Assist da pipeline Assist.
2. Desabilitar/remover a integração Codex Assist em Settings → Devices & services.
3. Remover a integração pelo HACS, se necessário.
4. Reiniciar o Home Assistant.

## Rollback completo

Se houver impacto além da integração, restaurar o backup completo criado antes da Fase 1.

Nenhum rollback deste projeto deve tocar nos arquivos ou componentes do APT0307/Digital Twin.

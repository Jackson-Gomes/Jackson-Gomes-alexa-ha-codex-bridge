# Fase 1 — Codex Assist no Home Assistant

## Ambiente validado

- HAOS 18.2
- Home Assistant Core 2026.9.2
- Supervisor 2026.09.2
- arquitetura amd64
- HACS carregado
- Core e Supervisor saudáveis
- entidade de teste: `light.luz_do_escritorio`

## Integração escolhida

`itsreverence/ha-codex-assist`

Versão atual verificada em 2026-09-18: `v0.4.5`.

Motivos:

- Conversation Agent nativo do Assist;
- autenticação ChatGPT/Codex por Device Code;
- sem OpenAI API key;
- HA 2026.6+;
- compatível com mudanças do HA 2026.9 a partir de 0.4.4;
- controle via Assist LLM API;
- contexto/follow-up;
- segurança baseada em entidades expostas ao Assist.

## Limite inicial

Expor ao Assist somente:

```text
light.luz_do_escritorio
```

Não expor Supervisor, shell, arquivos, backups, add-ons, administração, locks, alarmes, garagem, válvulas nem recursos do APT0307.

## Testes

1. `Qual o estado da luz do escritório?`
2. `Acenda a luz do escritório.`
3. Confirmar estado real de `light.luz_do_escritorio` via Home Assistant.
4. Na mesma conversa: `Apague ela.`
5. Confirmar resolução contextual e estado final.

## Autenticação

A autenticação deve ser concluída pelo usuário diretamente no fluxo Device Code. Nunca registrar ou compartilhar senha, cookie, access token, refresh token ou OAuth secret.

# Instalação — Fase 1

## Pré-requisitos verificados

- Home Assistant 2026.6.0 ou superior
- HACS
- conta ChatGPT com acesso ao Codex

## Codex Assist

1. Home Assistant → HACS → Integrations.
2. Procurar `Codex Assist`.
3. Instalar a versão estável atual (`v0.4.5` verificada em 2026-09-18).
4. Reiniciar o Home Assistant.
5. No ChatGPT, habilitar `Settings → Security → Enable device code authorization for Codex`, se disponível na conta.
6. Home Assistant → Settings → Devices & services → Add integration → `Codex Assist`.
7. Concluir autenticação por Device Code diretamente no navegador do usuário.
8. Selecionar Codex Assist como Conversation Agent na pipeline Assist.

## Regra

Não configurar OpenAI API key em nenhuma etapa.

# Troubleshooting

## Codex Assist não aparece no HACS

Atualize os dados do HACS e procure novamente por `Codex Assist`. O projeto está no catálogo padrão do HACS.

## Erros em Home Assistant 2026.9

Use Codex Assist 0.4.4 ou superior. A versão estável verificada em 2026-09-18 é 0.4.5.

Sintomas corrigidos a partir de 0.4.4 incluem falhas envolvendo `voluptuous_openapi` e `_Unsupported`.

## Falha de autenticação

- confirme acesso ao Codex na conta ChatGPT;
- confirme que Device Code authorization está habilitado em ChatGPT → Settings → Security, quando essa opção estiver disponível;
- refaça o fluxo Device Code;
- nunca copie tokens/cookies para logs ou issues.

## Entidade não pode ser controlada

Confirme que a entidade está explicitamente exposta ao Assist e que a pipeline usa Codex Assist como Conversation Agent.

## Backend Codex mudou

O projeto depende de uma interface downstream do Codex que não é um contrato público estável. Uma atualização upstream pode quebrar temporariamente o agente mesmo sem mudança no Home Assistant.

# Testes

## Smoke test da Fase 1

Estado inicial deve ser registrado pelo Home Assistant.

### Teste A — leitura

Pergunta no Assist:

`Qual o estado da luz do escritório?`

Esperado: resposta coerente com `light.luz_do_escritorio`.

### Teste B — ação

Comando no Assist:

`Acenda a luz do escritório.`

Esperado:

- Codex Assist usa ferramentas nativas do Assist;
- `light.luz_do_escritorio` muda para `on`;
- o estado real é validado separadamente pelo Home Assistant.

### Teste C — contexto

Na mesma conversa:

`Apague ela.`

Esperado: `ela` refere-se à luz do escritório e a entidade retorna a `off`.

## Critério de aprovação

A Fase 1 só é considerada validada se o estado real da entidade confirmar as ações e nenhuma entidade fora do escopo inicial estiver exposta ao agente.

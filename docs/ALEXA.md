# Alexa Skill — fases posteriores

A camada Alexa só será implementada após validar o Conversation Agent no Home Assistant.

## UX alvo

```text
Usuário: Alexa, abrir Casa.
Alexa: Pode falar.
Usuário: Acenda a luz do escritório.
Alexa → bridge → Home Assistant Assist → Codex Assist → entidade
Alexa: Luz do escritório ligada.
```

## Diretrizes

- usar uma Custom Skill;
- privilegiar linguagem livre em vez de centenas de intents;
- avaliar `AMAZON.SearchQuery` para pt-BR no momento da implementação;
- preservar contexto de conversa para follow-ups como `Apague ela.`;
- não transformar a skill em ponte administrativa do Home Assistant.

# Arquitetura

## Fluxo alvo

```text
Echo/Alexa
  ↓
Alexa Custom Skill
  ↓
Alexa bridge
  ↓
Home Assistant Conversation/Assist
  ↓
Codex Assist (Conversation Agent)
  ↓
Home Assistant Assist LLM API
  ↓
Entidades expostas ao Assist
  ↓
Casa

Resposta:
Codex Assist → Home Assistant → Alexa Skill response → Echo/TTS
```

## Princípios

1. Home Assistant é a autoridade de dispositivos e exposição.
2. Codex Assist não recebe uma ponte genérica de `call_service`.
3. O primeiro protótipo expõe somente `light.luz_do_escritorio`.
4. A camada Alexa será adicionada apenas depois que o fluxo Assist → Codex → entidade estiver validado.
5. Não existe dependência do projeto APTO0307/Digital Twin.

## Risco técnico conhecido

O `ha-codex-assist` usa autenticação da conta ChatGPT/Codex, mas depende de uma interface downstream do Codex que não é um contrato público estável para terceiros. Atualizações upstream podem exigir manutenção futura.

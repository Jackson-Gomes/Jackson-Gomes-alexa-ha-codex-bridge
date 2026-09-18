# Alexa → Home Assistant → Codex Bridge

Projeto independente para usar dispositivos Echo/Alexa como interface de voz enquanto Home Assistant Assist + Codex atuam como cérebro conversacional e de automação.

## Objetivo

```text
Echo/Alexa
↓
Alexa Custom Skill
↓
Alexa bridge
↓
Home Assistant Conversation/Assist
↓
Codex Conversation Agent
↓
Assist tools
↓
Home Assistant entities
↓
Casa

Resposta:
Codex → Home Assistant → Alexa Skill response → Echo/TTS
```

## Requisito fundamental

- Não usar OpenAI API paga.
- Preferir autenticação ChatGPT/Codex por OAuth / Device Code, quando tecnicamente disponível.
- Não configurar OpenAI API key como fallback.

## Fase atual

Fase 1: instalar e validar `itsreverence/ha-codex-assist` como Conversation Agent nativo do Home Assistant Assist.

Entidade inicial permitida:

```text
light.luz_do_escritorio
```

## Segurança

No protótipo inicial, o limite de controle deve ser o mecanismo normal de entidades expostas ao Assist. Não expor Supervisor, shell, configuração, backups, add-ons, arquivos, locks, alarmes, garagem, válvulas ou qualquer componente do projeto APT0307/Digital Twin.

## Isolamento do projeto

Este repositório é independente de `APTO307-Digital-Twin` e não deve modificar:

- `/config/www/apto3d/`
- `/config/custom_components/apto3d/`
- dashboard 3D
- DIAMANTE RGB
- ROBOTTEST

## Documentação

Consulte `docs/` para arquitetura, autenticação, instalação, segurança, testes, troubleshooting, rollback e futura integração Alexa.

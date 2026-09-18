# Segurança

## Boundary de controle

A segurança da Fase 1 depende do mecanismo oficial de exposição do Home Assistant Assist. O Codex Assist deve enxergar/controlar somente entidades explicitamente expostas ao Assist.

Entidade permitida no primeiro protótipo:

```text
light.luz_do_escritorio
```

## Não permitido

- Supervisor
- shell/terminal
- configuração administrativa
- backups
- instalação de add-ons
- escrita de arquivos
- locks
- alarmes
- garagem
- válvulas
- recursos do APT0307/Digital Twin

## Credenciais

Nunca armazenar no repositório:

- senha ChatGPT/OpenAI
- cookies
- access tokens
- refresh tokens
- OAuth secrets
- device codes

O Device Code deve ser consumido diretamente pelo usuário no fluxo oficial de autenticação.

## OpenAI API

Não configurar OpenAI API key como fallback. Caso uma alternativa passe a exigir API paga, ela fica fora deste projeto.

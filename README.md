# Aura Support AI

> Consumidores odeiam esperar horas por atendimento humano e ficam frustrados com robôs burros que não conseguem resolver problemas práticos sem transferir a ligação.

[![Autor: Bruno Dyas](https://img.shields.io/badge/autor-Bruno%20Dyas-2563eb?style=for-the-badge)](https://github.com/brunodyas)
[![Stack](https://img.shields.io/badge/stack-next-fullstack-059669?style=for-the-badge)](#stack-tecnológica)
[![Status](https://img.shields.io/badge/progresso-9%2F25-7c3aed?style=for-the-badge)](#sobre-o-projeto)

## Sobre o projeto

O mercado de atendimento ao cliente está saturado de chatbots baseados em regras simples que frustram os usuários. As empresas precisam de agentes de IA autônomos que não apenas respondam perguntas, mas resolvam problemas reais executando ações via API (como estornos, agendamentos e consultas a bancos de dados) de forma segura.

## Funcionalidades e melhorias

- Engine de Agentic Tool-Use: Integração com LangGraph para permitir que a IA execute chamadas de API externas (ex: Stripe, Shopify) de forma autônoma.
- Painel de Guardrails & Human-in-the-Loop: Interface administrativa para agentes humanos aprovarem ou rejeitarem ações de alto risco propostas pela IA antes de serem executadas.
- Análise de Sentimento e Escala preditiva: Algoritmo que detecta frustração em tempo real e prioriza automaticamente o transbordo para humanos com o histórico completo resumido pela IA.
- Transformação do aplicativo móvel em um painel de controle de Agentes Autônomos (Agentic AI).
- Implementação de um sistema de 'Human-in-the-loop' (HITL) para aprovação de ações transacionais críticas (estornos, agendamentos, alterações cadastrais) propostas por agentes de IA.
- Integração de um gateway de IA (Next.js) que intercepta mensagens, analisa sentimentos e gera resumos preditivos de frustração do cliente.
- Sistema de Guardrails de segurança em tempo real para evitar injeção de prompt e vazamento de dados sensíveis (PII) antes de enviar dados para LLMs.
- Notificações push inteligentes com resumos executivos gerados por IA e botões de ação rápida diretamente na tela de bloqueio do dispositivo móvel.

## Diferencial

Transformar o helpdesk tradicional em uma plataforma de agentes autônomos que executam tarefas transacionais com validação humana.

## Stack tecnológica

- **Perfil:** Next · Fullstack
- **Repositório:** [`aura-support-ai-a71eb3`](https://github.com/brunodyas/aura-support-ai-a71eb3)
- **Baseline OSS:** [chatwoot-mobile-app](https://github.com/chatwoot/chatwoot-mobile-app)

### Arquitetura

{'mobile_client': 'React Native (TypeScript) com Zustand para gerenciamento de estado local e conexões WebSocket seguras.', 'agentic_gateway': 'Next.js (App Router) atuando como middleware inteligente entre o app móvel, a API do Chatwoot e provedores de LLM (OpenAI/Anthropic).', 'database_and_cache': 'PostgreSQL para persistência de logs de auditoria de IA e Redis para gerenciamento de filas de aprovação em tempo real (HITL).', 'security_layer': 'LlamaGuard e filtros regex customizados para sanitização de inputs/outputs (Guardrails).'}

## Pré-requisitos

- Git

## Instalação

```bash
git clone https://github.com/brunodyas/aura-support-ai-a71eb3.git
cd aura-support-ai-a71eb3
npm install
npm run dev  # ou npm start
```

## Como executar

1. Conclua a instalação acima.
2. Configure variáveis de ambiente (`.env` ou `.env.example`, se existir).
3. Execute o comando de desenvolvimento ou suba os containers Docker.
4. Valide health/API antes de expor em produção.

## Variáveis de ambiente

- Copie `.env.example` para `.env` quando disponível.
- Nunca commite segredos reais (tokens, senhas, chaves privadas).

## Testes

```bash
# Node.js
npm test

# Python
pytest -q

# .NET
dotnet test

# Java
mvn test
```

> Use o comando compatível com a stack detectada neste repositório.

## Estrutura do repositório

```text
.
├── client/          # Frontend (quando aplicável)
├── server/          # Backend / API (quando aplicável)
├── src/             # Código principal
├── tests/           # Testes automatizados
├── docker-compose.yml
└── README.md
```

## Roadmap

- Refinar observabilidade (logs estruturados, métricas e alertas).
- Endurecer segurança (auth, rate limit, secrets management).
- Expandir cobertura de testes e automação de deploy.

## Licença

Consulte o arquivo `LICENSE` incluído neste repositório.

---

**Desenvolvido por [Bruno Dyas](https://github.com/brunodyas)**

Entrega produzida pela fábrica autónoma **Djenus** — engenharia de software orientada a produto.

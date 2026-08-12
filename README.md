# Mentor de Carreira em Tecnologia - Baseado em 2 Agentes Especializados

*Mentor de Carreira em Tecnologia baseado em dois agentes especializados*

![Prompt Engineering](https://img.shields.io/badge/AI-Prompt%20Engineering-8A2BE2)
![AI Agents](https://img.shields.io/badge/AI-Agent%20Design-412991)
![Generative AI](https://img.shields.io/badge/Generative%20AI-Career%20Mentor-6C63FF)
![GitHub Copilot](https://img.shields.io/badge/GitHub-Copilot-000000?logo=githubcopilot&logoColor=white)
![DIO](https://img.shields.io/badge/DIO-CI%26T%20Bootcamp-5A0FC8)
![Status](https://img.shields.io/badge/Status-Protótipo-blue)

O **AI Career Mentor** é um protótipo de sistema baseado em agentes de IA criado
para apoiar decisões relacionadas à carreira em tecnologia.

A solução utiliza **Prompt Engineering e separação de responsabilidades entre
agentes especializados** para estruturar um processo de mentoria em duas etapas:

**Diagnóstico do perfil → Planejamento de carreira**

O projeto foi desenvolvido durante o curso **Introdução à Engenharia de Prompt**,
integrante do Bootcamp **CI&T — Do Prompt ao Agente**, da DIO.

---

## 🎯 Objetivo

Construir um sistema de mentoria capaz de :

- Compreender o perfil do usuário
- Identificar interesses profissionais
- Considerar experiência e conhecimentos atuais
- Avaliar disponibilidade para aprendizado
- Identificar áreas de interesse
- Sugerir possíveis caminhos profissionais
- Estruturar um roadmap de desenvolvimento
- Propor ações para evolução profissional

O foco do projeto está no **design dos agentes e na engenharia das instruções**,
e não na implementação de uma aplicação automatizada.

---

## 🧠 Conceito

Em vez de utilizar um único prompt para executar todo o processo, o sistema divide
a tarefa entre **dois agentes especializados**.

```text
Usuário
   ↓
🧩 Agente Entrevistador
   ↓
Coleta estruturada de informações
   ↓
Perfil do Usuário
   ↓
🧠 Agente Planejador
   ↓
Análise do Perfil
   ↓
Recomendações
   ↓
Roadmap de Carreira
```

Essa separação permite que cada agente tenha **objetivo, responsabilidade, entrada
e saída claramente definidos**.

---

## 🏗️ Arquitetura Visual

A arquitetura organiza o processo de mentoria em dois agentes especializados,
com responsabilidades distintas e transferência estruturada de contexto entre as etapas.

<img width="800" height="400" alt="ChatGPT Image 12 de ago  de 2026, 18_46_24" src="https://github.com/user-attachments/assets/4120049e-7aa7-4901-a924-74334a9e07c9" />

O fluxo parte da coleta estruturada de informações pelo **Agente Entrevistador**,
passa pela construção do **Perfil Estruturado** e segue para o **Agente Planejador**,
responsável pela geração do plano de desenvolvimento profissional.

---

## Arquitetura dos Agentes

🧩 Agente 1 — Entrevistador de Carreira

Responsável pela etapa de **descoberta e diagnóstico**.

O agente conduz uma entrevista estruturada para compreender aspectos relevantes
do perfil profissional.

Informações investigadas

- Área de interesse
- Experiência atual
- Conhecimentos técnicos
- Preferências profissionais
- Disponibilidade para estudo
- Objetivos de carreira
- Interesse em áreas específicas

Entrada

Respostas fornecidas pelo usuário durante a entrevista.

Saída

Um **perfil estruturado**, preparado para ser utilizado pelo segundo agente.

---

## 🧠 Agente 2 — Planejador de Carreira

Responsável por transformar o perfil produzido pelo primeiro agente em um
**plano de desenvolvimento profissional**.

Processamento

O agente considera informações como:

- Preferências
- Experiência
- Objetivos
- Disponibilidade
- Áreas de interesse

Saída esperada

O planejamento pode incluir:

- Ranking de possíveis carreiras
- Recomendações de aprendizado
- Roadmap
- Sugestões de projetos para portfólio
- Preparação para entrevistas

---

## 🔄 Fluxo Multiagente

```text
┌──────────────────────────────┐
│           USUÁRIO            │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│    AGENTE ENTREVISTADOR      │
│                              │
│ • Interesses                 │
│ • Experiência                │
│ • Objetivos                  │
│ • Disponibilidade            │
│ • Preferências               │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│      PERFIL ESTRUTURADO      │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│      AGENTE PLANEJADOR       │
│                              │
│ • Analisa perfil             │
│ • Identifica caminhos        │
│ • Prioriza possibilidades    │
│ • Estrutura ações            │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│      PLANO DE CARREIRA       │
│                              │
│ • Carreiras sugeridas        │
│ • Roadmap                    │
│ • Projetos                   │
│ • Próximos passos            │
└──────────────────────────────┘
```

---

## ⚙️ Princípios de Design

1. Separação de Responsabilidades

Cada agente executa uma função específica:

**Entrevistador → coleta e estrutura**

**Planejador → analisa e recomenda**

2. Contexto Estruturado

O resultado da primeira etapa é utilizado como contexto para a segunda, reduzindo
a necessidade de o agente planejador reconstruir todas as informações.

3. Modularidade

A arquitetura permite que os agentes sejam modificados ou reutilizados
individualmente.

4. Extensibilidade

Novos agentes poderiam ser incorporados posteriormente:

```text
Entrevistador
     ↓
Planejador
     ↓
Avaliador Técnico
     ↓
Gerador de Roadmap
     ↓
Preparador de Entrevistas
```

---

## 🧪 Exemplo Conceitual

Perfil

```text
Interesse principal: Dados
Nível: Iniciante / Intermediário
Disponibilidade: 4 horas por semana
Objetivo: Transição de carreira
Interesse adicional: Inteligência Artificial
```

Possíveis caminhos avaliados

```text
→ Analista de Dados
→ Cientista de Dados
→ Machine Learning
```

A partir dessas informações, o agente planejador estrutura recomendações e um
possível caminho de desenvolvimento.

> As recomendações produzidas pelo modelo devem ser interpretadas como apoio à
> reflexão e planejamento, e não como garantia de adequação ou resultado profissional.

---

## 🛠️ Conceitos Aplicados

**Prompt Engineering** - Estruturação das instruções dos agentes

**Agent Design** - Definição de responsabilidades

**Context Engineering** - Transferência estruturada de informações

**Generative AI** - Geração e análise das respostas

**Decision Support** - Apoio ao planejamento

**Modular Design** - Separação das etapas do sistema

---

## 📂 Estrutura Atual

```text
Copilot-Prompts/
│
├── prompts/
│   ├── AGENTE-1-Entrevistador-de-Carreira.md
│   └── AGENTE-2-Planejador-de-Carreira.md
│
├── AGENTE 1 - Entrevistador de Carreira em Tecnologia.docx
├── AGENTE 2 - Planejador de Carreira em Tecnologia.docx
├── README.md
└── ...
```

Agente 1

`AGENTE 1 - Entrevistador de Carreira em Tecnologia.docx`

Contém a estrutura do agente responsável pela entrevista e diagnóstico.

Agente 2

`AGENTE 2 - Planejador de Carreira em Tecnologia.docx`

Contém a estrutura do agente responsável pela análise e planejamento.

---

## 💡 Competências Demonstradas

- Prompt Engineering
- Generative AI
- AI Agent Design
- Context Engineering
- Decomposição de problemas
- Estruturação de prompts
- Design de fluxos conversacionais
- Sistemas de apoio à decisão
- Arquitetura modular de agentes
- GitHub

---

## 🚀 Possíveis Evoluções

O protótipo pode evoluir para uma aplicação completa incorporando:

- Interface web
- Streamlit
- Integração com API de LLM
- Automação do fluxo entre agentes
- Persistência do perfil
- Scoring de competências
- Avaliação técnica
- Geração automática de roadmap
- Recomendações de cursos
- Análise de currículo
- Preparação para entrevistas
- Histórico de evolução
- Avaliação das respostas dos agentes

Uma arquitetura futura poderia assumir o formato:

```text
Interface
   ↓
Orquestrador
   ↓
Entrevistador
   ↓
Perfil estruturado
   ↓
Planejador
   ↓
Ferramentas / Bases externas
   ↓
Plano de desenvolvimento
```

---

## ⚠️ Escopo

Este projeto é um **protótipo baseado em Prompt Engineering**.

A arquitetura representa conceitualmente um sistema de agentes, mas o fluxo entre
os agentes **não está automatizado por software nesta versão**.

O projeto tem finalidade educacional e demonstrativa.

---

## 🎓 Contexto Acadêmico

Projeto desenvolvido no curso **Introdução à Engenharia de Prompt**, integrante
do Bootcamp:

**CI&T — Do Prompt ao Agente | DIO**

O desafio teve como foco a aplicação prática de conceitos de Prompt Engineering
na construção de soluções estruturadas com Inteligência Artificial Generativa.

---

## 🤝 Como Contribuir

Contribuições são bem-vindas especialmente nas áreas de:

- Prompt Engineering
- Agent Design
- Context Engineering
- Avaliação de prompts
- Automação de agentes
- UX conversacional

1. Faça um Fork do projeto
2. Crie uma branch para sua melhoria
3. Implemente e documente a alteração
4. Faça o commit
5. Envie a branch
6. Abra um Pull Request

---

## 👨‍💻 Autor

**Marcus Guedes**

Marketing | Data Science | Inteligência Artificial | Gestão de Projetos

GitHub: MCLG1661  

LinkedIn: Marcus Guedes

---

🤖 **Do prompt ao agente: estruturando IA Generativa para apoiar decisões de carreira.**


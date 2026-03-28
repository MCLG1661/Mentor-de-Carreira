# 🤖 Copilot - Prompts IA Mentor de Carreira em Tecnologia 

Este projeto foi desenvolvido como parte do bootcamp "Do Prompt ao Agente" da DIO, com o objetivo de criar um sistema baseado em prompts que funcione como um agente inteligente de apoio à decisão de carreira.
Os agentes foram projetados de forma modular, permitindo reutilização e adaptação para diferentes perfis de usuários.

![DIO](https://img.shields.io/badge/DIO-Bootcamp-blueviolet)

---

# 🎯 Objetivo

![Project](https://img.shields.io/badge/Project-AI%20Career%20Mentor-black)
![Status](https://img.shields.io/badge/Status-In%20Progress-yellow)

Criar um mentor de carreira em tecnologia capaz de :

- Entender o perfil do usuário
- Identificar interesses e nível de experiência
- Sugerir caminhos profissionais
- Gerar um plano de ação estruturado

---

# 💡 Diferencial do Projeto

Este projeto vai além de um prompt simples :

```
✔️ Possui fluxo estruturado
✔️ Simula um processo real de mentoria
✔️ Gera valor prático (plano acionável)
✔️ Pode ser expandido para um agente automatizado
```
---

 # 🛠️ Tecnologias e Conceitos Utilizados

![Python](https://img.shields.io/badge/Python-Data%20Science-blue)
![SQL](https://img.shields.io/badge/SQL-Analytics-orange)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-AI-green)
![Prompt Engineering](https://img.shields.io/badge/Prompt%20Engineering-LLM-purple)

- Engenharia de Prompt
- Estruturação de agentes conversacionais
- Lógica de decisão baseada em respostas
- Planejamento de carreira em tecnologia
- GitHub como portfólio

# 📂 Estrutura do Projeto

```
ia-mentor-carreira/
│
├── prompts/
│   ├── agente-entrevistador.txt
│   └── agente-planejador.txt
│
├── examples/
│   └── exemplo-uso.md
│
└── README.md
``` 

O sistema foi dividido em dois agentes complementares:

🧩 Agente 1 — Entrevistador de Carreira

Responsável por coletar informações do usuário através de perguntas estratégicas.

🧠 Agente 2 — Planejador de Carreira

Responsável por analisar as respostas e gerar recomendações personalizadas.

---

# Exemplo-uso.md

### Entrada (resumida)

- Interesse: dados
- Nível: iniciante/intermediário
- Tempo: 4h/semana
- Objetivo: transição de carreira
- Interesse: IA

### Saída esperada

- Cientista de Dados
- Engenheiro de Machine Learning
- Analista de Dados

---

# 📄 docs/arquitetura.md

Este projeto foi estruturado como um sistema de agentes em duas etapas, simulando um fluxo real de mentoria de carreira :

1. Coleta de informações (diagnóstico)
2. Análise e recomendação (planejamento)

A separação em dois agentes permite maior modularidade, reutilização e clareza na lógica de decisão.

---

## Estrutura dos Agentes

### 🧩 Agente 1 — Entrevistador

Responsável por coletar informações do usuário de forma estruturada.

**Função principal :**
- Extrair dados relevantes para análise de carreira

**Tipo de processamento :**
- Input guiado (perguntas sequenciais)

**Saída :**
- Perfil estruturado do usuário

Exemplo de saída :

PERFIL DO USUÁRIO:

Interesse principal : dados
Nível atual : iniciante/intermediário
Disponibilidade : 4h/semana
Preferência : dados
Objetivo : transição de carreira
Áreas de interesse : IA
Experiência prévia : cursos em plataformas online

### 🧠 Agente 2 — Planejador

Responsável por interpretar o perfil e gerar recomendações.

**Função principal :**
- Transformar dados em decisão

**Tipo de processamento :**
- Análise + geração de conteúdo estruturado

**Saída :**
- Ranking de carreiras
- Roadmap de aprendizado
- Projeto de portfólio
- Preparação para entrevistas

### 🔄 Fluxo do Sistema

```
Usuário
↓
Agente 1 (Entrevista)
↓
Perfil estruturado
↓
Agente 2 (Planejamento)
↓
Plano de carreira personalizado
```

### Lógica de Decisão

O sistema utiliza regras implícitas baseadas em :

- Preferência do usuário (dados, código, pessoas)
- Interesse em áreas específicas (ex: IA)
- Tempo disponível
- Objetivo de carreira

### Exemplo :

Se:
- Interesse = dados
- Interesse adicional = IA

Então:
→ Priorizar carreiras como:
- Cientista de Dados
- Engenheiro de Machine Learning

### ⚙️ Princípios de Design

### 1. Separação de responsabilidades

Cada agente possui uma função clara :

- Um coleta dados
- Outro toma decisões

### 2. Reutilização
Os agentes podem ser usados separadamente em outros contextos.

### 3. Escalabilidade

A arquitetura permite :

- Adição de novos agentes (ex: avaliador técnico)
- Integração com APIs de IA
- Automação completa do fluxo

### 4. Clareza de saída

As respostas são estruturadas para facilitar :

- leitura
- interpretação
- tomada de decisão

---

## 🚀 Possíveis Evoluções

- Transformar em aplicação com interface (Streamlit)
- Automatizar fluxo entre agentes
- Integrar com APIs de LLM (ex: OpenAI)
- Adicionar scoring automático de perfil

---

## 📊 Conclusão

Este projeto demonstra como a engenharia de prompts pode ser utilizada para criar soluções práticas e orientadas a decisão, simulando o comportamento de um agente inteligente.
A arquitetura foi pensada para simular um processo real de mentoria, utilizando princípios de engenharia de prompts para criar um sistema modular, escalável e orientado à decisão.

---

# 📌 Possíveis Evoluções

- Transformar em aplicação web (Streamlit)
- Integrar com API de IA
- Criar interface interativa
- Adicionar scoring automático de perfil

---

# 👨‍💻 Autor

Marcus Guedes : 

Profissional com atuação em Marketing e Data Science, com foco em transição para áreas de dados e inteligência artificial.

GitHub: https://github.com/MCLG1661 LinkedIn: https://www.linkedin.com/in/marcusguedes

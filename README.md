<div align="center">

# Miniguia de Estudos: Engenharia e Arquitetura de Dados

### Um Caderno Temático construído com NotebookLM como ferramenta de aprendizagem ativa

[![DIO](https://img.shields.io/badge/DIO-Desafio%20de%20Projeto-red)](https://www.dio.me/)
[![NotebookLM](https://img.shields.io/badge/IA-NotebookLM-blue)](https://notebooklm.google/)
[![Status](https://img.shields.io/badge/status-conclu%C3%ADdo-brightgreen)]()
[![License](https://img.shields.io/badge/license-MIT-lightgrey)]()

</div>

---

## Sobre o projeto

Este repositório documenta a construção de um **Caderno Temático no NotebookLM** sobre **Engenharia e Arquitetura de Dados**, desenvolvido como desafio de projeto da [DIO](https://www.dio.me/). O objetivo não é apenas apresentar um resumo do tema, mas registrar todo o processo de estudo: curadoria de fontes, engenharia de prompts, dificuldades encontradas e o material final consolidado — evidenciando pensamento crítico no uso de IA como ferramenta de aprendizagem, e não como atalho.

## Sumário

- [1. Contexto e Objetivos](#1-contexto-e-objetivos)
- [2. Curadoria de Fontes](#2-curadoria-de-fontes)
- [3. Engenharia de Prompts e Troubleshooting](#3-engenharia-de-prompts-e-troubleshooting)
- [4. Miniguia de Estudo — Entrega Final](#4-miniguia-de-estudo--entrega-final)
  - [4.1 Resumos Estruturados](#41-resumos-estruturados)
  - [4.2 Glossário](#42-glossário)
  - [4.3 Prompts Reutilizáveis](#43-prompts-reutilizáveis)
- [Estrutura do Repositório](#estrutura-do-repositório)
- [Conclusão](#conclusão)

---

## 1. Contexto e Objetivos

### Contexto

A área de **Engenharia de Dados** está entre as que mais crescem no mercado de tecnologia, sustentando praticamente todo o ecossistema de Analytics, Ciência de Dados e Inteligência Artificial. Apesar da relevância, é um campo que muda rápido: em poucos anos passamos de Data Warehouses monolíticos para Data Lakes, Lakehouses e arquiteturas descentralizadas como o Data Mesh. Escolhi esse assunto porque é o núcleo da minha trilha de estudos atual, e porque entender **arquitetura** — não apenas ferramentas — é o que diferencia um profissional júnior de alguém capaz de tomar decisões técnicas.

### Objetivos de estudo

| # | Objetivo |
|---|----------|
| 1 | Consolidar os **conceitos fundamentais** do ciclo de vida da engenharia de dados (geração, ingestão, armazenamento, transformação e serving) |
| 2 | Compreender as diferenças práticas entre **Data Warehouse, Data Lake, Data Lakehouse e Data Mesh** |
| 3 | Entender os princípios que orientam decisões de arquitetura (escalabilidade, governança, custo, interoperabilidade) |
| 4 | Treinar o uso de IA generativa (NotebookLM) como ferramenta de **estudo ativo baseado em fontes**, e não apenas como gerador de respostas prontas |
| 5 | Praticar **engenharia de prompts** para extrair explicações estruturadas, comparações e glossários confiáveis, sempre ancorados nas fontes carregadas (*grounded answers*) |

---

## 2. Curadoria de Fontes

Foram selecionadas fontes abertas, reconhecidas pela comunidade de dados, cobrindo desde os fundamentos até arquiteturas modernas. Todas foram carregadas como fontes no Caderno do NotebookLM.

| # | Fonte | Tipo | Foco | Link |
|---|-------|------|------|------|
| 1 | **Fundamentals of Data Engineering** — Joe Reis & Matt Housley (O'Reilly / eBook gratuito cedido pela Redpanda) | PDF / Livro | Ciclo de vida da engenharia de dados, fundamentos, *undercurrents* (segurança, DataOps, arquitetura, orquestração) | [freecomputerbooks.com](https://freecomputerbooks.com/Fundamentals-of-Data-Engineering.html) |
| 2 | **How to Move Beyond a Monolithic Data Lake to a Distributed Data Mesh** — Zhamak Dehghani | Artigo | Origem do conceito de Data Mesh e crítica aos Data Lakes centralizados | [martinfowler.com](https://martinfowler.com/articles/data-monolith-to-mesh.html) |
| 3 | **Data Mesh Principles and Logical Architecture** — Zhamak Dehghani | Artigo | Os 4 princípios do Data Mesh e sua arquitetura lógica | [martinfowler.com](https://martinfowler.com/articles/data-mesh-principles.html) |
| 4 | **The Data Engineering Cookbook** — Andreas Kretz (open source) | PDF | Modelagem de dados, pipelines, storage, batch vs. streaming | [freecomputerbooks.com](https://freecomputerbooks.com/The-Data-Engineering-Cookbook-Mastering-The-Plumbing-Of-Data-Science.html) |
| 5 | **Data Management Guide** — Martin Fowler | Portal / coletânea de artigos | Panorama geral de arquitetura de dados, Big Data e evolução do tema | [martinfowler.com/data](https://martinfowler.com/data/) |

> **Critério de seleção:** priorizei fontes **primárias e abertas** — os próprios autores dos conceitos, como Reis/Housley para o ciclo de vida de dados e Dehghani para Data Mesh — evitando conteúdo secundário ou pago, de forma a garantir respostas do NotebookLM bem fundamentadas (*grounded*) e citáveis.

---

## 3. Engenharia de Prompts e Troubleshooting

Documentação do processo real de interação com o NotebookLM: perguntas estratégicas, variações testadas, respostas obtidas e dificuldades encontradas ao longo do caminho.

### 3.1 Perguntas estratégicas elaboradas

| Prompt | Objetivo | Resultado obtido |
|--------|----------|-------------------|
| *"Resuma, em tópicos, as etapas do ciclo de vida da engenharia de dados descritas na fonte 'Fundamentals of Data Engineering', citando a fonte para cada etapa."* | Obter um resumo estruturado e rastreável | Retornou as 5 etapas (geração, armazenamento, ingestão, transformação, serving) com citações diretas ao livro — funcionou bem por pedir explicitamente a citação |
| *"Compare Data Lake, Data Warehouse e Data Lakehouse em uma tabela, com base apenas nas fontes carregadas."* | Testar geração de tabelas comparativas | Gerou tabela coerente, mas com lacuna sobre Lakehouse (fonte não trata o tema em profundidade) — o modelo sinalizou a limitação em vez de "inventar" |
| *"Quais são os 4 princípios do Data Mesh segundo Zhamak Dehghani? Explique cada um com um exemplo prático."* | Extrair conceito-chave com exemplo aplicado | Resposta completa (ownership por domínio, dado como produto, self-serve platform, governança federada), com exemplos plausíveis que precisaram de checagem manual |
| *"Gere 10 perguntas de revisão no estilo 'flashcard' sobre os temas das fontes carregadas."* | Criar material de revisão espaçada | Gerou perguntas boas, porém genéricas nas primeiras tentativas (ver dificuldades abaixo) |
| *"Quais tensões ou trade-offs de arquitetura aparecem quando comparamos Data Mesh com uma arquitetura centralizada?"* | Estimular pensamento crítico, não só memorização | Resposta rica, destacando custo de coordenação vs. autonomia, e complexidade de governança federada |

### 3.2 Variações de prompt testadas

| Versão | Prompt | Resultado |
|--------|--------|-----------|
| ❌ Vago | *"Fale sobre engenharia de dados."* | Resposta genérica, pouco ancorada nas fontes — quase um "resumo de senso comum" |
| ✅ Refinado | *"Com base exclusivamente nas fontes carregadas, explique o que é engenharia de dados e cite de qual fonte vem cada afirmação."* | Resposta específica, rastreável e alinhada ao material |
| ❌ Amplo demais | *"Crie um glossário completo de Big Data."* | Trouxe termos fora das fontes selecionadas (risco de alucinação/generalização) |
| ✅ Delimitado | *"Crie um glossário com os termos técnicos citados nas fontes carregadas, com definição de uma frase para cada."* | Glossário mais fiel e enxuto |

### 3.3 Dificuldades encontradas (troubleshooting)

1. **Respostas genéricas na primeira tentativa** — sem a instrução "com base nas fontes", o NotebookLM tendia a responder com conhecimento geral do modelo, em vez de se apoiar no material carregado.
   → *Solução:* adicionar explicitamente "baseie-se apenas nas fontes" e "cite a fonte".
2. **Perguntas de revisão repetitivas** — o primeiro lote de flashcards trouxe perguntas muito parecidas entre si.
   → *Solução:* pedir explicitamente variedade ("misture perguntas conceituais, comparativas e de aplicação prática").
3. **Dificuldade em comparar conceitos ausentes nas fontes** — ex.: Lakehouse é pouco citado no material selecionado.
   → *Solução:* o próprio NotebookLM sinalizou a limitação; percebi a importância de **checar a cobertura das fontes antes de pedir comparações**, complementando a curadoria quando necessário.
4. **Risco de excesso de confiança nas respostas** — mesmo com *grounding*, é preciso revisão crítica humana, especialmente em exemplos "práticos" gerados pela IA.
   → *Solução:* tratar toda resposta da IA como rascunho a validar, nunca como fonte final.

---

## 4. Miniguia de Estudo — Entrega Final

### 4.1 Resumos Estruturados

**O que é Engenharia de Dados?**
É a disciplina responsável por projetar, construir e manter os sistemas que coletam, armazenam, transformam e disponibilizam dados de forma confiável para analistas, cientistas de dados e sistemas de negócio.

**Ciclo de vida da Engenharia de Dados** *(baseado em Reis & Housley)*

1. **Geração (Source Systems)** — dados nascem em bancos transacionais, APIs, arquivos, sensores, eventos.
2. **Ingestão** — coleta dos dados via batch ou streaming, de forma confiável e resiliente.
3. **Armazenamento** — escolha entre bancos relacionais, data lakes, data warehouses ou lakehouses, considerando custo, performance e escalabilidade.
4. **Transformação** — modelagem e limpeza dos dados (ETL/ELT), aplicando regras de negócio.
5. **Serving** — disponibilização dos dados para BI, Machine Learning e aplicações de *reverse ETL*.

Esse ciclo é atravessado por **undercurrents** (temas transversais): segurança, gestão de dados, DataOps, arquitetura de dados, orquestração e engenharia de software.

**Arquiteturas de Dados — visão comparativa**

| Arquitetura | Características principais |
|-------------|------------------------------|
| **Data Warehouse** | Estrutura centralizada, otimizada para consultas analíticas com dados já modelados (*schema-on-write*). Forte em governança, mais rígida para dados não estruturados |
| **Data Lake** | Repositório centralizado que armazena dados brutos em qualquer formato (*schema-on-read*). Flexível, mas com risco de virar um "data swamp" sem boa governança |
| **Data Lakehouse** | Combina a flexibilidade do Data Lake com recursos de governança e performance do Data Warehouse |
| **Data Mesh** | Descentraliza a propriedade dos dados por domínio de negócio, tratando "dado como produto", com infraestrutura self-service e governança federada — resposta arquitetural aos gargalos de equipes centrais de dados |

**Princípios do Data Mesh**

1. Propriedade de dados orientada a domínio (*domain ownership*)
2. Dado como produto (*data as a product*)
3. Plataforma de infraestrutura self-service
4. Governança computacional federada

### 4.2 Glossário

| Termo | Definição resumida |
|-------|----------------------|
| **ETL** | *Extract, Transform, Load* — processo de extrair dados da origem, transformá-los e carregá-los no destino |
| **ELT** | Variante do ETL em que a transformação ocorre depois de os dados já estarem carregados no destino (comum em data warehouses modernos na nuvem) |
| **Data Lake** | Repositório que armazena dados brutos, estruturados ou não, sem exigir schema definido previamente |
| **Data Warehouse** | Sistema de armazenamento otimizado para consultas analíticas, com dados modelados e organizados |
| **Data Lakehouse** | Arquitetura híbrida que une a flexibilidade do data lake à governança/performance do data warehouse |
| **Data Mesh** | Arquitetura descentralizada de dados organizada por domínios de negócio, com dado tratado como produto |
| **DataOps** | Conjunto de práticas culturais e técnicas, inspiradas no DevOps, para agilizar e dar qualidade ao ciclo de vida dos dados |
| **Ingestão de dados** | Processo de coletar dados de fontes diversas para um sistema de armazenamento/processamento |
| **Governança federada** | Modelo de governança em que regras globais são aplicadas de forma automatizada e descentralizada entre domínios |
| **Orquestração** | Coordenação automatizada de pipelines e dependências entre tarefas de dados (ex.: Airflow) |
| **Schema-on-write / Schema-on-read** | Momento em que a estrutura dos dados é definida: na escrita (*write*) ou apenas na leitura (*read*) |

### 4.3 Prompts Reutilizáveis

Modelos de prompts testados e validados, prontos para reutilização em novas sessões de estudo no NotebookLM (ou em qualquer LLM com fontes carregadas):

```text
1. "Com base exclusivamente nas fontes carregadas, resuma [TEMA] em até 5 tópicos, citando a fonte de cada afirmação."

2. "Crie uma tabela comparativa entre [CONCEITO A] e [CONCEITO B], usando apenas informações presentes
   nas fontes. Se alguma fonte não cobrir o tema, indique a lacuna."

3. "Gere 10 perguntas de revisão sobre [TEMA], misturando perguntas conceituais, comparativas e de
   aplicação prática, no estilo flashcard (pergunta/resposta)."

4. "Quais são os principais trade-offs ou tensões arquiteturais envolvidos em [DECISÃO/CONCEITO]?
   Baseie-se nas fontes."

5. "Crie um glossário com os termos técnicos mencionados nas fontes sobre [TEMA], com definição de
   uma frase para cada termo."

6. "Explique [CONCEITO] como se estivesse ensinando para alguém iniciante, mantendo fidelidade às
   fontes carregadas."

7. "Liste 3 aplicações práticas ou estudos de caso do conceito [X] mencionados nas fontes."
```

> **Dica de uso:** sempre inclua a instrução *"baseie-se apenas nas fontes carregadas"* e peça citações — isso reduz respostas genéricas e aumenta a confiabilidade do material gerado.

---

## Estrutura do Repositório

```
miniguia-estudos/
└── README.md   → este arquivo, contendo todo o material do desafio
```

## Conclusão

Este projeto demonstrou como transformar o NotebookLM em uma ferramenta de **estudo ativo**: em vez de apenas "perguntar e receber respostas", a curadoria de fontes confiáveis, o refinamento iterativo de prompts e a documentação das dificuldades tornaram o processo de aprendizagem mais crítico, rastreável e reutilizável — competências centrais para quem constrói uma carreira em Engenharia e Arquitetura de Dados.

---

<div align="center">

Projeto desenvolvido como parte do desafio de projeto da **[DIO](https://www.dio.me/)** — Sem Parar Corpay - Back-end do Zero a Prática

</div>

# Diário de Bordo - Ranni Heler

Esta seção tem como objetivo registrar, ao longo das sprints, o acompanhamento individual das atividades realizadas no projeto.

A cada sprint, são documentadas as experiências, tarefas realizadas, dificuldades e aprendizados durante o processo de contribuição no MEPA, permitindo acompanhar a evolução individual dentro do projeto.

---

## Sprint 0 - Documentação  
**Duração**: 06/04/2026 - 22/04/2026  

### Resumo da Sprint

Nesta sprint, minha contribuição foi focada principalmente na **organização e documentação das issues prioritárias** para início das atividades no projeto MEPA.

Além disso, realizei estudos sobre a estrutura do projeto e entendimento geral do funcionamento do sistema, com o objetivo de conseguir selecionar tarefas mais adequadas para início prático.

---

### Atividades Realizadas

| Data | Atividade | Tipo | Referência | Status |
| ----- | --------- | ---- | ---------- | ------ |
| 20/04 | Estudo da estrutura geral do projeto MEPA | Estudo | [Repositório MEPA](https://gitlab.com/lappis-unb/projetos-energia/mepa) | Concluído✅ |
| 20/04 | Análise das issues disponíveis no repositório | Estudo | [Repositório MEPA](https://gitlab.com/lappis-unb/projetos-energia/mepa) | Concluído✅ |
| 21/04 | Levantamento e seleção de issues prioritárias | Estudo/Doc | [Sprint 0](../sprints/sprint0.md) | Concluído✅ |
| 21/04 | Organização das issues em categorias (fáceis e médias) | Doc | [Sprint 0](../sprints/sprint0.md) | Concluído✅ |
| 21/04 | Documentação das issues selecionadas | Doc | [Sprint 0](../sprints/sprint0.md) | Concluído✅ |

---

### Maiores Avanços

O principal avanço foi a definição clara de um **grupo inicial de issues prioritárias**, separadas por nível de dificuldade.

Essa organização ajuda diretamente no início das contribuições práticas, permitindo uma abordagem mais estruturada e reduzindo o tempo gasto decidindo por onde começar.

Os estudos realizados também contribuíram para uma melhor compreensão do contexto do projeto, facilitando a leitura e interpretação das issues.

---

### Dificuldades

A principal dificuldade foi identificar, entre diversas issues disponíveis, **quais eram mais viáveis para início**, especialmente considerando a falta de contexto em algumas descrições.

Também houve uma certa dificuldade inicial em entender completamente a organização do projeto e como as diferentes partes se conectam.

---

### Aprendizados

Durante essa sprint, aprendi a analisar issues de um projeto real com base em **complexidade, impacto e clareza de escopo**.

Também desenvolvi uma melhor noção de como estruturar tarefas iniciais em projetos open source, além de ganhar familiaridade com a leitura de repositórios e identificação de pontos de entrada para contribuição.

---

### Plano Pessoal para a Próxima Sprint

Na próxima sprint, pretendo iniciar a implementação prática de pelo menos uma das issues selecionadas, aprofundando o entendimento do código e do funcionamento do sistema.

---

## Sprint 1 - Refinamento da Documentação Técnica

**Duração**: 27/04/2026 - 11/05/2026

### Resumo da Sprint

Este ciclo de trabalho foi dedicado à auditoria e expansão da documentação do repositório backend do SIGE (SIGE API). O objetivo central foi elevar o padrão de Experiência do Desenvolvedor (DX), transformando manuais técnicos densos em guias visuais e práticos que facilitem o ingresso de novos colaboradores no projeto.

### Registro de Atividades

| Data | Descrição da Atividade | Categoria | Referência | Status |
| --- | --- | --- | --- | --- |
| 27/04 | Alinhamento com a o grupo sobre a Ana Carolina para estabelecer o fluxo de contribuição no projeto | Reunião | N/A | Concluído ✅ |
| 05/05 | Reunião de definição sobre o formato e os padrões técnicos das contribuições | Planejamento | N/A | Concluído ✅ |
| 06/05 | Delimitação do escopo da Sprint 1, priorizando a documentação do servidor API | Estratégia | N/A | Concluído ✅ |
| 10/05 | Implementação de melhorias no README (estrutura, endpoints e debug) no repositório fork | Documentação | [Link do Commit no Fork](https://gitlab.com/ranniheler/mepa-api-ranni/-/commit/f3a5fe24608cabc351a7117327d891473e2cc5ad) | Concluído ✅ |
| 10/05 | Submissão das melhorias para o repositório original via Merge Request | Integração | [Link do Merge Request](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-api/-/merge_requests/31) | Concluído ✅ |

### Principais Conquistas

* **Sincronia com a Coordenação**: Estabelecimento de uma comunicação clara com a Ana Carolina para garantir que as entregas estivessem alinhadas às expectativas do LAPPIS.
* **Mapeamento de Lacunas**: Identificação de pontos cegos na documentação original, especificamente em relação à hierarquia de pastas e procedimentos de depuração.
* **Contribuição Efetiva**: Finalização e envio do primeiro Merge Request contendo melhorias estruturais e guias de qualidade de código (Ruff e pre-commit).

### Desafios Encontrados

O principal obstáculo foi identificar oportunidades de melhoria real em uma documentação que já possuía uma ótima base. O desafio foi ir além do básico, focando em ferramentas que não estavam explicitadas, como a árvore de diretórios e o mapeamento rápido de endpoints, para reduzir a carga cognitiva de quem consulta o repositório pela primeira vez.

### Lições Aprendidas

A sprint reforçou a importância de documentar não apenas "o que" o sistema faz, mas "como" o desenvolvedor interage com ele no dia a dia. A inclusão de guias de monitoramento, logs e checklists de setup inicial provou ser essencial para tornar o projeto verdadeiramente acessível e sustentável.

## Sprint 2 - Testes de Relatórios e Eventos

**Duração**: 12/05/2026 - 25/05/2026

### Resumo da Sprint

Nesta sprint, minha atuação foi focada principalmente na implementação e expansão da suíte de testes do módulo de medidores do MEPA Web, com ênfase especial nos fluxos de relatórios técnicos, eventos e componentes utilizados pelos geradores de PDF.

A atividade foi realizada com base na issue originalmente levantada por um colega da equipe, utilizando-a como referência para estruturar os cenários necessários e ampliar a cobertura dos componentes mais críticos do sistema.

Além da criação dos testes, também foi necessário desenvolver mocks para módulos específicos do Next.js, permitindo que os testes fossem executados corretamente dentro do ambiente do Vitest.

---

### Registro de Atividades

| Data  | Descrição da Atividade                                                                         | Categoria    | Referência           | Status      |
| ----- | ---------------------------------------------------------------------------------------------- | ------------ | -------------------- | ----------- |
| 17/05 | Estudo da estrutura dos componentes de relatório técnico e eventos                             | Estudo       | MEPA Web             | Concluído ✅ |
| 23/05 | Análise da issue de testes utilizada como base para implementação                              | Planejamento | Issue #73            | Concluído ✅ |
| 23/05 | Criação de mocks para módulos do Next.js (`next/navigation`, `next/image`, `next/cache`, etc.) | Infra/Testes | Repositório MEPA Web | Concluído ✅ |
| 23/05 | Implementação de testes para actions e páginas de relatório técnico                            | Testes       | [MR Sprint 2](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests/77)         | Concluído ✅ |
| 24/05 | Implementação de testes para componentes de eventos e summaries                                | Testes       | [MR Sprint 2](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests/77)          | Concluído ✅ |
| 24/05 | Implementação de testes para filtros, tabelas e estados de loading/error                       | Testes       | [MR Sprint 2](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests/77)          | Concluído ✅ |
| 24/05 | Ajustes de responsividade e estabilização da suíte de testes                                   | Refatoração  | [MR Sprint 2](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests/77)            | Concluído ✅ |
| 25/05 | Revisão final e preparação do Merge Request                                                    | Integração   | [MR Sprint 2](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests/77)            | Concluído ✅ |

---

### Principais Conquistas

* Expansão significativa da cobertura de testes do módulo de medidores.
* Criação de uma infraestrutura de mocks reutilizáveis para o ambiente Next.js no Vitest.
* Implementação de testes para fluxos críticos relacionados a:

  * relatórios técnicos
  * summaries
  * tabelas de eventos
  * filtros
  * error boundaries
  * loading states
* Maior estabilidade da suíte de testes para futuras implementações no projeto.
* Pequena melhoria visual na responsividade do seletor de período da tabela de eventos.

---

### Desafios Encontrados

A principal dificuldade desta sprint foi lidar com dependências do Next.js dentro do ambiente de testes. Muitos componentes dependiam diretamente de APIs como `next/navigation`, `next/image` e `next/headers`, o que exigiu a criação de mocks específicos para evitar falhas durante a execução.

Outro desafio foi estruturar testes para componentes assíncronos e estados de carregamento sem tornar os cenários frágeis ou excessivamente acoplados à implementação interna.

---

### Lições Aprendidas

Durante esta sprint, aprofundei bastante meu entendimento sobre testes em aplicações React/Next.js utilizando Vitest e React Testing Library.

Também aprendi mais sobre:

* isolamento de dependências em testes
* mocking de módulos do Next.js
* validação de fluxos assíncronos
* estratégias para testes de componentes complexos e interativos

Além disso, foi uma experiência importante trabalhar a partir de uma issue originalmente levantada por outro integrante da equipe, adaptando e expandindo a proposta inicial conforme as necessidades reais encontradas no projeto.

---

### Plano Pessoal para a Próxima Sprint

Na próxima sprint, pretendo continuar contribuindo diretamente no MEPA Web, focando mais em funcionalidades práticas do sistema e aprofundando o contato com fluxos de frontend mais complexos, especialmente envolvendo visualização de dados e experiência do usuário.

---

## Histórico de Versão

| Data       | Versão | Descrição                 | Autor                                       |
| ---------- | ------ | ------------------------- | ------------------------------------------- |
| 21/04/2026 | 1.0    | Versão inicial - Sprint 0 | [Ranni Heler](https://github.com/akaeranni) |
| 10/05/2026 | 1.1    | Sprint 1                  | [Ranni Heler](https://github.com/akaeranni) |
| 25/05/2026 | 1.2    | Sprint 2                  | [Ranni Heler](https://github.com/akaeranni) |

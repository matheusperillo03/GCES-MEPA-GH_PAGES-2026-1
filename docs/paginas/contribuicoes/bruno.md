# Diário de Bordo - Bruno Vasconcelos

Esta seção tem como objetivo registrar, ao longo das sprints, o acompanhamento individual das atividades realizadas por cada integrante do grupo.

A cada sprint, cada membro irá documentar sua experiência no projeto, descrevendo as tarefas realizadas, dificuldades encontradas, decisões tomadas e aprendizados adquiridos durante o processo de contribuição no MEPA. Além disso, o diário de bordo funciona como um histórico do desenvolvimento do projeto, tornando rastreável o processo de contribuição em um ambiente de software livre.

---
## Sprint 0 - Documentação
**Duração**: 06/04/2026 - 22/04/2026

### Resumo da Sprint

Nesta sprint, o foco principal foi preparar a base para as próximas contribuições no projeto MEPA. Além de conseguir subir o ambiente e compreender melhor a estrutura do repositório, também foi necessário iniciar a documentação do nosso próprio grupo, organizando o espaço onde serão registradas as sprints, atas e demais entregas da disciplina.

### Atividades Realizadas

| Data | Atividade | Tipo | Referência | Status |
| ----- | --------- | ---- | ---------- | ------ |
| 18/04 | Estudo da estrutura do repositório MEPA | Estudo | [Repositório MEPA](https://gitlab.com/lappis-unb/projetos-energia/mepa) | Concluído✅ |
| 18/04 | Análise dos 3 repositórios do grupo MEPA no GitLab | Estudo | [Repositório MEPA](https://gitlab.com/lappis-unb/projetos-energia/mepa) | Concluído✅ |
| 18/04 | Estudo da estrutura do repositório MEPA | Doc | [Repositório MEPA](https://gitlab.com/lappis-unb/projetos-energia/mepa) | Concluído✅ |
| 21/04 | Revisão de documentação  sprint 0| Doc | [Repositório GCES - MEPA](https://github.com/matheusperillo03/GCES-MEPA-GH_PAGES-2026-1) | Concluído✅ |



### Maiores Avanços

Consegui estruturar a base da documentação do grupo, deixando o MkDocs funcionando no repositório e com deploy automático configurado. Isso ajudou a organizar melhor o fluxo de trabalho da equipe e facilitou a construção das páginas que serão usadas ao longo da disciplina.

Além disso, o estudo inicial do repositório MEPA foi importante para entender como o projeto está dividido e como as partes do sistema se relacionam. Ao identificar que o projeto é separado em três repositórios principais, ficou mais claro onde cada tipo de contribuição pode acontecer e como o trabalho do grupo deve ser direcionado.

Também foi possível iniciar o levantamento de issues e entender melhor o perfil das tarefas disponíveis, o que será útil para definir contribuições mais adequadas nas próximas sprints.

### Dificuldades

O principal avanço nesta sprint foi compreender a estrutura real do projeto MEPA e como ele está organizado dentro do GitLab. Identificar que o sistema é dividido em três repositórios principais — API, Web e Infra — permitiu visualizar com mais clareza onde cada tipo de contribuição se encaixa e como as partes se comunicam entre si.

Além disso, a configuração do fluxo de deploy automático da documentação do grupo, utilizando GitHub Actions com MkDocs, foi um passo importante para estabelecer uma base técnica sólida. Essa automação garante que o site do grupo seja atualizado automaticamente a cada push, facilitando a organização das entregas da disciplina.

Outro avanço relevante foi o início do levantamento e análise das issues disponíveis no MEPA. Isso ajudou a mapear tarefas com perfil mais adequado para iniciantes, direcionando melhor os próximos passos do grupo e reduzindo a barreira de entrada para contribuições futuras.

### Aprendizados

Durante essa sprint, aprendi mais sobre a estrutura de um projeto de software livre em um contexto real, principalmente sobre a divisão entre frontend, backend e infraestrutura. Também tive contato mais prático com a configuração do MkDocs e com a automação de deploy da documentação, o que ajudou bastante na organização do repositório do grupo.


### Plano Pessoal para a Próxima Sprint

Na próxima sprint, pretendo começar a me aprofundar mais nas issues do MEPA para identificar possíveis contribuições mais simples e adequadas ao nosso nível de familiaridade com o projeto.

---

## Sprint 1 - Primeira Contribuição
**Duração**: 27/04/2026 - 11/05/2026

### Resumo da Sprint

Nesta sprint, realizei minha primeira contribuição efetiva ao projeto MEPA, focada em documentação. A tarefa consistiu em adicionar uma seção de "Problemas comuns" (Troubleshooting) no `README.md` do repositório **mepa-web**. Durante o processo, também identifiquei que meu fork estava privado e precisei ajustar a visibilidade - uma lição importante para contribuições futuras.

Devido ao alto volume de demandas e à agenda corrida dos mantenedores, não foi possível que eles preparassem issues específicas para nossa equipe. Diante disso, fomos orientados a buscar contribuições mais acessíveis, como melhorias na documentação dos repositórios MEPA (web, api e infra).

### Atividades Realizadas

| Data | Atividade | Status |
|------|-----------|--------|
| 08/05 | Exploração dos repositórios MEPA para identificar pontos de melhoria | ✅ |
| 10/05 | Fork do `mepa-web` (inicialmente privado, depois ajustado para público) | ✅ |
| 10/05 | Configuração de chave SSH no GitLab | ✅ |
| 10/05 | Criação da branch `docs/troubleshooting` e edição do README | ✅ |
| 11/05 | Abertura do Merge Request para a branch `develop` | ✅ |

### Maiores Avanços

- **Primeiro MR no GitLab**: Embora já tenha familiaridade com Git e GitHub, foi minha primeira contribuição usando GitLab. Aprendi as diferenças práticas: onde ficam os forks, como configurar upstream e o fluxo de abertura de MRs.
- **Fork privado → público**: Errei a visibilidade do fork e precisei corrigir. Aprendi que, para contribuições open source, o fork precisa ser público.
- **Seção de Troubleshooting**: Contribuí com um guia prático para problemas comuns (porta ocupada, API não responde, rebuild de containers, logs), preenchendo uma lacuna que dificultava o onboarding de novos contribuidores.

### Dificuldades

- **Fork privado por engano**: Percebi apenas depois de abrir o MR que meu fork estava privado, ajustei a visibilidade a tempo para dar visibilidade a outros contribuidores.
- **Autenticação no GitLab**: Diferente do GitHub, o GitLab não aceita senha no terminal, resolvi configurando chave SSH, que é mais simples e definitiva para resolver os problemas que estava tendo com autenticação com o GitLab.

### Aprendizados

- **Pipeline falhou, mas não impede**: Assim como outros MRs do grupo, o pipeline de CI/CD falhou. Como minha alteração foi apenas em documentação, entendi que isso não invalida a contribuição.
- **Fork precisa ser público**: Lição simples, mas fácil de esquecer na primeira vez.

### Plano Pessoal para a Próxima Sprint

- Acompanhar o MR aberto e responder a eventuais pedidos de ajuste.
- Explorar o repositório `mepa` em busca de oportunidades semelhantes.
- Se possível, evoluir para contribuições um pouco mais técnicas.

---

## Sprint 2

Nesta sprint, o foco foi aumentar a cobertura de testes dos relatórios PDF do MEPA Web (Financeiro, Técnico e Sustentabilidade). Após identificar que esses fluxos estavam com pouca ou nenhuma cobertura automatizada, assumi a responsabilidade por essa parte dentro da Issue #78.

Atividades Realizadas

| Data | Atividade | Tipo | Referência | Status |
|------|-----------|------|------------|--------|
| 21/05 | Análise dos arquivos dos relatórios PDF sem testes | Estudo | Issue #78 | Concluído ✅ |
| 21/05 | Estruturação da Issue #78 | Doc | Issue #78 | Concluído ✅ |
| 22/05 | Implementação dos testes para `buildFinancialReportPdfData.ts` | Teste | MR !78 | Concluído ✅ |
| 22/05 | Implementação dos testes para `FinancialReportPdfDocument.tsx` | Teste | MR !78 | Concluído ✅ |
| 23/05 | Implementação dos testes para `FinancialReportPdfActions.tsx` (helpers puros) | Teste | MR !78 | Concluído ✅ |
| 24/05 | Implementação dos testes para relatórios Técnico e Sustentabilidade | Teste | MR !78 | Concluído ✅ |
| 25/05 | Abertura do MR !78 | Teste | MR !78 | Concluído ✅ |

Maiores Avanços

- Criei o MR !78 com testes para 9 arquivos (3 relatórios × 3 arquivos cada), totalizando 39+ testes;
- Alcancei cobertura de ~90-100% nas funções puras (`buildPdfData`) e componentes PDF (`Document`);
- Aprendi a mockar o `@react-pdf/renderer` de forma DOM-safe para testar componentes React que renderizam PDF;
- Documentei as limitações das `Actions` (dependências de browser), mantendo transparência técnica no MR.

Dificuldades

O maior desafio foi lidar com as dependências de browser nas `Actions`. As funções `captureFigure`, `waitForChartRender` e `captureAllFigures` dependem de `requestAnimationFrame`, `document.fonts.ready`, `URL.createObjectURL` e `window.open` — APIs que não existem no ambiente Node do Vitest sem simulação pesada. Decidi focar nos helpers puros (`sanitizeFileName` e `buildPdfFileName`) que concentram a lógica de negócio relevante (normalização de nome de arquivo, zero-padding do mês, fallback de entidade).

Outro desafio foi mockar o `@react-pdf/renderer` de forma que o componente `FinancialReportPdfDocument` conseguisse renderizar sem quebrar, preservando os elementos `Document`, `Page` e `Text` para asserções estruturais.

Aprendizados

Aprendi na prática como testar componentes React que usam bibliotecas de renderização pesada como `@react-pdf/renderer`, usando stubs DOM-safe e snapshots versionados. Entendi que nem sempre vale a pena forçar cobertura em trechos que dependem de APIs de browser — é melhor isolar o que é realmente testável e documentar o restante.

Também ficou claro que cobertura de linhas sozinha não conta toda a história: as `Actions` têm baixa cobertura (~22%), mas os helpers puros exportados estão totalmente testados, e a lógica de transformação (`buildPdfData`) e renderização (`Document`) estão protegidas contra regressões.

Plano Pessoal para a Próxima Sprint

Quero acompanhar o feedback do time sobre o MR !78 e incorporar as sugestões de revisão. Também quero entender se a abordagem de "testar o que é realmente testável e documentar limitações" foi bem recebida, e se podemos aplicar a mesma estratégia para outros módulos com dependências de browser.

---

## Sprint 3

Nesta sprint, o foco foi complementar a cobertura de testes dos relatórios PDF do MEPA Web, com atenção especial ao módulo de Relatório Técnico. A partir da Issue #73, identifiquei que o Relatório Financeiro já havia recebido cobertura em um MR anterior, então concentrei minha contribuição em um MR separado para o `technical-report`, mantendo o escopo pequeno e complementar.

| Data | Atividade | Tipo | Referência | Status |
|------|-----------|------|------------|--------|
| 01/06 | Análise dos testes já existentes para o Relatório Financeiro | Estudo | Issue #73 / MR !75 | Concluído ✅ |
| 03/06 | Comparação entre os módulos `financial-report` e `technical-report` | Estudo | Issue #73 | Concluído ✅ |
| 04/06 | Ampliação dos testes de `buildTechnicalReportPdfData.ts` | Teste | Issue #73 | Concluído ✅ |
| 08/06 | Criação de testes para helpers puros de nome de arquivo do Relatório Técnico | Teste | Issue #73 | Concluído ✅ |
| 09/06 | Extração de helper puro para `technicalReportPdfFileName.ts` | Código/Teste | Issue #73 | Concluído ✅ |

Maiores Avanços

- Ampliei a suíte de testes do Relatório Técnico seguindo o padrão já usado no Relatório Financeiro;
- Cobri cenários de montagem da estrutura de dados usada pelo PDF técnico;
- Adicionei testes para formatação de datas, valores nulos, vazios, indefinidos e fallbacks textuais;
- Testei a inclusão e omissão das seções opcionais de DHT, além da renumeração correta de tabelas e figuras;
- Isolei os helpers puros de nome de arquivo em um módulo testável, evitando dependências de browser nos testes.

Dificuldades

A principal dificuldade foi manter o escopo pequeno sem deixar de cobrir os comportamentos mais importantes do Relatório Técnico. Algumas partes do fluxo de geração de PDF dependem de APIs de browser e de bibliotecas pesadas, como captura de imagens do DOM e geração real via `@react-pdf/renderer`, então optei por não testar diretamente esses trechos nesta etapa.

Também foi necessário tomar cuidado para não duplicar o trabalho já realizado no MR !75, que cobre o Relatório Financeiro. Como o objetivo era criar uma contribuição complementar, foquei apenas no módulo `technical-report`.

Aprendizados

Aprendi melhor como reaproveitar padrões de teste já existentes no projeto sem copiar cegamente a implementação. Também ficou mais claro que, em módulos com dependências fortes de browser, a melhor estratégia é separar helpers puros e testar a transformação de dados, deixando fluxos de captura/renderização real para testes mais específicos ou futuras refatorações.

Além disso, pratiquei uma abordagem de contribuição mais incremental: analisar o MR relacionado, identificar o que ainda estava descoberto e propor uma entrega pequena, focada e fácil de revisar.

Plano Pessoal para a Próxima Sprint

Quero validar os testes no ambiente completo do projeto com `pnpm run lint`, `pnpm run type-check` e `pnpm run test:coverage`, além de acompanhar possíveis comentários de revisão. Também pretendo observar se há espaço para aplicar a mesma estratégia de isolamento de helpers puros em outros fluxos de geração de PDF ou componentes com dependências de browser.

### Referências

- **Merge Request original (Relatório Financeiro – Issue #73):** [!75 - test: adiciona testes que satisfazem a issue #73 para a parte de relatórios financeiros](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests/75)

---

 
## Histórico de Versão

| Data | Versão | Descrição | Autor |
|------|--------|-----------|-------|
| 20/04/2026 | 1.0 | Versão inicial - Sprint 0 | [Bruno Vasconcelos](https://github.com/brunocva) |
| 11/05/2026 | 1.1 | Versão inicial - Sprint 1 | [Bruno Vasconcelos](https://github.com/brunocva) |
| 25/05/2026 | 1.2 | Versão inicial - Sprint 2 | [Bruno Vasconcelos](https://github.com/brunocva) |
| 09/06/2026 | 1.3 | Versão inicial - Sprint 3 | [Bruno Vasconcelos](https://github.com/brunocva) |
| 01/07/2026 | 1.4 | Versão inicial - Sprint 4 | [Bruno Vasconcelos](https://github.com/brunocva) |

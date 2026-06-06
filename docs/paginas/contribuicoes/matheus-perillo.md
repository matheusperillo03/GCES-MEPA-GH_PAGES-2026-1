# Diário de Bordo - Matheus Perillo

Esta seção tem como objetivo registrar, ao longo das sprints, o acompanhamento individual das atividades realizadas no projeto.

A cada sprint, são documentadas as experiências, tarefas realizadas, dificuldades e aprendizados durante o processo de contribuição no MEPA, permitindo acompanhar a evolução individual dentro do projeto.

---

## Sprint 0 - Documentação  
**Duração**: 06/04/2026 - 22/04/2026  

### Resumo da Sprint

Nesta sprint, minha contribuição foi focada principalmente na **criação do repositório para documentação, criação e configuração inicial do github pages, organização e documentação de como configurar o ambiente** para início das atividades no projeto MEPA.

---

### Atividades Realizadas

| Data | Atividade | Tipo | Referência | Status |
| ----- | --------- | ---- | ---------- | ------ |
| 13/04 | Criação do repositório | Documentação | [Repositório de documentação MEPA](https://github.com/matheusperillo03/GCES-MEPA-GH_PAGES-2026-1) | Concluído✅ |
| 13/04 | Configuração inicial do github pages | Configuração | [Repositório de documentação MEPA](https://github.com/matheusperillo03/GCES-MEPA-GH_PAGES-2026-1) | Concluído✅ |
| 20/04 | Estudo da estrutura geral do projeto MEPA | Estudo | [Repositório MEPA](https://gitlab.com/lappis-unb/projetos-energia/mepa) | Concluído✅ |
| 20/04 | Análise das tecnologias para configurar o ambiente | Estudo | [Repositório MEPA](https://gitlab.com/lappis-unb/projetos-energia/mepa) | Concluído✅ |
| 21/04 | Levantamento e catálogo de documentação relativo a instalação e configuração local do projeto | Estudo/Doc | [Sprint 0](../sprints/sprint0.md) | Concluído✅ |
| 21/04 | Organização do Documento | Doc | [Sprint 0](../sprints/sprint0.md) | Concluído✅ |
| 21/04 | Documentação das issues selecionadas | Doc | [Sprint 0](../sprints/sprint0.md) | Concluído✅ |

---

### Maiores Avanços

- Criação do repositório de configuração do github pages para documentação do projeto.
- Identificação e **configuração dos ambientes de infraestrutura, web e API** do projeto MEPA.

---

### Dificuldades

O maior desafio foi a curva de aprendizado do GitLab e da estrutura do projeto, ambos desconhecidos até então. Somado a isso, a configuração dos ambientes de desenvolvimento com tecnologias inéditas exigiu bastante tempo de pesquisa e experimentação.

---

### Aprendizados

Aprendi na prática a configurar os ambientes de infra, web e API, ganhando familiaridade com as tecnologias do projeto. Com o tempo, também fui ficando mais à vontade para analisar as issues abertas e entender quais priorizar, considerando complexidade, impacto e o quão bem definidas estão.

---

### Plano Pessoal para a Próxima Sprint

Na próxima sprint, quero entender melhor como o projeto funciona por dentro, explorar a arquitetura com mais calma e ver como as peças se conectam. Com isso, espero chegar nas issues com mais confiança e conseguir resolvê-las de forma mais efetiva.

---

## Sprint 2 - Testes
**Duração**: 12/05/2026 - 25/05/2026

### Resumo da Sprint

Nesta sprint, o foco foi aumentar a cobertura de testes do módulo de **Mapa** do MEPA Web, que estava em apenas 49% no módulo principal e 21% nos componentes. Após entrar em contato com o time e obter acesso ao relatório de cobertura (`lcov.info`), identifiquei os três arquivos mais críticos sem testes (`map-explorer`, `map-explorer-markers` e `map-explorer-sidebar`) e assumi a responsabilidade por esse módulo dentro da [Issue #75](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/work_items/75), que foi dividida entre três integrantes.

### Atividades Realizadas

| Data | Atividade | Tipo | Referência | Status |
| ----- | --------- | ---------------------------------------- | --------------- | ------ |
| 13/05  | Reunião com o grupo atuante para saber como podemos atuar no projeto | Solicitação | Não resultou em material concreto | Concluído✅ |
| 19/05  | Separação de possíveis temas de issues com base no coverage, dentro do nosso grupo | Decisão interna | Não resultou em material concreto | Concluído✅ |
| 20/05  | Análise do relatório de cobertura e identificação dos arquivos do módulo Mapa sem testes | Estudo | [Issue #75](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/work_items/75) | Concluído✅ |
| 21/05  | Estruturação da [Issue #75](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/work_items/75) | Doc | [Issue #75](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/work_items/75) | Concluído✅ |
| 21/05  | Estudo da estrutura do módulo Mapa e das dependências externas (Leaflet, next/dynamic) | Estudo | [MR #76](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests/76) | Concluído✅ |
| 22/05  | Implementação dos testes para `entity-icons.ts`, `page.tsx` e `map-explorer-sidebar.tsx` | Teste | [MR #76](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests/76) | Concluído✅ |
| 23/05  | Implementação dos testes para `map-explorer.tsx` e `map-explorer-markers.tsx` | Teste | [MR #76](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests/76) | Concluído✅ |
| 25/05  | Abertura da [Issue #75](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/work_items/75) | Doc | [Issue #75](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/work_items/75) | Concluído✅ |
| 25/05  | Abertura do [MR #76](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests/76) | Teste | [MR #76](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests/76) | Concluído✅ |


### Maiores Avanços

- Criei o [MR #76](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests/76) com 63 novos testes em 5 arquivos, elevando a cobertura do módulo Mapa de **49% para 91%** e dos componentes de **21% para 78%**, atingindo ambas as metas da issue;
- Abri minha primeira issue no projeto, a [Issue #75](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/work_items/75);
- Aprendi a mockar bibliotecas complexas como o Leaflet (exports nomeados e default simultâneos) e o `next/dynamic` com resolução assíncrona no ambiente Vitest.


### Dificuldades

O maior desafio foi lidar com as dependências externas do módulo. O **Leaflet** exige um mock que cubra tanto os exports nomeados quanto o export default ao mesmo tempo, e o **`next/dynamic`** precisou de tratamento especial para simular a resolução assíncrona de componentes no ambiente de testes. Além disso, entender como os arquivos `map-explorer`, `map-explorer-sidebar` e `map-explorer-markers` se integram entre si — via callbacks (`onMarkerClick`, `onMeterClick`) e estado compartilhado — exigiu bastante leitura do código antes de escrever qualquer teste.

### Aprendizados

Aprendi na prática como estruturar testes para componentes React com dependências pesadas de browser e bibliotecas de mapa. Entendi como o rollback otimista funciona no frontend e como testá-lo de forma confiável. Também ficou claro que a cobertura de linhas sozinha não conta toda a história — é preciso garantir que os cenários de erro e os fluxos alternativos também sejam exercitados.


### Plano Pessoal para a Próxima Sprint

Quero entender se vamos continuar buscando mais implementações de testes automatizados ou se vamos contribuir com issues funcionais abertas no momento. Também quero acompanhar o feedback do time sobre o MR #76 e incorporar as sugestões de revisão.

---

## Sprint 3 - Testes
**Duração**: 26/05/2026 - 08/06/2026

### Resumo da Sprint

Nesta sprint, o foco foi cobrir módulos que estavam com 0% de cobertura de testes: os **componentes raiz** (`src/components`), os **gráficos** (`src/components/charts`) e os **stories** (`src/stories`). Esses módulos somavam 1.086 linhas instrumentáveis sem qualquer proteção contra regressões. Abri a [Issue #76](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/work_items/76) para formalizar o escopo e criei o [MR #86](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests/86) cobrindo todos os módulos da issue.

### Atividades Realizadas

| Data | Atividade | Tipo | Referência | Status |
| ----- | --------- | ---------------------------------------- | --------------- | ------ |
| 26/05  | Análise do relatório de cobertura e identificação dos módulos sem testes | Estudo | [Issue #76](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/work_items/76) | Concluído✅ |
| 27/05  | Estruturação da [Issue #76](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/work_items/76) | Doc | [Issue #76](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/work_items/76) | Concluído✅ |
| 27/05  | Estudo da estrutura dos módulos de componentes raiz e gráficos | Estudo | [MR #86](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests/86) | Concluído✅ |
| 28/05  | Implementação dos testes para `src/components` (ErrorBoundary, MetricCard, ReportsDateFilter, LoadingSuspense) | Teste | [MR #86](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests/86) | Concluído✅ |
| 30/05  | Implementação dos testes para `src/components/charts` (MonthlyEnergyChart, ChartCard) | Teste | [MR #86](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests/86) | Concluído✅ |
| 02/06  | Implementação dos smoke tests para os módulos de `src/stories` (23 arquivos) | Teste | [MR #86](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests/86) | Concluído✅ |
| 04/06  | Abertura da [Issue #76](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/work_items/76) | Doc | [Issue #76](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/work_items/76) | Concluído✅ |
| 05/06  | Abertura do [MR #86](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests/86) | Teste | [MR #86](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests/86) | Concluído✅ |

### Maiores Avanços

- Criei o [MR #86](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests/86) com **+590 testes em 31 arquivos**, zerando a dívida de cobertura de 5 módulos e atingindo todas as metas da [Issue #76](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/work_items/76);
- Aprendi a mockar bibliotecas de visualização complexas como o `recharts` e a testar componentes com polling assíncrono via `swr`;
- Implementei smoke tests para 23 arquivos `.stories.tsx`, estabelecendo uma camada de proteção para os contratos visuais do projeto.

### Dificuldades

O maior desafio foi lidar com a complexidade dos módulos de gráficos. O `MonthlyEnergyChart` (494 linhas) e o `ChartCard` (261 linhas) possuem lógica densa de normalização de séries temporais, zoom e polling em tempo real, exigindo mocks cuidadosos do `recharts` e do `swr` para evitar testes frágeis. O `ErrorBoundary`, por ser um componente de classe com retry, também demandou uma abordagem diferente das habituais com componentes funcionais.

### Aprendizados

Aprendi como estruturar testes para componentes com estado assíncrono e polling, entendendo quando usar `waitFor` e `act` corretamente. Também entendi melhor o papel dos stories como contratos visuais e como smoke tests podem ser uma estratégia eficiente para cobrir rapidamente um grande volume de arquivos com baixo custo de manutenção.

### Plano Pessoal para a Próxima Sprint

Quero acompanhar o feedback do time sobre o [MR #86](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests/86) e incorporar as sugestões de revisão. Também quero avaliar se ainda há módulos críticos sem cobertura ou se é hora de migrar para contribuições funcionais no projeto.

---

## Histórico de Versão

| Data       | Versão | Descrição                 | Autor |
| ---------- | ------ | ------------------------- | ----- |
| 21/04/2026 | 1.0    | Versão inicial - Sprint 0 | [Matheus Perillo](https://github.com/matheusperillo03) |
| 24/05/2026 | 1.1    | Contribuição para a Sprint 2 | [Matheus Perillo](https://github.com/matheusperillo03) |
| 05/06/2026 | 1.2    | Contribuição para a Sprint 3 | [Matheus Perillo](https://github.com/matheusperillo03) |
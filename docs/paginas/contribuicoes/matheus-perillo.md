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

## Histórico de Versão

| Data       | Versão | Descrição                 | Autor |
| ---------- | ------ | ------------------------- | ----- |
| 21/04/2026 | 1.0    | Versão inicial - Sprint 0 | [Matheus Perillo](https://github.com/matheusperillo03) |
| 24/05/2026 | 1.1    | Contribuição para a Sprint 2 | [Matheus Perillo](https://github.com/matheusperillo03) |
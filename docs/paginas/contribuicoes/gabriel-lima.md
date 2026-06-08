# Diário de Bordo - Gabriel Lima da Silva

Esta seção tem como objetivo registrar, ao longo das sprints, o acompanhamento individual das atividades realizadas por cada integrante do grupo.

A cada sprint, cada membro irá documentar sua experiência no projeto, descrevendo as tarefas realizadas, dificuldades encontradas, decisões tomadas e aprendizados adquiridos durante o processo de contribuição no MEPA. Além disso, o diário de bordo funciona como um histórico do desenvolvimento do projeto, tornando rastreável o processo de contribuição em um ambiente de software livre.

---

## Sprint 0 - Documentação
**Duração**: 06/04/2026 - 22/04/2026

### Resumo da Sprint

Nesta sprint, minha atuação esteve concentrada em dois eixos complementares: o preparo do ambiente de desenvolvimento e a estruturação da documentação do grupo. No lado técnico, dediquei tempo a entender como o MEPA é orquestrado em containers, subindo o ambiente local com Docker e Docker Compose e estudando o repositório de infraestrutura. No lado da documentação, contribuí com a identidade visual do site do grupo e com a organização da seção de Contribuições Individuais, definindo um padrão de diário de bordo que pudesse ser reaproveitado por todos os integrantes.

### Atividades Realizadas

| Data | Atividade | Tipo | Referência | Status |
| ----- | --------- | ---- | ---------- | ------ |
| 16/04 | Estudo do funcionamento da disciplina e análise de documentações de grupos anteriores para entender as entregas esperadas | Estudo | Repositórios de turmas anteriores | Concluído✅ |
| 17/04 | Configuração do ambiente de desenvolvimento local com Docker e Docker Compose | Configuração | Local | Concluído✅ |
| 18/04 | Estudo do repositório de infraestrutura do MEPA e da orquestração dos containers | Estudo | [Repositório MEPA](https://gitlab.com/lappis-unb/projetos-energia/mepa) | Concluído✅ |
| 20/04 | Personalização visual da documentação do grupo (tema Material, paleta de cores e CSS customizado) | Código/Doc | [extra.css](https://github.com/matheusperillo03/GCES-MEPA-GH_PAGES-2026-1/blob/docs/docs/stylesheets/extra.css) | Concluído✅ |
| 21/04 | Estruturação da seção de Contribuições Individuais e padronização do template de diário de bordo | Doc | [Contribuições](../contribuicoes/gabriel-lima.md) | Concluído✅ |
| 22/04 | Revisão geral da documentação da Sprint 0 e ajustes na navegação do MkDocs | Doc | [Sprint 0](../sprints/sprint0.md) | Concluído✅ |

### Maiores Avanços

- Consegui subir o ambiente local do MEPA por meio do Docker Compose, compreendendo como os serviços do projeto se comunicam entre si;
- Aprofundei o entendimento da camada de infraestrutura do projeto, o que ajudou a enxergar como as partes (web, API e infra) se conectam em tempo de execução;
- Contribuí com a identidade visual da documentação do grupo e ajudei a padronizar o template de diário de bordo, facilitando o trabalho dos demais integrantes nas próximas sprints.

### Dificuldades

A maior dificuldade desta sprint foi a curva de aprendizado da infraestrutura do projeto. Subir todos os serviços via Docker Compose exigiu pesquisa sobre variáveis de ambiente, dependências entre containers e portas, algo com o qual eu ainda não tinha tanta familiaridade. Além disso, por ser o início da disciplina, levou um tempo até eu compreender exatamente o que era esperado como entrega da Sprint 0 e como organizar a documentação do grupo de forma coerente.

### Aprendizados

Aprendi na prática como funciona a orquestração de containers com Docker e Docker Compose em um projeto real, ganhando uma visão mais clara da separação entre infraestrutura, backend e frontend. No âmbito da documentação, entendi a importância de padronizar a estrutura desde cedo: definir um template comum de diário de bordo reduz retrabalho e dá consistência ao registro das contribuições de todo o grupo.

### Plano Pessoal para a Próxima Sprint

Na próxima sprint, pretendo partir do ambiente já configurado para realizar minha primeira contribuição efetiva ao projeto, buscando uma oportunidade de melhoria adequada ao meu nível de familiaridade e acompanhando de perto o fluxo de contribuição adotado pelos mantenedores.

---

## Sprint 1 - Primeira Contribuição
**Duração**: 27/04/2026 - 11/05/2026

### Resumo da Sprint

Nesta sprint, realizei minha primeira contribuição efetiva ao projeto MEPA, com foco em documentação. Como os mantenedores não conseguiram preparar issues específicas para a equipe a tempo, fomos orientados a buscar melhorias acessíveis na documentação dos repositórios. Aproveitando o estudo de infraestrutura que havia feito na sprint anterior, optei por contribuir no repositório `mepa-infra`, onde percebi que o passo a passo para subir o ambiente local com Docker estava disperso e que as variáveis de ambiente necessárias não estavam claramente documentadas. Minha contribuição foi reunir essas informações em um guia de configuração local e descrever as variáveis em um arquivo de exemplo.

### Atividades Realizadas

| Data | Atividade | Tipo | Referência | Status |
|------|-----------|------|------------|--------|
| 28/04 | Análise da documentação dos repositórios MEPA em busca de oportunidades de contribuição | Estudo | [Repositório MEPA](https://gitlab.com/lappis-unb/projetos-energia/mepa) | Concluído ✅ |
| 06/05 | Levantamento das variáveis de ambiente e dos passos necessários para subir o ambiente local | Estudo | [MEPA Infra](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-infra) | Concluído ✅ |
| 08/05 | Fork do `mepa-infra` e criação da branch `docs/setup-ambiente-local` | Código/Doc | — | Concluído ✅ |
| 08/05 | Redação de um guia de configuração local com Docker Compose no `README.md` | Doc | [MEPA Infra](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-infra) | Concluído ✅ |
| 09/05 | Documentação das variáveis de ambiente em um arquivo `.env.example` | Doc | [MEPA Infra](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-infra) | Concluído ✅ |
| 09/05 | Abertura do Merge Request com as alterações | Código/Doc | [MEPA Infra](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-infra) | Concluído ✅ |

### Maiores Avanços

- **Primeira contribuição efetiva**: Abri um Merge Request no `mepa-infra` reunindo, em um único guia, o passo a passo para subir o ambiente local com Docker Compose, reduzindo a barreira de entrada para novos colaboradores.
- **Documentação das variáveis de ambiente**: Descrever as variáveis necessárias em um `.env.example` ajuda quem está configurando o projeto pela primeira vez a entender rapidamente o que precisa ser preenchido, evitando erros silenciosos na subida dos containers.
- **Aproveitamento do estudo da Sprint 0**: Consegui transformar o aprendizado de infraestrutura da sprint anterior em uma contribuição concreta e de impacto direto no onboarding.

### Dificuldades

- **Identificar uma lacuna ainda não coberta**: Como vários colegas também atuaram em documentação, foi preciso analisar com cuidado o que já havia sido melhorado para encontrar uma contribuição que agregasse valor sem sobreposição — no fim, o guia de setup e as variáveis de ambiente eram um ponto ainda pouco documentado.
- **Adaptação ao fluxo do GitLab**: O processo de fork, configuração do remote e abertura de MR no GitLab exigiu um tempo de adaptação em relação ao fluxo a que eu estava acostumado.

### Aprendizados

- **Documentação de infraestrutura como facilitador de onboarding**: Um guia de setup claro e um `.env.example` bem descrito são tão importantes quanto o próprio código para que novos colaboradores consigam rodar o projeto sem depender dos mantenedores.
- **Fluxo de contribuição via fork no GitLab**: Pratiquei o ciclo completo de contribuição em um projeto sem acesso de escrita direto — fork, branch, commit e Merge Request para o repositório original.
- **Boas práticas de nomenclatura**: Apliquei um nome de branch descritivo (`docs/setup-ambiente-local`) seguindo as convenções comuns em projetos open source.

### Plano Pessoal para a Próxima Sprint

- **Acompanhar o MR aberto**: Monitorar a revisão dos mantenedores e responder a eventuais pedidos de ajuste.
- **Evoluir para contribuições técnicas**: Com o ambiente já dominado, pretendo partir para contribuições de código na próxima sprint, especialmente na frente de testes automatizados que o grupo começou a explorar.

---

## Sprint 2 - Testes Unitários
**Duração**: 12/05/2026 - 25/05/2026

### Resumo da Sprint

Nesta sprint, dei meu primeiro passo em contribuições de código no MEPA Web (`mepa-web`), atuando na frente de testes automatizados que o grupo passou a priorizar. Assumi o bloco **Relatório de Sustentabilidade**, parte da [Issue #73](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/work_items/73) (guarda-chuva de relatórios em PDF). Os arquivos desse módulo estavam com `LH: 0` no `coverage/lcov.info`, o que é especialmente arriscado por se tratar de um entregável crítico para o usuário final: qualquer regressão em formatação de moeda/data, em fallbacks de valor nulo ou na montagem do payload de download passaria despercebida sem uma rede de testes. Implementei uma suíte Vitest cobrindo o bloco e criei um helper compartilhado de mocks de PDF reaproveitável pelos demais blocos (Financeiro e Técnico).

### Atividades Realizadas

| Data  | Atividade | Tipo | Referência | Status |
| ----- | --------- | ---- | ---------- | ------ |
| 14/05 | Análise do relatório de cobertura (`lcov.info`) e identificação dos arquivos do módulo de Sustentabilidade sem testes | Estudo | [Issue #73](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/work_items/73) | Concluído ✅ |
| 16/05 | Estudo do fluxo de geração de PDF e das dependências externas (`@react-pdf/renderer`) | Estudo | MEPA Web | Concluído ✅ |
| 19/05 | Criação do helper compartilhado de mocks de PDF (`src/tests/mocks/pdf.ts`), reaproveitável pelos blocos Financeiro e Técnico | Testes | [MR Issue #73](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web) | Concluído ✅ |
| 20/05 | Exposição nominal de helpers puros em `page.tsx` e `SustainabilityReportPdfActions.tsx` (refatoração sem mudança de comportamento) | Refatoração | [MR Issue #73](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web) | Concluído ✅ |
| 22/05 | Implementação dos testes de `buildSustainabilityReportPdfData.ts` e `SustainabilityReportPdfActions.tsx` | Testes | [MR Issue #73](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web) | Concluído ✅ |
| 23/05 | Implementação dos testes de `page.tsx` (sustentabilidade) e `SustainabilityReportPdfDocument.tsx`, com snapshot versionado | Testes | [MR Issue #73](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web) | Concluído ✅ |
| 25/05 | Validação da suíte completa (`lint`, `type-check`, `test:coverage`) e abertura do Merge Request | Integração | [MR Issue #73](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web) | Concluído ✅ |

### Maiores Avanços

- **+90 testes** adicionados ao bloco de Sustentabilidade, elevando a suíte de **410 para 500 testes** (51 arquivos, todos verdes em ~4s, sem nenhum `console.error`/`console.warn`).
- **Cobertura atingida nos arquivos do escopo** (meta ≥ 80% LH nos arquivos com lógica e ≥ 70% de branches no builder principal):

  | Arquivo | LH | Branches |
  | ------- | -- | -------- |
  | `buildSustainabilityReportPdfData.ts` | 100% | 100% |
  | `SustainabilityReportPdfActions.tsx` | 96% | 90% |
  | `page.tsx` (sustentabilidade) | 95% | 70% |
  | `SustainabilityReportPdfDocument.tsx` | 83% | 55% |

- **Helper compartilhado de mocks de PDF** (`src/tests/mocks/pdf.ts`): criei stubs DOM-safe para o `@react-pdf/renderer`, pensados para reuso nos blocos Financeiro e Técnico — uma infraestrutura que beneficia toda a Issue #73, não apenas o meu bloco.
- **Snapshot versionado** do `SustainabilityReportPdfDocument`, gerado a partir de uma fixture representativa, protegendo a estrutura do documento contra regressões visuais.

### Dificuldades

O maior desafio foi tornar testável um módulo construído em torno do `@react-pdf/renderer`, uma biblioteca que manipula o DOM e o fluxo de geração/download de arquivos. Foi necessário desenhar mocks DOM-safe e expor os helpers puros (`clampToNow`, `getPeriodRange`, `formatTimelineMonthLabel`, `getEnergyHistoryMaxY`, `splitDisplayValue`, `sanitizeFileName`, `buildPdfFileName`) de forma nominal, garantindo que a refatoração não alterasse comportamento algum.

Outro ponto delicado foi identificar **branches inalcançáveis**: as actions `getSustainabilitySummaryAction` e `getSustainabilityHistoryAction` (em `actions.ts`) capturam todos os erros em `try/catch` e retornam `null`, o que torna o tratamento de `HTTPError 401` em `page.tsx` (redirect para `/login?session_expired=true`) um trecho de código defensivo hoje inalcançável. Testei esse ramo simulando a propagação do erro, deixando-o pronto para quando o `try/catch` for ajustado — e registrei a ressalva para discussão com o time.

### Aprendizados

- **Mocking de bibliotecas com efeito de DOM**: aprendi a isolar dependências como o `@react-pdf/renderer` com stubs DOM-safe, mantendo os testes estáveis e independentes do comportamento de terceiros.
- **Testabilidade via extração de funções puras**: expor helpers puros sem alterar comportamento é uma forma eficaz de cobrir lógica de formatação e montagem de payload sem depender da renderização completa do componente.
- **Leitura crítica de cobertura**: distinguir branches realmente testáveis de código defensivo inalcançável evita "forçar" cobertura artificial e gera feedback útil para os mantenedores sobre o tratamento de erros das actions.
- **Snapshots como contrato**: snapshots a partir de fixtures representativas são uma forma barata de proteger a estrutura de documentos gerados contra regressões.

### Plano Pessoal para a Próxima Sprint

Na próxima sprint, pretendo continuar contribuindo com a cobertura de testes do `mepa-web`, aproveitando o helper de mocks de PDF que criei para acelerar a cobertura de outros módulos. Também quero acompanhar o feedback dos mantenedores sobre a MR e avaliar, junto ao time, se a propagação de erro nas actions de Sustentabilidade deve virar um MR separado.

---

## Sprint 3 - Cobertura de Testes
**Duração**: 05/06/2026

### Resumo da Sprint

_(a preencher)_

### Atividades Realizadas

| Data | Atividade | Tipo | Referência | Status |
| ----- | --------- | ---- | ---------- | ------ |
| | | | | |

### Maiores Avanços

- _(a preencher)_

### Dificuldades

_(a preencher)_

### Aprendizados

_(a preencher)_

### Plano Pessoal para a Próxima Sprint

_(a preencher)_

---

## Histórico de Versão

| Data | Versão | Descrição | Autor |
| ---- | ------ | --------- | ----- |
| 22/04/2026 | 1.0 | Versão inicial - Sprint 0 | [Gabriel Lima](https://github.com/gabriel-lima258) |
| 09/05/2026 | 1.1 | Adiciona Sprint 1 | [Gabriel Lima](https://github.com/gabriel-lima258) |
| 25/05/2026 | 1.2 | Adiciona Sprint 2 | [Gabriel Lima](https://github.com/gabriel-lima258) |

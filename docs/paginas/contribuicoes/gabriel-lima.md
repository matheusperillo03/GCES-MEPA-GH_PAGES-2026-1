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

## Sprint 3 - Cobertura de Testes (Core: Hooks, Utils, Lib e Services)
**Duração**: 26/05/2026 - 08/06/2026

### Resumo da Sprint

Nesta sprint dei continuidade à frente de testes automatizados do `mepa-web`, assumindo a [Issue #79](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/work_items/79) — guarda-chuva de cobertura das **camadas centrais** da aplicação: `src/hooks/`, `src/utils/`, `src/lib/` e `src/services/`. Esses módulos concentram a lógica reaproveitada por toda a aplicação (formatação de moeda/data, cálculo de disponibilidade fotovoltaica, requisições HTTP, estratégias de cache, parsing de erros e os hooks de dados), mas estavam quase sem testes dedicados — qualquer regressão neles se propagaria silenciosamente por várias telas. Implementei uma suíte com **Vitest + @testing-library/react** (ambiente happy-dom), criando **um arquivo de teste por arquivo-fonte** e cobrindo happy path e casos de erro/edge cases onde a lógica é não-trivial. Segui a convenção de mocks inline já adotada no projeto (`vi.mock` / `vi.stubGlobal`), sem introduzir a pasta `src/tests/mocks/` (inexistente no repositório), e isolei `fetch`, server actions, `next/cache` e o cliente `mepaAPI`.

### Atividades Realizadas

| Data | Atividade | Tipo | Referência | Status |
| ----- | --------- | ---- | ---------- | ------ |
| 27/05 | Levantamento: execução da suíte (baseline de 58 arquivos / 455 testes) e mapeamento dos arquivos sem teste em hooks, utils, lib e services | Estudo | [Issue #79](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/work_items/79) | Concluído ✅ |
| 29/05 | Testes dos utils puros: `currency`, `pv-availability`, `dateUtils`, `meter-display` e `meter-event-display` | Testes | branch `test/79-core-hooks-utils-lib-services` | Concluído ✅ |
| 01/06 | Testes dos utils com mock (`status-mapper`, `fetcher`, `serverFetcher`) e da lib (`constants`, `errors/error-messages`, `errors/error-parser`, `cache-strategies`) | Testes | branch `test/79-core-hooks-utils-lib-services` | Concluído ✅ |
| 03/06 | Teste de services (`meters.server`) e dos hooks puros (`useDebounce`, `usePerformance`, `useSingleData`, `useDateValidation`, `useChartFilters`, `useChartData`) | Testes | branch `test/79-core-hooks-utils-lib-services` | Concluído ✅ |
| 05/06 | Testes dos hooks assíncronos (`useSummaryData`, `useMeterData`, `useMeters`, `useTechnicalReport`, `useEntityFavorites`, `useActiveMeterEvents`, `useEntityDetail`) | Testes | branch `test/79-core-hooks-utils-lib-services` | Concluído ✅ |
| 08/06 | Validação da suíte completa (84 arquivos / 674 testes, sem warnings) e preparação do Merge Request | Integração | [Issue #79](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/work_items/79) | Concluído ✅ |

### Maiores Avanços

- **+26 arquivos de teste e +219 testes**, elevando a suíte de **58 → 84 arquivos** e de **455 → 674 testes** (todos verdes, sem nenhum `console.error`/`console.warn` relacionado aos novos arquivos), com ~2.133 linhas de teste adicionadas.
- **Cobertura das quatro camadas-núcleo** com um arquivo de teste por fonte:
  - **Utils (8):** `currency`, `pv-availability`, `dateUtils`, `meter-display`, `meter-event-display`, `status-mapper`, `fetcher`, `serverFetcher`;
  - **Lib (4):** `constants`, `errors/error-messages`, `errors/error-parser`, `cache-strategies`;
  - **Services (1):** `meters.server`;
  - **Hooks (13):** `useDebounce`, `usePerformance`, `useSingleData`, `useDateValidation`, `useChartFilters`, `useChartData`, `useSummaryData`, `useMeterData`, `useMeters`, `useTechnicalReport`, `useEntityFavorites`, `useActiveMeterEvents`, `useEntityDetail`.
- **Isolamento de dependências externas**: `fetch` mockado para os fetchers (`fetcher`, `serverFetcher`, `useSummaryData`); server actions mockadas por hook; `next/cache` mockado (`unstable_cache` → identidade, `revalidateTag` espionável) e o cliente `mepaAPI` substituído nos testes de `cache-strategies`.
- **Cobertura de erros e edge cases** na lógica não-trivial: respostas 204/404/4xx/5xx e erro de rede nos fetchers; prioridade de status sobre texto e modo dev × produção no `error-parser`; branches do `cache-strategies` (filtro de tempo string × objeto, `categoryFilter "-"`, normalização de acrônimo, token ausente); estados de loading/erro, cancelamento no unmount, refetch e paginação nos hooks; reuso de **cache module-level (TTL/dedupe)** em `useActiveMeterEvents` e `useEntityDetail`.

### Dificuldades

- **Determinismo de datas/timezone** no `dateUtils`: funções que serializam datas com offset fixo (`-03:00`) e dependem de `new Date()` exigiram asserções por padrão (regex/`startsWith`) e reconstrução do valor esperado, evitando testes frágeis que quebrariam em outro fuso.
- **Mockar `next/cache` e o cliente `mepaAPI` (ky)**: foi necessário transformar `unstable_cache` em função identidade para executar a lógica interna diretamente e simular a cadeia `.get(...).json()` do `mepaAPI`, inclusive o `.catch()` encadeado.
- **Caches module-level** em `useActiveMeterEvents` e `useEntityDetail`: como o estado vive fora do componente, isolei cada teste usando `entityId` distintos para evitar contaminação entre casos, além de validar explicitamente o reuso de cache dentro do TTL.
- **Render de JSX em util** (`status-mapper`): testar `getStatusBadge` exigiu renderizar o componente `Badge` com `@testing-library/react` e mockar `getMeterStatusConfig` para controlar label e cor.

### Aprendizados

- **Padrões de teste de hooks** com `renderHook` + `waitFor`/`act`, lidando com efeitos assíncronos, timers falsos (`vi.useFakeTimers`) e limpeza de estado entre casos.
- **Categorização de erros em camada de rede**: validar que cada faixa de status e erro de conexão é mapeada para o tipo correto reforça a robustez da camada de dados.
- **Teste de estratégias de cache e invalidação** sem acoplar ao runtime do Next, mockando `next/cache` e verificando as tags revalidadas.
- **Evitar duplicação**: identifiquei que `useFinancialReportPdfData` já possuía teste e o mantive intacto, focando esforço apenas nas lacunas reais de cobertura.

### Plano Pessoal para a Próxima Sprint

Acompanhar a revisão do Merge Request da Issue #79 e responder a eventuais ajustes dos mantenedores; e seguir ampliando a cobertura no `mepa-web`, avançando de testes unitários para cenários de integração entre hooks e componentes.

---

## Histórico de Versão

| Data | Versão | Descrição | Autor |
| ---- | ------ | --------- | ----- |
| 22/04/2026 | 1.0 | Versão inicial - Sprint 0 | [Gabriel Lima](https://github.com/gabriel-lima258) |
| 09/05/2026 | 1.1 | Adiciona Sprint 1 | [Gabriel Lima](https://github.com/gabriel-lima258) |
| 25/05/2026 | 1.2 | Adiciona Sprint 2 | [Gabriel Lima](https://github.com/gabriel-lima258) |
| 08/06/2026 | 1.3 | Adiciona Sprint 3 | [Gabriel Lima](https://github.com/gabriel-lima258) |

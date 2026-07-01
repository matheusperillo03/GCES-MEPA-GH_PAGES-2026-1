# Objetivo

A sprint 4 teve como objetivo bem semelhante as anteriores, os membros criaram issues relacionada a testes que foram desenvolvidas e resolvidas na Sprint.

## Issue 77

Foi identificado que os componentes de nós visuais utilizados na renderização de diagramas da área administrativa (`src/app/admin/components`) necessitavam de uma validação de suas interações e a falta de testes.

### Componentes de Nós (React Flow)

Os arquivos contemplados no escopo de testes de nós gráficos estão no MR 88  foram:

- `consumer-unit-node.tsx`
- `meter-node.tsx`

**O que foi testado:** - **Renderização e Estados:** Exibição correta de dados de Unidades Consumidoras (nome da UC, número, status Ativa/Inativa, fallbacks de tradução e tratamento de siglas/nomes das distribuidoras) e de Medidores (números de série, identificadores contextuais, badges dinâmicos de "Carga" vs "Gerador" e labels de modelo).
- **Propagação de Eventos:** Validação estrita do comportamento de clique nos botões internos "Ver UC" e "Ver Medidor", garantindo que a execução do callback `onView` dispare corretamente e acione o método `stopPropagation`, impedindo que cliques em elementos internos ativem eventos indesejados no nó pai ou na área de manipulação (canvas) do React Flow.
- **Mocks e Infraestrutura:** Isolamento completo do módulo externo `reactflow` simulando os conectores `Handle` e o objeto de posicionamento `Position` diretamente no DOM virtual do Vitest, além de mocks para ícones do `lucide-react` (`Zap`, `Eye`) e componentes atômicos de UI (`Badge`, `Button`).

**Resultado:** Os dois arquivos alcançaram cobertura máxima, saltando para patamares próximos de **100%** em statements, branches, functions e lines. ✅

---

### Utilitários do Painel Administrativo

Complementando o escopo da Issue #77, foram identificados arquivos utilitários do módulo `src/app/admin/components` sem cobertura de testes: funções de formatação de datas, ordenação de opções de select e extração de mensagens de erro de formulário. O MR referente à branch `37-admin-components-coverage` foi aberto para cobrir esses utilitários.

Os arquivos criados foram:

- `date-input-format.test.ts` com 35 testes de formatação e conversão de datas no padrão BR
- `select-option-sorting.test.ts` com 18 testes de ordenação e geração de labels para selects
- `form-error-message.test.ts` com 12 testes de extração e priorização de mensagens de erro

**O que foi testado:** conversão e formatação de datas entre ISO e `dd/MM/yyyy`, cobrindo casos como datas inválidas, zero-padding e anos bissextos. Também foram contempladas a ordenação alfabética e por critério de selects com labels dinâmicas, além da priorização de mensagens de erro provenientes de múltiplas fontes do formulário.

**Resultado:** 65 novos testes em 3 arquivos, com a cobertura de `admin/components` ampliada em **~20%**.

---

## Issue 76

Foi identificado que o módulo `src/utils` concentrava funções utilitárias puras amplamente reutilizadas na aplicação, abrangendo formatação monetária, mapeamento de status fotovoltaico, manipulação de datas e exibição de dados de medidores, todas com cobertura de testes nula. O MR foi aberto na mesma branch `37-admin-components-coverage`, totalizando **172 novos testes** no conjunto das duas issues, aguardando pipeline e aprovação.

### Utilitários de Utils

Os arquivos criados foram:

- `currency.test.ts` com 8 testes de formatação de valores monetários com locale `pt-BR`
- `pv-availability.test.ts` com 18 testes de mapeamento de status de disponibilidade fotovoltaica
- `dateUtils.test.ts` com 26 testes de formatação, conversão e validação de datas
- `meter-display.test.ts` com 17 testes de formatação e exibição de dados de medidores
- `meter-event-display.test.ts` com 28 testes de formatação e exibição de eventos de medidores

**O que foi testado:** formatação monetária e métrica com locale `pt-BR` e mapeamento completo de status fotovoltaico. Foram cobertos também a formatação de início e fim de dia para strings ISO e `dd/MM/yyyy`, o cálculo de diferença em horas, a validação de intervalo e os casos de borda, além da formatação e exibição de atributos e eventos de medidores.

**Resultado:** 107 novos testes em 5 arquivos, com a cobertura de `src/utils` ampliada em **~20%**.

---

## Issue 80

Foi identificado que o módulo `src/app/instituicoes` — responsável pelo painel de instituições, pela visualização em grafo (React Flow) da hierarquia de entidades e medidores, pelas *server actions* de consumo da API e pelos utilitários de montagem da árvore de medidores — concentrava grande volume de código sem cobertura de testes. O MR referente a essa issue foi aberto para cobrir as *server actions*, os componentes de cliente (incluindo os grafos interativos) e os utilitários puros do módulo, estabelecendo como meta uma cobertura superior a **90%**.

### Server Actions e Utilitários

Os arquivos criados/ampliados foram:

- `actions.ts` (raiz) — testes de busca de entidades, árvore, medidores, UCs, plantas FV, período de medição mais recente (com paginação e normalização) e mutações (criar/atualizar/patch/excluir) com revalidação de cache
- `[instituicaoId]/actions.ts` — testes das *actions* de relatórios financeiros e de sustentabilidade
- `institution-meter-tree.test.ts` — ampliação dos casos de enriquecimento da árvore de medidores

**O que foi testado:** normalização dos diferentes formatos de resposta da API (`data` / `results` / `items` / array cru), tratamento de ausência de token de sessão, paginação completa, mapeamento de medidores de grafo e de entidade, resolução do período mais recente com tratamento de respostas `204`/`404` e datas inválidas, além da revalidação de tags de cache. Nos utilitários, foi coberta a resolução de entidades por `id` numérico, string e sigla, casos de referência ambígua e medidores sem correspondência.

### Componentes de Cliente e Grafos (React Flow)

Os arquivos criados foram:

- `institution-flow-viewer.test.tsx` e `institution-meters-graph.test.tsx` — grafos interativos (busca/focalizador, zoom, centralização, tela cheia e tema por status do medidor)
- `institution-master-detail.test.tsx` — árvore lateral, filtro, painel de detalhes, alertas por severidade, medidores diretos/indiretos e navegação entre sub-instituições
- `institution-meters-graph-section.tsx`, `meters-map-section.tsx`, `institution-view-node`/`meter-view-node` (complementos), `institution-skeleton`, `entities-error-state`, `institution-flow-viewer-wrapper`
- `page.tsx` (Painel raiz) — *skeleton* de carregamento, cards de métrica, gráfico mensal, *fallback* de período e modal de alertas
- `error.tsx`, `loading.tsx`, páginas de *redirect* (`[instituicaoId]`, `grafo`, `hierarquia`) e `interactive`/`report`

**O que foi testado:** renderização e estados dos componentes, propagação e *stopPropagation* de cliques nos nós, fluxo de abertura/seleção/fechamento do modal de alertas com navegação, resolução de período de *fallback*, ramificações de erro e estados vazios. A infraestrutura incluiu o isolamento completo de `reactflow` e `dagre`, mocks dos *hooks* de dados (`useEntityDetail`, `useActiveMeterEvents`, `useMeters`, `usePageTransition`), das *server actions* e dos componentes de UI atômicos, além do *stub* de APIs do DOM não implementadas pelo `happy-dom` (`scrollTo`, `requestAnimationFrame`, `window.print`).

**Resultado:** mais de **130 novos testes** em 20 novos arquivos (157 testes no escopo de `instituicoes`, todos passando), elevando a cobertura de praticamente todos os grupos de **0–6%** para patamares acima de **90%** — com diversos arquivos atingindo **100%**. ✅

| Grupo | Stmts (antes → depois) | Lines (antes → depois) |
| --- | --- | --- |
| `instituicoes` (raiz) | 0% → **94,87%** | 0% → **96,44%** |
| `instituicoes/components` | 5,64% → **95,06%** | 6,04% → **97,66%** |
| `[instituicaoId]` | 0% → **100%** | 0% → **100%** |
| `[instituicaoId]/components` | 0% → **100%** | 0% → **100%** |
| `instituicoes/grafo` | 0% → **100%** | 0% → **100%** |
| `[instituicaoId]/grafo` | 0% → **100%** | 0% → **100%** |
| `[instituicaoId]/hierarquia` | 0% → **100%** | 0% → **100%** |
| `instituicoes/utils` | 85,33% → **97,33%** | 88,52% → **100%** |

## Issue 81

Foi identificado que o módulo src/app/entidades/[entidadeId]/performance — responsável pela página de monitoramento de desempenho das plantas fotovoltaicas (cards de produção, temperatura, irradiância, potência atual e taxa de desempenho, gráficos diários/mensais, alertas de medidores e exportação de relatórios) — estava com 0% de cobertura de testes, apesar de concentrar, isoladamente, mais linhas do que diversas issues anteriores somadas. [Issue 81](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/work_items/81). O [MR referente à branch est/81-entity-performance](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests/101) foi aberto para cobrir a lógica de cálculo/agregação, as server actions e os componentes de UI do módulo, com meta de cobertura de linhas igual ou superior a 80%.

  ### Lógica de Cálculo e Server Actions

  Os arquivos criados foram:

  - performance.mappers.test.ts — formatação de datas/períodos no fuso America/Sao_Paulo, formatação de números/energia/moeda, derivação de tonalidade e
  texto de status de desempenho (Adequado/Precário/Crítico), mapeamento dos gráficos de geração e irradiância diários a partir da resposta da API, e
  normalização da taxa de desempenho mensal (percentual → razão 0–1)
  - actions.test.ts — busca paralela dos dados de performance/live/dia com fallback independente para null em caso de falha de qualquer uma das três
  chamadas, paginação e deduplicação de eventos ativos por medidor, e ordenação por data mais recente
  
  O que foi testado: parsing e validação de parâmetros de período/data vindos da URL, cálculo do último dia do período quando não é o período atual, busca e
  correspondência de traces de gráfico por apelidos/termos (com exclusão de termos conflitantes, como "esperada" vs. "medida"), e tratamento de erros de
  rede isolado por requisição via serverFetcher.

  ### Página e Componentes de Interação
  
  Os arquivos criados foram:

  - page.test.tsx — ramificações de notFound() (entidade inválida, sessão sem permissão de visualizar plantas, dados de performance ausentes) e renderização
  completa dos cards/links condicionados às permissões da sessão (medidores e relatórios)
  - performance-alerts-button.test.tsx — alertas por entidade (sem meterIds) e por medidores específicos, estado de carregamento, fallback de alertas e
  navegação ao selecionar um alerta (incluindo o fluxo de retorno ao mapa)
  - performance-charts-section.test.tsx — cache em memória/sessionStorage dos gráficos diários ao trocar a data filtrada e recarregamento via navegação
  popstate
  - performance-daily-date-filter.test.tsx — navegação entre dias, limites de data mínima/atual e abertura do calendário
  - performance-info-tooltip.test.tsx — fixação por clique, fechamento por Escape/clique externo e exibição por hover
  - performance-generation-chart.calculations.test.ts e performance-generation-chart.render.test.tsx — funções puras de agregação temporal (hora/dia/mês),
  janelas de zoom/filtro de data, geração de séries para download em CSV/PDF, e renderização dos gráficos de geração/irradiância/taxa de desempenho (vazio,
  com dados, séries desativadas, barra vs. linha)
  - not-found.test.tsx — estado vazio de permissão específico da planta

  O que foi testado: mocks das server actions, dos hooks de navegação do Next (useRouter, usePathname, useSearchParams) e das dependências de geração de
  PDF/imagem (html2canvas, jsPDF), permissões via canViewAdminResource/canViewRebacScope, e simulação de tempo do sistema (vi.setSystemTime) para tornar
  deterministas os filtros relativos de data ("Última hora", "Hoje", "Últimos 7 dias" etc.).

  Resultado: 200 novos testes em 10 arquivos, todos passando, elevando a cobertura da pasta de 0% para 88,8% de linhas — acima da meta de 80% definida nos
  critérios de aceitação.

  | Arquivo | Stmts (antes → depois) | Lines (antes → depois) |
  | --- | --- | --- |
  | performance.mappers.ts | 0% → 99,45% | 0% → 100% |
  | actions.ts | 0% → 100% | 0% → 100% |
  | page.tsx | 0% → 100% | 0% → 100% |
  | not-found.tsx | 0% → 100% | 0% → 100% |
  | performance-info-tooltip.tsx | 0% → 97,22% | 0% → 100% |
  | performance-daily-date-filter.tsx | 0% → 82,6% | 0% → 91,66% |
  | performance-charts-section.tsx | 0% → 87,5% | 0% → 92,98% |
  | performance-alerts-button.tsx | 0% → 87,36% | 0% → 90,69% |
  | performance-generation-chart.tsx | 0% → 81,68% | 0% → 82,73% |
  | Total da pasta | 0% → 87,04% | 0% → 88,8% |

  Durante a escrita dos testes, foi identificado um bug em produção: buildDisabledLabelRanges (usada por PerformanceGenerationChart/PerformanceBackendChart)
  lança uma exceção quando um intervalo de status "desativado" se estende até o último ponto de dados da série — um cenário realista sempre que um medidor
  permanece indisponível até o fim do período filtrado. O achado foi documentado e reproduzido por um teste dedicado, mas a correção foi deixada para um MR
  de bugfix separado, já que o escopo desta issue era exclusivamente cobertura de testes. 


---

### Análises e Calendário (MR !78)

Complementando o escopo da Issue #77, foram identificados e corrigidos testes quebrados nos módulos de **Análises** e **Calendário** da área administrativa.

**Arquivos corrigidos/criados:**
- `calendario/page.test.tsx` — 3 testes de renderização e estados do calendário mensal
- `analises/page.test.tsx` — 4 testes de análise de dados, filtros e exportação

**O que foi testado:** renderização de estados vazio, erro e com dados no calendário mensal; correção de mocks de `mepaAPI.get` para `fetch` global (alinhando com a implementação real); validação do componente `ErrorMessage` genérico; fluxos de resumo, loading e erro em análises.

**Resultado:** 7 testes corrigidos/validados, elevando a cobertura de `calendario/page.tsx` de **0% para 75,34%** e de `analises/page.tsx` de **0% para 54,54%**.

## Histórico de Versão

| Data       | Versão | Descrição                                             | Autor                                                 |
| ---------- | ------ | ----------------------------------------------------- | ----------------------------------------------------- |
| 22/06/2026 | 1.0    | Criação da Sprint 4     | [Marcos Bezerra](https://github.com/marcoslbz)        |
| 22/06/2026 | 1.1    | Adicionando Issues 77 (utilitários) e 76 (utils) | [Matheus Barros](https://github.com/Ninja-Haiyai) |
| 23/06/2026 | 1.2    | Adicionando Issue 80 | [Vitor Hoffmann](https://github.com/vitor-hoffmann) |
| 23/06/2026 | 1.3    | Adicionando Issue 81 | [Caio Sabino](https://github.com/caiomsabino) |
| 01/07/2026 | 1.4    | Adicionando Análises/Calendário (MR !78) na Issue 77  | [Bruno Araújo](https://github.com/brunocva)           |

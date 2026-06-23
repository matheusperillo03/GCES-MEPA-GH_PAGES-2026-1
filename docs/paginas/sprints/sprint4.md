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

---

## Histórico de Versão

| Data       | Versão | Descrição                                             | Autor                                                 |
| ---------- | ------ | ----------------------------------------------------- | ----------------------------------------------------- |
| 22/06/2026 | 1.0    | Criação da Sprint 4     | [Marcos Bezerra](https://github.com/marcoslbz)        |
| 22/06/2026 | 1.1    | Adicionando Issues 77 (utilitários) e 76 (utils) | [Matheus Barros](https://github.com/Ninja-Haiyai) |
| 23/06/2026 | 1.2    | Adicionando Issue 80 | [Vitor Hoffmann](https://github.com/vitor-hoffmann) |

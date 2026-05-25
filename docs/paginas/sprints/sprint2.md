# Objetivo

A sprint 2 teve como objetivo identificar oportunidades de abertura de issue no ramo de testes automatizados e resolvê-las, contribuindo assim com MRs que aumentassem a cobertura de testes do projeto.

## Issue 73

Foi identificado que não haviam testes automatizados para a geração de relatórios e dos geradores PDF do projeto. Com isso, foram divididas tarefas para os três tipos de relatórios presentes no repositório, a fim de elencar os testes a serem feitos, como fazer e suas motivações.

### Relatório Financeiro

O relatório financeiro possui 3 arquivos principais para teste:

- `buildFinancialReportPdfData`
- `FinancialReportPdfData`
- `FinancialReportPdfActions`

#### `buildFinancialReportPdfData.ts`
Função pura responsável por transformar o payload da API (`FinancialReportApiData`) em uma estrutura tipada (`FinancialReportPdfData`) consumida pelo documento PDF. Ela concentra toda a lógica de formatação: moeda (pt-BR), datas ISO, fallbacks diferenciados para `null`/`undefined`/`""`, cálculo de percentuais de composição de custo, montagem das três tabelas de histórico (demanda, energia e totais) e inclusão condicional do glossário.

**O que foi testado:** montagem completa do payload; todos os helpers internos (`safeText`, `formatDateOrFallback`, `formatContractDemand`, `safePercent`, `formatMonthYearLabel`, `getHistoryTotalValue`, `buildFinancialWarnings`); fallbacks para cada tipo de ausência de dado; propagação de assets e chartImages; glossário condicional; zero-padding do mês.

**Resultado:** 25 testes  — LH ~90% · Branches ~82%

---

#### `FinancialReportPdfDocument.tsx`
Componente React que recebe a `FinancialReportPdfData` e renderiza a árvore do documento PDF usando `@react-pdf/renderer` (capa, introdução, tabela de medidores, linhas de contrato, info items de custo/economia, subsection de composição com figura e Tabela 3, tabelas de histórico e glossário).

**O que foi testado:** renderização sem crash com stub DOM-safe do `@react-pdf/renderer`; presença dos elementos estruturais (`Document`, `Page`); conteúdo de capa (título, entidade, universidade, UC); parágrafos de introdução e linhas de contrato; info items financeiros; snapshot completo da árvore HTML gerada pelo mock.

**Resultado:** 5 testes  + 1 snapshot versionado — LH ~100% · Branches ~95%

---

#### `FinancialReportPdfActions.tsx`
Componente React client-side que orquestra a geração e o download/preview do PDF. Internamente captura o gráfico de composição via `html-to-image`, monta o payload com `buildFinancialReportPdfData`, gera o blob com `@react-pdf/renderer` e dispara o download ou abre uma nova aba. Exporta dois helpers puros: `sanitizeFileName` (normalização NFD, remoção de caracteres reservados, colapso de espaços/dashes) e `buildPdfFileName` (nome final do arquivo com mês zero-padded e fallback de entidade).

**O que foi testado:** apenas os dois helpers puros exportados. O componente em si e os helpers assíncronos de DOM (`captureFigure`, `waitForChartRender`, `captureAllFigures`) não foram cobertos pois dependem de `requestAnimationFrame`, `document.fonts.ready`, `URL.createObjectURL` e `window.open` — APIs de browser fora do escopo desta MR.

**Resultado:** 9 testes  — LH ~22% · Branches ~18% (A cobertura do FinancialReportActions é baixa pois o arquivo exporta dois helpers puros, sanitizeFileName e buildPdfFileName, que são as únicas funções testadas nesta MR. Esses helpers concentram toda a lógica de negócio relevante do arquivo: normalização de nomes de arquivo com diacríticos, remoção de caracteres reservados de filesystem e montagem do nome final do PDF com mês zero-padded e fallback de entidade.)

## Issue 75

Foi identificado que os módulos de Pessoas, Mapa e Painel não possuíam cobertura adequada de testes automatizados — com 954 linhas instrumentáveis e coberturas variando de 0% a 49%. Com isso, as tarefas foram divididas entre três integrantes, cada um responsável por um módulo distinto.

### Mapa

O módulo de Mapa possuía cobertura de 49% no módulo principal e 21% nos componentes, com três arquivos pesados (`map-explorer`, `map-explorer-markers` e `map-explorer-sidebar`) praticamente sem testes.

Os arquivos contemplados foram:

- `entity-icons.ts`
- `page.tsx`
- `map-explorer-sidebar.tsx`
- `map-explorer.tsx`
- `map-explorer-markers.tsx`

**O que foi testado:** callbacks de marcadores (`onMarkerClick`, `onMeterClick`); renderização do mapa e da sidebar; alternância de visualizações; mock do Leaflet com exports nomeados e default simultâneos; mock de `next/dynamic` com resolução assíncrona; rollback otimista e tratamento de erros.

**Resultado:** 63 novos testes em 5 arquivos — Mapa (total): 49% → **91%** ✅ · Mapa/components (total): 21% → **78%** ✅ — Metas atingidas (mapa ≥80%, mapa/components ≥70%)

---

### Pessoas

_A ser preenchido por Matheus Barros._

---

### Painel

_A ser preenchido por Marcos Bezerra._

---

| Data     | Versão | Descrição             | Autor               |
| -------- | ------ | --------------------- | ------------------  |
| 24/05/2026 | 1.0  | Estruturando a Sprint e adicioando a colaboração | [Caio Sabino](https://github.com/caiomsabino) |
| 24/05/2026 | 1.1  | Adiciona documentação da Issue 75 (parte Mapa) | [Matheus Perillo](https://github.com/matheusperillo03) |

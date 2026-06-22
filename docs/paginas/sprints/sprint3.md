# Objetivo

A sprint 3 teve como objetivo continuar identificando oportunidades de abertura de issue no ramo de testes automatizados e resolvê-las, contribuindo assim com MRs que aumentassem a cobertura de testes do projeto.

## Issue 76

Foi identificado que os módulos de componentes raiz (`src/components`), gráficos (`src/components/charts`) e stories (`src/stories`) não possuíam cobertura adequada de testes automatizados — totalizando 1.086 linhas instrumentáveis com coberturas variando de 0% a 21%. Com isso, a [Issue #76](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/work_items/76) foi aberta e o [MR #86](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests/86) foi criado para resolvê-la.

### Componentes Raiz

O módulo `src/components` possuía cobertura de apenas 21%, com componentes críticos amplamente reutilizados na aplicação — como `ErrorBoundary`, `MetricCard` e `ReportsDateFilter` — sem nenhuma cobertura de teste.

Os principais arquivos contemplados foram:

- `ErrorBoundary` (componente de classe com lógica de retry)
- `LoadingSuspense` (useState com timer)
- `MetricCard`
- `ReportsDateFilter`

**O que foi testado:** renderização dos componentes sem crash; lógica de retry do `ErrorBoundary`; comportamento do `LoadingSuspense` com timer; validação de datas futuras no `ReportsDateFilter`; mocks de `swr`, `next/navigation` e `next/router`.

**Resultado:** `src/components`: 0% → **75,52%** ✅ — Meta ≥70% atingida

---

### Charts

O módulo `src/components/charts` estava com 0% de cobertura e continha lógica complexa de normalização de séries temporais, algoritmos de zoom, polling em tempo real e renderização com `recharts`.

Os principais arquivos contemplados foram:

- `MonthlyEnergyChart` (494 linhas)
- `ChartCard` (261 linhas)

**O que foi testado:** renderização dos gráficos com dados válidos e séries vazias; polling de dados e tratamento de falhas gracioso; lógica de zoom e normalização de séries temporais; mocks estratégicos do `recharts` e `swr`.

**Resultado:** `src/components/charts`: 0% → **73,21%** ✅ — Meta ≥70% atingida

---

### Stories

Os módulos de stories (`src/stories/blocks`, `src/stories/__fixtures__` e `src/stories/foundations/components`) estavam com 0% de cobertura. Eles funcionam como contratos visuais e fixtures compartilhadas de teste.

**O que foi testado:** smoke tests para 23 arquivos `.stories.tsx`; presença e montagem dos blocos, fixtures e componentes de fundação.

**Resultado:**

| Módulo | Antes | Depois | Meta |
| ------ | ----- | ------ | ---- |
| `src/stories/blocks` | 0% | **66,66%** | ≥60% ✅ |
| `src/stories/__fixtures__` | 0% | **76%** | ≥60% ✅ |
| `src/stories/foundations/components` | 0% | **100%** | ≥70% ✅ |

---

## Issue 77

Foi identificado que o módulo `src/app/admin/components` apresentava diversos arquivos com cobertura de testes baixa ou nula, abrangendo desde componentes de nós do diagrama até as telas de gestão do painel administrativo. A [Issue #77](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/work_items/77) foi aberta pelo Marcos, que resolveu parte dela através do [MR !85](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests/85), e o restante do escopo foi resolvido através do [MR !88](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests/88).

### Componentes do Painel Administrativo

Os arquivos contemplados no MR !88 foram:

- `entity-node.tsx`
- `canvas-controls.tsx`
- `admin-unified-page.tsx`
- `meters-management.tsx`

**O que foi testado:** renderização condicional dos nós do diagrama (handles de conexão, contagem de filhos e medidores, fallback de tradução); navegação entre as abas do painel administrativo com sincronização da URL e preservação das abas já visitadas; zoom, criação de nós, undo e limpeza de histórico do canvas; busca, filtragem por aba e estados de carregamento/erro/vazio da listagem de medidores.

**Resultado:** os quatro arquivos saltaram de **0%** para praticamente **100%** de cobertura em statements, branches, functions e lines.

> 💡 A única branch não coberta de `entity-node.tsx` (linha 186, `parentId ?? null`) é um fallback defensivo inalcançável, já que o bloco só é renderizado quando `parentId !== null && parentId !== undefined`.

---

### Utilitários do Painel Administrativo

Complementando o escopo da Issue #77, foram identificados arquivos utilitários do módulo `src/app/admin/components` sem cobertura de testes: funções de formatação de datas, ordenação de opções de select e extração de mensagens de erro de formulário. O [MR referente à branch `37-admin-components-coverage`](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web) foi aberto para cobrir esses utilitários, aumentando a cobertura do módulo em ~20%.

Os arquivos criados foram:

- `date-input-format.test.ts` com 35 testes de formatação e conversão de datas no padrão BR
- `select-option-sorting.test.ts` com 18 testes de ordenação e geração de labels para selects
- `form-error-message.test.ts` com 12 testes de extração e priorização de mensagens de erro

**O que foi testado:** conversão e formatação de datas entre ISO e `dd/MM/yyyy`, cobrindo casos como datas inválidas, zero-padding e anos bissextos. Também foram contempladas a ordenação alfabética e por critério de selects com labels dinâmicas, além da priorização de mensagens de erro provenientes de múltiplas fontes do formulário.

**Resultado:** 65 novos testes em 3 arquivos, com a cobertura do módulo `admin/components` ampliada em **~20%**.

---

## Issue 78

Foi mapeado que os módulos que compõem o ecossistema do Design System — incluindo componentes de interface de usuário (`src/components/ui`) e carregamento estrutural (`src/components/skeletons`) — contavam com uma cobertura crítica inicial de apenas ~15%, totalizando 968 linhas instrumentáveis. Para solucionar essa defasagem, a suíte de testes foi expandida com a criação de **45 novos arquivos de teste** (43 para a UI e 2 para Skeletons), adicionando **411 novos casos de teste** totalmente integrados e validados.

### Design System: UI + Skeletons

O escopo desta issue abrangeu 947 linhas do módulo `ui` e 21 linhas do módulo `skeletons`, garantindo a confiabilidade desde elementos primitivos até estruturas complexas de navegação e exibição de dados.

Os principais arquivos e fluxos contemplados foram:

- **Componentes Primitivos:** Garantia de comportamento e renderização de estados de componentes base (como `Badge`, `Button`, `Input`, `Switch`, entre outros).
- **Componentes Complexos de Interface:**
  - `Sidebar`: Comportamento de alternância responsiva (mobile/desktop/none), acionamento via atalhos de teclado e validação das propriedades do hook `useSidebar`.
  - `Chart`: Resolução de chaves de configuração nativas (`nameKey`, `labelKey`), tratamento de payloads customizados e integração estrutural com mocks adaptados para o `ResponsiveContainer` da biblioteca `recharts`.
  - `ConditionalLayout`: Validação dos fluxos lógicos e isolamento de renderização nas ramificações de autenticação (`auth`) e aplicação (`app`).
  - Estruturas de controle e popovers avançados: `StandardDrawer`, `Form`, `Select`, `DropdownMenu`, `Calendar` e `DateFilterSelectPopover`.
- **Mocks e Infraestrutura:** Configuração de mocks específicos para simular o comportamento de `pointer-capture` exigido pelo Radix UI, além do isolamento de dependências de `next/navigation`, `next/image` e `sonner`.

**O que foi testado:** Renderização rigorosa livre de falhas estruturais, fluxos condicionais defensivos, acionamento de callbacks internos, formatação e tratamento dinâmico de dados e respostas visuais de componentes de esqueleto.

**Resultado:**

| Módulo | Stmts | Branch | Funcs | Lines | Antes | Meta |
| ------ | ----- | ------ | ----- | ----- | ----- | ---- |
| `src/components/ui` | 98,93% | 90,20% | 98,95% | 99,07% | ~15% | ≥90% ✅ |
| `src/components/skeletons` | 100,00% | 100,00% | 100,00% | 100,00% | ~15% | ≥90% ✅ |
| **Total do Escopo** | **98,95%** | **90,40%** | **99,00%** | **99,08%** | **~15%** | **≥90% ✅** |

> 💡 **Nota de Execução:** Visando manter a árvore de configurações original do projeto intacta, o arquivo `vitest.config.mts` não foi modificado. Devido a isso, os arquivos `.stories.tsx` continuam sendo computados no relatório de cobertura padrão da aplicação. Para inspecionar o índice real e isolado dos componentes de código do Design System (desconsiderando os stories), pode-se executar o comando em linha:
> ```bash
> pnpm exec vitest run --coverage \
>   --coverage.include='src/components/ui/**' \
>   --coverage.include='src/components/skeletons/**' \
>   --coverage.exclude='**/*.stories.tsx'
> ```

---

## Issue 79

Foi identificado que os módulos centrais da aplicação — `src/lib/errors`, `src/utils` e `src/hooks` — concentravam lógica de negócio crítica amplamente reutilizada em toda a aplicação, mas sem nenhuma cobertura de testes automatizados. A [Issue #79](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/work_items/79) foi aberta para mapear e cobrir esses módulos, e o [MR !89](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests/89) foi criado para resolvê-la.

### Core: Lib, Utils e Hooks

Os módulos contemplados abrangem desde o tratamento padronizado de erros da API até a formatação de datas e valores monetários, passando pelo controle de estado de formulários com validação de datas.

Os principais arquivos contemplados foram:

- `src/lib/errors/error-parser.ts`
- `src/utils/dateUtils.ts`
- `src/utils/currency.ts`
- `src/utils/pv-availability.ts`
- `src/hooks/useDebounce.ts`
- `src/hooks/useDateValidation.ts`

**O que foi testado:** extração de mensagem de erro a partir de múltiplos formatos (`string`, `Error`, objetos de API com `.message`, `.error`, `.detail` e `.msg`); match por status HTTP com precedência sobre padrões textuais; categorização completa de erros e helpers de conveniência (`isAuthError`, `isConnectionError`, `isServerError`, `isValidationError`, `formatErrorMessage`, `formatErrorFull`); formatação de início e fim de dia para strings ISO e `dd/MM/yyyy`; cálculo de diferença em horas, validação de intervalo e lógica de zoom de gráfico com timers mockados via `vi.setSystemTime`; formatação de valores monetários e métricas com locale `pt-BR`; mapeamento de status de disponibilidade fotovoltaica; comportamento de debounce com cancelamento de chamadas intermediárias e cleanup ao desmontar; e controle de estado de erros por índice em `useDateValidation`.

### Cobertura Obtida

| Módulo | Stmts | Branch | Funcs | Lines | Antes |
| ------- | ----- | ------ | ----- | ----- | ----- |
| `src/utils/currency.ts` | 100% | 100% | 100% | 100% | 0% |
| `src/utils/pv-availability.ts` | 100% | 100% | 100% | 100% | 0% |
| `src/hooks/useDebounce.ts` | 100% | 100% | 100% | 100% | 0% |
| `src/utils/dateUtils.ts` | 96,22% | 100% | 100% | 95,91% | 0% |
| `src/lib/errors/error-parser.ts` | 94,73% | 84% | 100% | 93,87% | 0% |
| `src/hooks/useDateValidation.ts` | 82,25% | 69,23% | 80% | 82,14% | 0% |
| **Total do Escopo** | **92,38%** | **89,56%** | **92,72%** | **92,06%** | **0%** |

> 💡 **Nota de Cobertura:** As linhas não cobertas correspondem a branches defensivos inalcançáveis no ambiente de testes: o bloco `catch` do `JSON.stringify` em `error-parser.ts` (linha 43) e o caminho `process.env.NODE_ENV === "development"` (linha 76), que nunca é atingido porque o ambiente `happy-dom` sempre expõe `window`; as linhas 17 e 51 de `dateUtils.ts`, referentes ao `return null` do caminho sem separador de data e ao `return String(error)` nunca alcançado após o bloco `try/catch`; e as funções `handleLocalBlur` (linhas 40–46) e `setLocalDateErrorAtIndex` (linhas 82–85) de `useDateValidation.ts`, que operam sobre o array interno de erros de subgráficos e não foram exercitadas nos cenários implementados.

**Resultado:** os 6 arquivos passaram a contar com cobertura abrangente de testes automatizados, totalizando **67 testes**, todos passando. ✅

---

## Issue 73 (Complementar)

Foi identificado que o módulo de relatórios PDF do MEPA Web possuía cobertura de testes incompleta, com atenção especial ao Relatório Técnico (`technical-report`). A [Issue #73](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/work_items/73) foi aberta e já havia recebido cobertura parcial para o Relatório Financeiro através do [MR !75](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests/75). O restante do escopo, focado no módulo `technical-report`, foi resolvido através de um MR separado e complementar.

### Relatório Técnico (technical-report)

Os arquivos contemplados no MR complementar foram:

- `buildTechnicalReportPdfData.ts` (ampliação da suíte de testes)
- `technicalReportPdfFileName.ts` (criação do arquivo e testes)

**O que foi testado:** montagem da estrutura de dados usada pelo PDF técnico; formatação de datas, valores nulos, vazios, indefinidos e fallbacks textuais; inclusão e omissão corretas das seções opcionais de DHT; renumeração correta de tabelas e figuras; extração de helper puro para nome de arquivo, eliminando dependências de browser nos testes.

**Resultado:** os comportamentos mais importantes do Relatório Técnico foram cobertos, seguindo o mesmo padrão já consolidado no Relatório Financeiro.

> 💡 Algumas partes do fluxo de geração de PDF dependem de APIs de browser e bibliotecas pesadas (captura de imagens do DOM, geração real via `@react-pdf/renderer`). Optou-se por não testar diretamente esses trechos nesta etapa, isolando helpers puros e testando a transformação de dados.

---

### Utilitários do Relatório Técnico

Complementando o escopo da Issue #73, foi extraído e testado um helper puro responsável pela geração do nome do arquivo do Relatório Técnico, anteriormente embutido em um módulo com dependências de browser.

Os arquivos criados/ampliados foram:

- `technicalReportPdfFileName.test.ts` — testes para cenários de nome de arquivo
- `buildTechnicalReportPdfData.test.ts` — ampliação com novos cenários de teste

**O que foi testado:** geração correta do nome do arquivo do Relatório Técnico; tratamento de dados nulos, vazios e indefinidos na montagem da estrutura do PDF; fallbacks textuais para valores ausentes; lógica de inclusão/omissão de seções opcionais de DHT; renumeração automática de tabelas e figuras.

**Resultado:** nova suíte de testes para o Relatório Técnico, seguindo o padrão já consolidado no módulo financeiro e isolando responsabilidades puras de dependências externas ✅

---


| Data     | Versão | Descrição             | Autor               |
| -------- | ------ | --------------------- | ------------------  |
| 05/06/2026 | 1.0  | Estruturando a Sprint 3 e adicionando a documentação da Issue 76 | [Matheus Perillo](https://github.com/matheusperillo03) |
| 07/06/2026 | 1.1  | Adicionando a documentação da Issue 78 (Design System: UI + Skeletons) | [Vitor Hoffmann](https://github.com/vitor-hoffmann) |
| 07/06/2026 | 1.2  | Adicionando a documentação da Issue 77 (Admin Components) | [Caio Sabino](https://github.com/caiomsabino) |
| 08/06/2026 | 1.3  | Adicionando a documentação da Issue 79 (Core: Lib, Utils e Hooks) | [Ranni Heler](https://github.com/akaeranni) |
| 08/06/2026 | 1.4  | Adicionando a documentação dos Utilitários do Painel Administrativo (Issue 77) | [Matheus Barros](https://github.com/Ninja-Haiyai) |
| 08/06/2026 | 1.5  | Adicionando a documentação da Issue 73 (Relatório Técnico - PDF) | [Bruno Vasconcelos](https://github.com/brunocva) |

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

| Data     | Versão | Descrição             | Autor               |
| -------- | ------ | --------------------- | ------------------  |
| 05/06/2026 | 1.0  | Estruturando a Sprint 3 e adicionando a documentação da Issue 76 | [Matheus Perillo](https://github.com/matheusperillo03) |
| 07/06/2026 | 1.1  | Adicionando a documentação da Issue 78 (Design System: UI + Skeletons) | [Vitor Hoffmann](https://github.com/vitor-hoffmann) |

# Diário de Bordo - Vitor Valerio Hoffmann

Esta seção tem como objetivo registrar, ao longo das sprints, o acompanhamento individual das atividades realizadas por cada integrante do grupo.

A cada sprint, cada membro irá documentar sua experiência no projeto, descrevendo as tarefas realizadas, dificuldades encontradas, decisões tomadas e aprendizados adquiridos durante o processo de contribuição no MEPA. Além disso, o diário de bordo funciona como um histórico do desenvolvimento do projeto, tornando rastreável o processo de contribuição em um ambiente de software livre.

---

## Sprint 0 - Documentação
**Duração**: 06/04/2026 - 22/04/2026

### Resumo da Sprint

Nesta sprint, o foco principal foi o estudo inicial da arquitetura do projeto MEPA, o mapeamento de oportunidades de contribuição e a adaptação às ferramentas utilizadas pelos mantenedores. Além disso, iniciei as tentativas de configuração do ambiente de desenvolvimento local e atuei em conjunto com a equipe para estruturar a documentação das issues no GitHub Pages.

### Atividades Realizadas

| Data | Atividade | Tipo | Referência | Status |
| ----- | --------- | ---------------------------------------- | --------------- | ------ |
| 15/04 | Estudo da estrutura do repositório MEPA | Estudo | [Repositório MEPA](https://gitlab.com/lappis-unb/projetos-energia/mepa) | Concluído✅ |
| 17/04 | Configuração do ambiente de desenvolvimento (Linux) | Configuração | Local | Em andamento⏳ |
| 18/04 | Investigação e mapeamento de issues (fácil, média e difícil) | Análise | Issues do Repositório | Concluído✅ |
| 19/04 | Reunião com o Ranni para divisão das tarefas de documentação | Organização | Comunicação Interna | Concluído✅ |
| 21/04 | Documentação de parte das issues mapeadas | Doc | GitHub Pages da equipe | Concluído✅ |

### Maiores Avanços

- Consegui entender de forma geral como o projeto funciona e como a sua estrutura está organizada;
- Realizei um mapeamento estratégico das issues abertas, categorizando-as por nível de dificuldade para facilitar as próximas etapas;
- Iniciei a estruturação da documentação no GitHub Pages em parceria com o Ranni.

### Dificuldades

Encontrei alguns obstáculos iniciais, principalmente técnicos e de organização. A configuração do ambiente no meu sistema Linux tem sido um desafio por se tratar de um projeto novo e complexo. Além disso, a falta de familiaridade com o GitLab (já que estou mais acostumado com o GitHub) e a dificuldade de entender exatamente como o fluxo de contribuição funciona no repositório atrasaram um pouco o processo prático.

No aspecto da equipe, tivemos dificuldade em encontrar um horário em comum que funcionasse para todos realizarem reuniões de alinhamento.

### Aprendizados

Durante essa sprint, aprendi a navegar e utilizar o GitLab, expandindo minhas ferramentas além do GitHub. O estudo do repositório me deu uma visão clara da arquitetura do projeto. No âmbito das soft skills, compreendi a importância de priorizar e garantir tempo para se reunir com a equipe; sem esse alinhamento, é muito difícil manter um fluxo de trabalho eficiente e coeso.

### Plano Pessoal para a Próxima Sprint

Meu objetivo para a próxima sprint é compreender perfeitamente o que precisa ser entregue para a disciplina, finalizar de vez a configuração do meu ambiente de desenvolvimento local e, finalmente, puxar uma issue mapeada para começar a desenvolver.

---

## Sprint 1 - Primeira Contribuição
**Duração**: 27/04/2026 - 11/05/2026

### Resumo da Sprint

Nesta sprint, realizei minha primeira contribuição efetiva ao projeto MEPA, com foco em documentação. Após uma análise dos três repositórios do projeto, identifiquei oportunidades de melhoria na documentação de um deles: a ausência de um arquivo `CONTRIBUTING.md` e pontos de melhoria no `README.md`. Assim como outros membros do grupo, fui orientado a buscar contribuições mais acessíveis, dada a indisponibilidade dos mantenedores para preparar issues específicas neste momento.

### Atividades Realizadas

| Data | Atividade | Tipo | Referência | Status |
|------|-----------|------|------------|--------|
| 28/04 | Análise dos 3 repositórios MEPA para identificar oportunidades de contribuição | Estudo | [MEPA GitLab](https://gitlab.com/lappis-unb/projetos-energia/mepa) | Concluído ✅ |
| 08/05 | Clone do repositório alvo e criação de branch para a contribuição | Código/Doc | — | Concluído ✅ |
| 08/05 | Criação do arquivo `CONTRIBUTING.md` com diretrizes de contribuição | Doc | — | Concluído ✅ |
| 08/05 | Melhoria do `README.md` com informações mais claras e completas | Doc | — | Concluído ✅ |
| 08/05 | Abertura do Merge Request com as alterações | Código/Doc | — | Concluído ✅ |

### Maiores Avanços

- **Primeira contribuição efetiva**: Consegui abrir um Merge Request com melhorias reais na documentação do projeto, contribuindo diretamente para a experiência de novos colaboradores.
- **Criação do CONTRIBUTING.md**: A ausência desse arquivo era uma lacuna relevante no repositório, pois sem ele fica difícil para novos contribuidores entenderem como colaborar corretamente. Preencher essa lacuna foi uma contribuição de impacto direto para o onboarding da comunidade.
- **Aprendizado sobre o fluxo no GitLab**: Como tenho mais familiaridade com o GitHub, essa sprint me permitiu praticar o fluxo completo de contribuição no GitLab — fork, criação de branch, commit e abertura de MR.

### Dificuldades

- **Identificar onde contribuir**: Analisar três repositórios simultaneamente e decidir qual deles tinha a oportunidade mais adequada ao meu nível de familiaridade com o projeto exigiu tempo e critério. No fim, optei por priorizar a ausência do `CONTRIBUTING.md`, por ser uma melhoria objetiva e de alto valor para o projeto.
- **Adaptação ao GitLab**: Pequenas diferenças de interface e fluxo em relação ao GitHub geraram alguma fricção no início, mas foram superadas ao longo do processo.

### Aprendizados

- **Importância da documentação para projetos open source**: Um bom `CONTRIBUTING.md` e um `README.md` claro são fundamentais para que novos colaboradores consigam se integrar ao projeto sem depender diretamente dos mantenedores. Contribuir com isso é tão válido quanto contribuir com código.
- **Boas práticas de nomenclatura de branches**: Apliquei um padrão descritivo na criação da branch, seguindo convenções comuns em repositórios open source.
- **Autonomia na busca por contribuições**: Diante da indisponibilidade dos mantenedores para definir tarefas específicas, aprendi a identificar de forma independente onde minha contribuição poderia ser mais útil.

### Plano Pessoal para a Próxima Sprint

- **Acompanhar o MR aberto**: Monitorar se os mantenedores revisarão e aprovarão as alterações, respondendo prontamente a eventuais pedidos de ajuste.
- **Buscar novas contribuições**: Caso haja tempo e o MR seja aceito, explorar outros pontos de melhoria nos repositórios `mepa-web` ou `mepa-api`, possivelmente evoluindo para contribuições mais técnicas.

---

## Sprint 2 - Testes de Cobertura do Módulo de Medidores
**Duração**: 12/05/2026 - 25/05/2026

### Resumo da Sprint

Nesta sprint, atuei diretamente na implementação da suíte de testes unitários do módulo de medidores do MEPA Web (`mepa-web`), em colaboração com o Ranni. O trabalho foi iniciado com um estudo aprofundado do repositório para entender os padrões de teste já existentes, a configuração do Vitest e as convenções adotadas pelos mantenedores.

A partir desse estudo, identifiquei os módulos que careciam de cobertura e estruturei o trabalho como um conjunto de issues independentes, cada uma correspondendo a um módulo específico, para que os demais integrantes do grupo também pudessem contribuir de forma paralela e organizada.

A implementação foi feita junto com o Ranni, cobrindo os fluxos principais dos componentes de relatório técnico, eventos e suas respectivas interfaces de usuário.

---

### Atividades Realizadas

| Data  | Descrição da Atividade                                                                                          | Categoria    | Referência                                                                 | Status       |
| ----- | --------------------------------------------------------------------------------------------------------------- | ------------ | -------------------------------------------------------------------------- | ------------ |
| 17/05 | Estudo da estrutura do repositório `mepa-web` e dos padrões de teste existentes                                 | Estudo       | MEPA Web                                                                   | Concluído ✅  |
| 20/05 | Análise dos módulos sem cobertura e levantamento dos cenários necessários                                       | Planejamento | MEPA Web                                                                   | Concluído ✅  |
| 21/05 | Divisão do trabalho em issues independentes por módulo, para distribuição entre o grupo                         | Organização  | [MR Sprint 2](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests/77) | Concluído ✅  |
| 23/05 | Implementação dos testes dos componentes de relatório técnico (`report-button`, `technical-report`)             | Testes       | [MR Sprint 2](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests/77) | Concluído ✅  |
| 24/05 | Implementação dos testes dos componentes de eventos (`event-list`, `event-table`, `event-summary`, `filter`)    | Testes       | [MR Sprint 2](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests/77) | Concluído ✅  |
| 24/05 | Implementação dos testes de métricas numéricas e visão geral (`numeric-measurements`, `overview-page`)          | Testes       | [MR Sprint 2](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests/77) | Concluído ✅  |
| 25/05 | Revisão da cobertura, ajuste de casos limite e preparação do Merge Request                                      | Integração   | [MR Sprint 2](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests/77) | Concluído ✅  |

---

### Principais Conquistas

- **Cobertura acima de 90% de branches** nos módulos-alvo do projeto, incluindo:
  - `src/app/medidores` — 93,75% de cobertura de branches
  - `src/app/medidores/[medidorId]/components` — 91,09% de cobertura de branches
  - `src/app/medidores/[medidorId]/eventos/components` — 92,63% de cobertura de branches
  - `src/app/medidores/[medidorId]/ficha-tecnica` — 100% de cobertura de branches
- **563 testes passando** ao final da sprint, distribuídos em 75 arquivos de teste.
- **Organização em issues**: a divisão do trabalho em tarefas independentes por módulo facilitou a contribuição paralela dos demais integrantes do grupo.
- Criação de uma infraestrutura sólida de mocks para módulos externos (`@react-pdf/renderer`, `html-to-image`, `swr`, `lucide-react`, componentes de UI internos), tornando os testes isolados e estáveis.

---

### Desafios Encontrados

O principal desafio foi entender a fundo como cada componente se comporta em diferentes estados (carregando, com erro, com dados, sem dados) para criar cenários de teste representativos sem torná-los frágeis.

Outro ponto complexo foi a cobertura de branches em operadores `??` e condicionais ternários cujas ramificações alternativas são logicamente inalcançáveis — nesses casos, foi necessário identificar quais branches realmente valiam o esforço de teste e quais eram proteções defensivas do código sem impacto prático.

A configuração de mocks para componentes assíncronos (como o gerador de PDF) exigiu o uso de `vi.useFakeTimers()` e `vi.runAllTimersAsync()` para simular corretamente o fluxo de geração e download de arquivos.

---

### Lições Aprendidas

- **Leitura de relatórios de cobertura**: aprendi a interpretar relatórios V8 de cobertura, distinguindo branches inalcançáveis de branches simplesmente não testados, o que torna o trabalho muito mais direcionado.
- **Mocking estratégico**: entendi como isolar dependências externas de forma eficiente, evitando que os testes dependam de comportamentos de bibliotecas de terceiros.
- **Testes de componentes assíncronos e com timers**: o uso de `waitFor`, `vi.useFakeTimers` e `vi.runAllTimersAsync` foi fundamental para testar fluxos que envolvem debounce, polling e geração de arquivos.
- **Colaboração orientada a tarefas**: a divisão prévia do trabalho em issues bem delimitadas facilitou muito a colaboração com o Ranni e reduziu conflitos de código durante a integração.

### Plano Pessoal para a Próxima Sprint

Na próxima sprint, pretendo continuar contribuindo no MEPA Web, com foco em funcionalidades práticas do sistema. Quero aprofundar o contato com fluxos mais complexos de frontend, especialmente os relacionados à visualização de dados e à experiência do usuário em telas de análise.

---

## Sprint 3 - Design System, Skeletons e Componentes Core
**Duração**: 26/05/2026 - 07/06/2026

### Resumo da Sprint

Nesta sprint, o grande objetivo foi consolidar a estabilidade da interface do usuário atacando dívidas técnicas críticas em módulos fundamentais: o Design System (`src/components/ui`), os Skeletons de carregamento, e os Componentes Raiz/Gráficos (Issues 76 e 78).

Para lidar com o volume e a complexidade do ecossistema do Design System (quase 1.000 linhas de código sem cobertura), adotei uma abordagem metódica. Primeiro, dediquei um tempo substancial para **estudar cada componente isoladamente**, entendendo seu papel na interface e suas dependências. Em seguida, **pensei e planejei a arquitetura dos mocks** necessários para não engessar o código (especialmente com bibliotecas como Radix UI e Recharts). Por fim, **implementei ativamente os testes**, iterando até garantir que todos os fluxos condicionais e estados visuais estivessem garantidos.

### Atividades Realizadas

| Data  | Descrição da Atividade                                                                                          | Categoria    | Referência                                                                 | Status       |
| ----- | --------------------------------------------------------------------------------------------------------------- | ------------ | -------------------------------------------------------------------------- | ------------ |
| 27/05 | Estudo profundo da arquitetura do Design System (módulos UI e Skeletons) e das dependências externas            | Estudo       | MEPA Web (Issue 78)                                                        | Concluído ✅  |
| 29/05 | Planejamento da estratégia de mocks para Radix UI (`pointer-capture`), Next.js (`navigation`) e Recharts        | Planejamento | MEPA Web                                                                   | Concluído ✅  |
| 02/06 | Implementação de testes em componentes de interface complexos (`Sidebar`, `Chart`, `ConditionalLayout`, `Form`) | Testes       | Issue 78                                                                   | Concluído ✅  |
| 04/06 | Execução e ajuste fino de testes unitários para a Issue 76 (Root Components, Charts, e Stories)                 | Testes       | Issue 76                                                                   | Concluído ✅  |
| 05/06 | Validação global de métricas e testes de regressão (45 novos arquivos, 411 testes)                              | Integração   | Execução Local / CLI                                                       | Concluído ✅  |

### Maiores Avanços

- **Expansão massiva da suíte de testes:** Criação de 45 novos arquivos de teste (43 para a UI e 2 para Skeletons), adicionando **411 novos casos de teste** ao repositório.
- **Salto de cobertura crítico:** O módulo de Design System e Skeletons saltou de uma cobertura pífia (~15%) para **99,07% em linhas e 90,40% em branches**, superando a meta estabelecida.
- **Teste de componentes estruturais complexos:** Consegui mockar e testar fluxos difíceis, como a resolução de chaves e formatação dentro do componente abstrato `Chart` e o gerenciamento de eventos responsivos da `Sidebar`.
- Apoio na validação dos componentes raiz (Issue 76), ajudando a tirar módulos inteiros da inércia (0% → +70%).

### Dificuldades

A maior dificuldade foi lidar com componentes da UI baseados em bibliotecas terceiras não-triviais. Testar os popovers, seletores de data e tooltips construídos em cima do **Radix UI** exigiu o desenvolvimento de um workaround específico de "pointer-capture" para evitar que os eventos de ponteiro falhassem durante a renderização no ambiente de teste (`happy-dom`).

Outro gargalo considerável foi estruturar os testes para o componente **Chart**, que encapsula lógicas de `recharts`. Foi necessário forjar payloads customizados e chaves de configuração (`nameKey`, `labelKey`) para garantir que as funções de transformação rodassem perfeitamente, além de lidar com o `ResponsiveContainer` que costuma se comportar mal fora de um ambiente de navegador real.

### Aprendizados

- **Análise Reversa de Dependências:** Aprendi que, para testar wrappers de UI complexos de forma efetiva, primeiro é necessário dissecar como a biblioteca de base (como Radix ou Recharts) interage com o DOM virtual.
- **Respeito à configuração global (Vitest):** Entendi a importância de não alterar os padrões globais (como tentar excluir agressivamente os `.stories.tsx` do arquivo de configuração oficial) para favorecer minhas próprias métricas de PR, preferindo aplicar esses filtros em comandos paralelos pelo CLI (`--coverage.exclude`) para provar o valor entregue sem sujar o `vitest.config.mts` do mantenedor.
- **O tripé do desenvolvimento TDD tardio:** A validação metodológica de *"Estudar -> Planejar o mock -> Implementar a asserção"* se provou extremamente mais rápida a longo prazo do que tentar codar testes reativos baseados apenas em tentativa e erro.

### Plano Pessoal para a Próxima Sprint

Com a robustez dos componentes base e do Design System muito bem estabelecida, o foco agora é auxiliar no refinamento final do repositório para o encerramento do semestre letivo, realizando eventuais polimentos de código que restarem ou apoiando na revisão de Merge Requests dos meus colegas.

---

## Histórico de Versão

| Data       | Versão | Descrição                          | Autor                                                       |
| ---------- | ------ | ---------------------------------- | ----------------------------------------------------------- |
| 21/04/2026 | 1.0    | Versão inicial - Sprint 0          | [Vitor Hoffmann](https://github.com/vitor-hoffmann)         |
| 11/05/2026 | 1.1    | Adiciona Sprint 1                  | [Vitor Hoffmann](https://github.com/vitor-hoffmann)         |
| 25/05/2026 | 1.2    | Adiciona Sprint 2                  | [Vitor Hoffmann](https://github.com/vitor-hoffmann)         |
| 07/06/2026 | 1.3    | Adiciona Sprint 3                  | [Vitor Hoffmann](https://github.com/vitor-hoffmann)         |

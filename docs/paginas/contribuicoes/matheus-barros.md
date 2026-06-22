# Diário de Bordo - Matheus Barros
 
Esta seção tem como objetivo registrar, ao longo das sprints, o acompanhamento individual das atividades realizadas no projeto.
 
A cada sprint, são documentadas as experiências, tarefas realizadas, dificuldades e aprendizados durante o processo de contribuição no MEPA, permitindo acompanhar a evolução individual dentro do projeto.
 
---
 
## Sprint 0 - Documentação  
**Duração**: 06/04/2026 - 22/04/2026  
 
### Resumo da Sprint
 
Nesta sprint, minha contribuição foi focada principalmente na **organização e documentação de como configurar o ambiente** para início das atividades no projeto MEPA.
 
Meu foco principal foi entender os processos de instalação e tecnologias envolvidas no projeto. 
 
---
 
### Atividades Realizadas
 
| Data | Atividade | Tipo | Referência | Status |
| ----- | --------- | ---- | ---------- | ------ |
| 20/04 | Estudo da estrutura geral do projeto MEPA | Estudo | [Repositório MEPA](https://gitlab.com/lappis-unb/projetos-energia/mepa) | Concluído |
| 20/04 | Análise das tecnologias para configurar o ambiente | Estudo | [Repositório MEPA](https://gitlab.com/lappis-unb/projetos-energia/mepa) | Concluído |
| 21/04 | Levantamento e catálogo de documentação relativo a instalação e configuração local do projeto | Estudo/Doc | [Sprint 0](../sprints/sprint0.md) | Concluído |
| 21/04 | Organização do Documento | Doc | [Sprint 0](../sprints/sprint0.md) | Concluído |
| 21/04 | Documentação das issues selecionadas | Doc | [Sprint 0](../sprints/sprint0.md) | Concluído |
 
---
 
### Maiores Avanços
 
- Identificação e **configuração dos ambientes de infraestrutura, web e API** do projeto MEPA.
- Realização de estudos que proporcionaram uma compreensão mais sólida do contexto do projeto, facilitando a leitura e interpretação das issues.
---
 
### Dificuldades
 
A principal dificuldade foi lidar com a **complexidade da estrutura do projeto e com o GitLab**, plataforma com a qual não tinha familiaridade prévia e que exigiu um tempo considerável de adaptação. Além disso, foi necessário **configurar múltiplos ambientes de desenvolvimento** com tecnologias nunca utilizadas antes, o que demandou esforço e pesquisa adicionais.
 
---
 
### Aprendizados
 
Aprendi a **configurar e subir os ambientes de infraestrutura, web e API**, além de desenvolver familiaridade com as tecnologias envolvidas no projeto. Também aprimorei minha capacidade de analisar e priorizar issues em repositórios reais, considerando critérios como complexidade, impacto e clareza de escopo.
 
---
 
### Plano Pessoal para a Próxima Sprint
 
Na próxima sprint, pretendo aprofundar meu entendimento sobre o funcionamento geral do projeto, explorando com mais detalhes a arquitetura e as interações entre os componentes. Com essa base mais sólida, o objetivo é estar preparado para iniciar a resolução das issues selecionadas de forma mais eficiente e segura.
 
---
 
## Sprint 1 - Primeira Contribuição
**Duração**: 27/04/2026 - 11/05/2026
 
### Resumo da Sprint
 
Nesta sprint, realizei minha primeira contribuição efetiva ao projeto MEPA, com foco em documentação. Identifiquei uma issue aberta que apontava referências incorretas ao projeto SIGE/SMI nos arquivos `README.md` e `CONTRIBUTING.md` do repositório `mepa-api`, dificultando o onboarding de novos colaboradores. Assumi a tarefa de corrigir essas referências e abrir um Merge Request com as alterações.
 
---
 
### Atividades Realizadas
 
| Data | Atividade | Tipo | Referência | Status |
|------|-----------|------|------------|--------|
| 10/05 | Análise de issues abertas e identificação de oportunidade de contribuição no `mepa-api` | Estudo | [Issue #docs](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-api/-/issues) | Concluído |
| 11/05 | Correção do `README.md` e `CONTRIBUTING.md`, abertura de MR via fork | Doc | [MR](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-api/-/merge_requests) | Concluído |
---
 
### Maiores Avanços
 
- **Primeira contribuição efetiva ao MEPA**: Abertura de um Merge Request com correções reais que impactam diretamente a experiência de novos colaboradores no repositório.
- **Domínio do fluxo de contribuição no GitLab**: Percorri o processo completo — fork, autenticação via token de acesso pessoal, criação de branch, commit e abertura de MR apontando para o repositório upstream.
- **Correções de alto impacto para o onboarding**: As alterações garantem que novos colaboradores consigam seguir o README do clone até `make start-dev` sem sair do repositório correto, eliminando links quebrados e referências a projetos externos.
---
 
### Dificuldades
 
- **Autenticação no GitLab via terminal**: O GitLab não aceitou senha diretamente, foi necessário criar um Personal Access Token e configurar a URL remota com ele.
- **Adaptação ao GitLab**: Pequenas diferenças de interface e fluxo em relação ao GitHub geraram dificuldade no início, mas foram superadas ao longo do processo.
---
 
### Aprendizados
 
- **Fluxo de contribuição via fork no GitLab**: Aprendi na prática como contribuir para projetos aos quais não se tem acesso de escrita direto, utilizando fork + MR para o repositório original.
- **Autenticação com Personal Access Token**: Entendi como o GitLab gerencia autenticação no terminal e como configurar o remote corretamente para realizar o push com segurança.
- **Boas práticas de nomenclatura de branches e commits**: Apliquei o padrão Conventional Commits (`docs: fix README and CONTRIBUTING references to SIGE/SMI projects`) e um nome de branch descritivo (`docs/fix-readme-contributing-references`).
---
 
### Plano Pessoal para a Próxima Sprint
 
- **Acompanhar o MR aberto**: Monitorar a revisão dos mantenedores e responder prontamente a eventuais pedidos de ajuste.
- **Buscar novas contribuições**: Explorar outros pontos de melhoria nos repositórios do MEPA, avançando para contribuições mais técnicas conforme o projeto evolui.
---
 
## Sprint 2 - Testes Unitários
**Duração**: 12/05/2026 - 25/05/2026
 
### Resumo da Sprint
 
Nesta sprint, minha contribuição foi focada em **testes unitários para componentes do módulo `pessoas`** do MEPA Web. Identifiquei 4 componentes sem cobertura de testes e implementei uma suíte completa para cada um, elevando a cobertura do diretório de 27% para aproximadamente 47%.
 
---
 
### Atividades Realizadas
 
| Data | Atividade | Tipo | Referência | Status |
|------|-----------|------|------------|--------|
| 12/05 | Análise dos componentes sem cobertura de testes no módulo `pessoas` | Estudo | [Repositório MEPA Web](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web) | Concluído |
| 18/05 | Implementação de testes para `ResendActivationButton` (8 testes) | Teste | [MR](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests) | Concluído |
| 19/05 | Implementação de testes para `SendPasswordResetButton` (9 testes) | Teste | [MR](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests) | Concluído |
| 21/05 | Implementação de testes para `BlockToggleButton` (12 testes) | Teste | [MR](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests) | Concluído |
| 23/05 | Implementação de testes para `PeopleFeedbackToast` (7 testes) | Teste | [MR](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests) | Concluído |
 
---
 
### Maiores Avanços
 
- **36 novos testes implementados** para os 4 componentes sem cobertura, elevando a cobertura do diretório `pessoas` de 27% para ~47%.
- **`ResendActivationButton`**: Cobertos renderização condicional por status, chamada da action e toast de sucesso/erro com mensagens padrão (8 testes).
- **`SendPasswordResetButton`**: Cobertos guarda das condições `active + email`, chamada da action e toast de sucesso/erro com mensagens padrão (9 testes).
- **`BlockToggleButton`**: Cobertos `isSelf`, status inválido, bloquear/desbloquear, confirm dialog, actions e toasts de sucesso/erro (12 testes).
- **`PeopleFeedbackToast`**: Cobertos `emitPeopleToast` (evento + sessionStorage), exibição de toast, fechamento e restauração ao montar (7 testes).
 
---
 
### Dificuldades
 
- **Compreensão do comportamento assíncrono dos componentes**: Alguns componentes dependiam de eventos customizados e sessionStorage, exigindo atenção especial ao ciclo de vida e à ordem de execução nos testes.
- **Configuração do ambiente de testes**: Ajustar mocks para actions, toasts e eventos do DOM exigiu estudo da documentação do Vitest e das convenções do projeto.
 
---
 
### Aprendizados
 
- **Testes unitários com Vitest e Testing Library**: Aprofundei meu conhecimento em como testar componentes Vue com renderização condicional, eventos customizados e interações com o sessionStorage.
- **Cobertura de código como métrica de qualidade**: Aprendi a interpretar relatórios de cobertura e a priorizar componentes com maior risco e menor cobertura.
- **Boas práticas de mock**: Aprendi a isolar dependências externas (actions, toasts, APIs do browser) para garantir testes determinísticos e de fácil manutenção.
 
---
 
### Plano Pessoal para a Próxima Sprint
 
- **Acompanhar o MR aberto**: Monitorar a revisão dos mantenedores e responder a eventuais pedidos de ajuste nos testes.
- **Ampliar a cobertura**: Identificar outros módulos do MEPA Web com cobertura abaixo do esperado e propor novas contribuições de testes ou funcionalidades.
 
---
 
## Sprint 3 - Utilitários de Admin/Components
**Duração**: 26/05/2026 - 08/06/2026

### Resumo da Sprint

Nesta sprint, minha contribuição foi focada em **testes unitários para funções utilitárias do módulo `admin/components`** do MEPA Web, complementando o escopo da Issue #77. Foram criados 3 arquivos de teste cobrindo formatação de datas, ordenação de selects e extração de erros de formulário, aumentando a cobertura do módulo em ~20%.

---

### Atividades Realizadas

| Data | Atividade | Tipo | Referência | Status |
|------|-----------|------|------------|--------|
| 26/05 | Análise dos utilitários sem cobertura em `admin/components` | Estudo | [Repositório MEPA Web](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web) | Concluído |
| 02/06 | Implementação de testes para `date-input-format` (35 testes) | Teste | [MR](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests) | Concluído |
| 05/06 | Implementação de testes para `select-option-sorting` (18 testes) | Teste | [MR](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests) | Concluído |
| 07/06 | Implementação de testes para `form-error-message` (12 testes) | Teste | [MR](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests) | Concluído |
| 08/06 | Abertura do MR na branch `37-admin-components-coverage` | MR | [MR](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests) | Concluído |

---

### Maiores Avanços

- **65 novos testes implementados** em 3 arquivos, cobrindo formatação de datas, ordenação de selects e extração de erros de formulário do módulo `admin/components`.
- **`date-input-format`**: testes de conversão entre ISO e `dd/MM/yyyy`, incluindo zero-padding, datas inválidas e anos bissextos (35 testes).
- **`select-option-sorting`**: testes de ordenação alfabética, por critério e geração de labels dinâmicas (18 testes).
- **`form-error-message`**: testes de extração e priorização de mensagens de erro provenientes de múltiplas fontes do formulário (12 testes).

---

### Dificuldades

Os testes de tratamento de data foram a parte mais desafiadora da sprint. Os casos de borda envolvendo datas inválidas, fuso horário e conversão entre formatos exigiram várias iterações para garantir cobertura correta sem falsos positivos.

---

### Aprendizados

- **Cobertura de utilitários puros**: testar funções sem dependências externas é mais direto, mas exige criatividade para mapear todos os casos de borda relevantes.
- **Casos de borda em datas**: aprendi a importância de cobrir explicitamente formatos inválidos, zero-padding e comportamentos de localização ao testar utilitários de data.

---

### Plano Pessoal para a Próxima Sprint

Pretendo acompanhar o MR aberto, responder a eventuais pedidos de ajuste dos mantenedores e identificar oportunidades de expandir ainda mais a cobertura do módulo `admin/components`.

---

## Sprint 4 - Testes de Utilitários de Utils
**Duração**: 09/06/2026 - 22/06/2026

### Resumo da Sprint

Nesta sprint, ampliei as contribuições de testes para o módulo `src/utils` do MEPA Web. Foram criados 5 arquivos de teste cobrindo utilitários puros de formatação monetária, disponibilidade fotovoltaica, datas e exibição de medidores, totalizando 107 novos testes. Junto com os 65 testes do ciclo anterior em `admin/components`, o MR reúne 172 testes no total, aguardando pipeline e aprovação.

---

### Atividades Realizadas

| Data | Atividade | Tipo | Referência | Status |
|------|-----------|------|------------|--------|
| 09/06 | Análise dos utilitários sem cobertura em `src/utils` | Estudo | [Repositório MEPA Web](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web) | Concluído |
| 12/06 | Implementação de testes para `currency` (8 testes) | Teste | [MR](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests) | Concluído |
| 14/06 | Implementação de testes para `pv-availability` (18 testes) | Teste | [MR](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests) | Concluído |
| 16/06 | Implementação de testes para `dateUtils` (26 testes) | Teste | [MR](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests) | Concluído |
| 19/06 | Implementação de testes para `meter-display` (17 testes) | Teste | [MR](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests) | Concluído |
| 20/06 | Implementação de testes para `meter-event-display` (28 testes) | Teste | [MR](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests) | Concluído |
| 22/06 | Abertura do MR consolidado com 172 testes no total | MR | [MR](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-web/-/merge_requests) | Concluído |

---

### Maiores Avanços

- **107 novos testes em `src/utils`**, cobrindo formatação monetária, disponibilidade fotovoltaica, datas, atributos e eventos de medidores.
- **MR consolidado com 172 testes**, reunindo o trabalho desta sprint e da anterior em uma contribuição única aguardando aprovação.

---

### Dificuldades

Os testes de data continuaram sendo o ponto mais desafiador, especialmente ao lidar com fuso horário, formatos ISO e conversões entre padrões. Garantir cobertura completa dos casos de borda sem introduzir falsos positivos exigiu várias iterações.

---

### Aprendizados

Testar utilitários puros reforçou a importância de pensar nos cenários extremos desde o início. Cada função exigiu cobrir valores nulos, entradas inválidas e diferentes formatos, o que aprofundou meu entendimento sobre qualidade e completude dos testes.

---

### Plano Pessoal para a Próxima Sprint

Pretendo acompanhar o MR aberto, responder a eventuais pedidos de ajuste dos mantenedores e, após a aprovação, identificar novos módulos com cobertura baixa para continuar expandindo a suíte de testes do projeto.

---

## Histórico de Versão

| Data       | Versão | Descrição                 | Autor |
| ---------- | ------ | ------------------------- | ----- |
| 21/04/2026 | 1.0    | Versão inicial - Sprint 0 | [Matheus Barros](https://github.com/Ninja-Haiyai) |
| 11/05/2026 | 1.1    | Adiciona Sprint 1 | [Matheus Barros](https://github.com/Ninja-Haiyai) |
| 25/05/2026 | 1.2    | Adiciona Sprint 2 | [Matheus Barros](https://github.com/Ninja-Haiyai) |
| 08/06/2026 | 1.3    | Adiciona Sprint 3 | [Matheus Barros](https://github.com/Ninja-Haiyai) |
| 22/06/2026 | 1.4    | Adiciona Sprint 4 | [Matheus Barros](https://github.com/Ninja-Haiyai) |

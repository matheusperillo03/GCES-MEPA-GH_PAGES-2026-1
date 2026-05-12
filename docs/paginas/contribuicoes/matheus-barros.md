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
| 20/04 | Estudo da estrutura geral do projeto MEPA | Estudo | [Repositório MEPA](https://gitlab.com/lappis-unb/projetos-energia/mepa) | Concluído✅ |
| 20/04 | Análise das tecnologias para configurar o ambiente | Estudo | [Repositório MEPA](https://gitlab.com/lappis-unb/projetos-energia/mepa) | Concluído✅ |
| 21/04 | Levantamento e catálogo de documentação relativo a instalação e configuração local do projeto | Estudo/Doc | [Sprint 0](../sprints/sprint0.md) | Concluído✅ |
| 21/04 | Organização do Documento | Doc | [Sprint 0](../sprints/sprint0.md) | Concluído✅ |
| 21/04 | Documentação das issues selecionadas | Doc | [Sprint 0](../sprints/sprint0.md) | Concluído✅ |
 
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
| 10/05 | Análise de issues abertas e identificação de oportunidade de contribuição no `mepa-api` | Estudo | [Issue #docs](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-api/-/issues) | Concluído ✅ |
| 11/05 | Correção do `README.md` e `CONTRIBUTING.md`, abertura de MR via fork | Doc | [MR](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-api/-/merge_requests) | Concluído ✅ |
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
 
## Histórico de Versão
 
| Data       | Versão | Descrição                 | Autor |
| ---------- | ------ | ------------------------- | ----- |
| 21/04/2026 | 1.0    | Versão inicial - Sprint 0 | [Matheus Barros](https://github.com/Ninja-Haiyai) |
| 11/05/2026 | 1.1    | Adiciona Sprint 1 | [Matheus Barros](https://github.com/Ninja-Haiyai) |
 
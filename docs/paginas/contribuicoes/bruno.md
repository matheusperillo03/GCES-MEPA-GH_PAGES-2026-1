# Diário de Bordo - Bruno Vasconcelos

Esta seção tem como objetivo registrar, ao longo das sprints, o acompanhamento individual das atividades realizadas por cada integrante do grupo.

A cada sprint, cada membro irá documentar sua experiência no projeto, descrevendo as tarefas realizadas, dificuldades encontradas, decisões tomadas e aprendizados adquiridos durante o processo de contribuição no MEPA. Além disso, o diário de bordo funciona como um histórico do desenvolvimento do projeto, tornando rastreável o processo de contribuição em um ambiente de software livre.

---
## Sprint 0 - Documentação
**Duração**: 06/04/2026 - 22/04/2026

### Resumo da Sprint

Nesta sprint, o foco principal foi preparar a base para as próximas contribuições no projeto MEPA. Além de conseguir subir o ambiente e compreender melhor a estrutura do repositório, também foi necessário iniciar a documentação do nosso próprio grupo, organizando o espaço onde serão registradas as sprints, atas e demais entregas da disciplina.

### Atividades Realizadas

| Data | Atividade | Tipo | Referência | Status |
| ----- | --------- | ---- | ---------- | ------ |
| 18/04 | Estudo da estrutura do repositório MEPA | Estudo | [Repositório MEPA](https://gitlab.com/lappis-unb/projetos-energia/mepa) | Concluído✅ |
| 18/04 | Análise dos 3 repositórios do grupo MEPA no GitLab | Estudo | [Repositório MEPA](https://gitlab.com/lappis-unb/projetos-energia/mepa) | Concluído✅ |
| 18/04 | Estudo da estrutura do repositório MEPA | Doc | [Repositório MEPA](https://gitlab.com/lappis-unb/projetos-energia/mepa) | Concluído✅ |
| 21/04 | Revisão de documentação  sprint 0| Doc | [Repositório GCES - MEPA](https://github.com/matheusperillo03/GCES-MEPA-GH_PAGES-2026-1) | Concluído✅ |



### Maiores Avanços

Consegui estruturar a base da documentação do grupo, deixando o MkDocs funcionando no repositório e com deploy automático configurado. Isso ajudou a organizar melhor o fluxo de trabalho da equipe e facilitou a construção das páginas que serão usadas ao longo da disciplina.

Além disso, o estudo inicial do repositório MEPA foi importante para entender como o projeto está dividido e como as partes do sistema se relacionam. Ao identificar que o projeto é separado em três repositórios principais, ficou mais claro onde cada tipo de contribuição pode acontecer e como o trabalho do grupo deve ser direcionado.

Também foi possível iniciar o levantamento de issues e entender melhor o perfil das tarefas disponíveis, o que será útil para definir contribuições mais adequadas nas próximas sprints.

### Dificuldades

O principal avanço nesta sprint foi compreender a estrutura real do projeto MEPA e como ele está organizado dentro do GitLab. Identificar que o sistema é dividido em três repositórios principais — API, Web e Infra — permitiu visualizar com mais clareza onde cada tipo de contribuição se encaixa e como as partes se comunicam entre si.

Além disso, a configuração do fluxo de deploy automático da documentação do grupo, utilizando GitHub Actions com MkDocs, foi um passo importante para estabelecer uma base técnica sólida. Essa automação garante que o site do grupo seja atualizado automaticamente a cada push, facilitando a organização das entregas da disciplina.

Outro avanço relevante foi o início do levantamento e análise das issues disponíveis no MEPA. Isso ajudou a mapear tarefas com perfil mais adequado para iniciantes, direcionando melhor os próximos passos do grupo e reduzindo a barreira de entrada para contribuições futuras.

### Aprendizados

Durante essa sprint, aprendi mais sobre a estrutura de um projeto de software livre em um contexto real, principalmente sobre a divisão entre frontend, backend e infraestrutura. Também tive contato mais prático com a configuração do MkDocs e com a automação de deploy da documentação, o que ajudou bastante na organização do repositório do grupo.


### Plano Pessoal para a Próxima Sprint

Na próxima sprint, pretendo começar a me aprofundar mais nas issues do MEPA para identificar possíveis contribuições mais simples e adequadas ao nosso nível de familiaridade com o projeto.

---

## Sprint 1 - Primeira Contribuição
**Duração**: 27/04/2026 - 11/05/2026

### Resumo da Sprint

Nesta sprint, realizei minha primeira contribuição efetiva ao projeto MEPA, focada em documentação. A tarefa consistiu em adicionar uma seção de "Problemas comuns" (Troubleshooting) no `README.md` do repositório **mepa-web**. Durante o processo, também identifiquei que meu fork estava privado e precisei ajustar a visibilidade - uma lição importante para contribuições futuras.

Devido ao alto volume de demandas e à agenda corrida dos mantenedores, não foi possível que eles preparassem issues específicas para nossa equipe. Diante disso, fomos orientados a buscar contribuições mais acessíveis, como melhorias na documentação dos repositórios MEPA (web, api e infra).

### Atividades Realizadas

| Data | Atividade | Status |
|------|-----------|--------|
| 08/05 | Exploração dos repositórios MEPA para identificar pontos de melhoria | ✅ |
| 10/05 | Fork do `mepa-web` (inicialmente privado, depois ajustado para público) | ✅ |
| 10/05 | Configuração de chave SSH no GitLab | ✅ |
| 10/05 | Criação da branch `docs/troubleshooting` e edição do README | ✅ |
| 11/05 | Abertura do Merge Request para a branch `develop` | ✅ |

### Maiores Avanços

- **Primeiro MR no GitLab**: Embora já tenha familiaridade com Git e GitHub, foi minha primeira contribuição usando GitLab. Aprendi as diferenças práticas: onde ficam os forks, como configurar upstream e o fluxo de abertura de MRs.
- **Fork privado → público**: Errei a visibilidade do fork e precisei corrigir. Aprendi que, para contribuições open source, o fork precisa ser público.
- **Seção de Troubleshooting**: Contribuí com um guia prático para problemas comuns (porta ocupada, API não responde, rebuild de containers, logs), preenchendo uma lacuna que dificultava o onboarding de novos contribuidores.

### Dificuldades

- **Fork privado por engano**: Percebi apenas depois de abrir o MR que meu fork estava privado, ajustei a visibilidade a tempo para dar visibilidade a outros contribuidores.
- **Autenticação no GitLab**: Diferente do GitHub, o GitLab não aceita senha no terminal, resolvi configurando chave SSH, que é mais simples e definitiva para resolver os problemas que estava tendo com autenticação com o GitLab.

### Aprendizados

- **Pipeline falhou, mas não impede**: Assim como outros MRs do grupo, o pipeline de CI/CD falhou. Como minha alteração foi apenas em documentação, entendi que isso não invalida a contribuição.
- **Fork precisa ser público**: Lição simples, mas fácil de esquecer na primeira vez.

### Plano Pessoal para a Próxima Sprint

- Acompanhar o MR aberto e responder a eventuais pedidos de ajuste.
- Explorar o repositório `mepa` em busca de oportunidades semelhantes.
- Se possível, evoluir para contribuições um pouco mais técnicas.

---

## Histórico de Versão
| Data     | Versão | Descrição             | Autor               |
| -------- | ------ | --------------------- | ------------------  |
| 20/04/2026 | 1.0    | Versão inicial - Sprint 0        | [Bruno Vasconcelos](https://github.com/brunocva)    |
| 11/05/2026 | 1.0 | Versão inicial - Sprint 1 | [Bruno Vasconcelos](https://github.com/brunocva) |

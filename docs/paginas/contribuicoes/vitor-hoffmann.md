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

## Histórico de Versão

| Data       | Versão | Descrição                          | Autor                                                       |
| ---------- | ------ | ---------------------------------- | ----------------------------------------------------------- |
| 21/04/2026 | 1.0    | Versão inicial - Sprint 0          | [Vitor Hoffmann](https://github.com/vitor-hoffmann)         |
| 11/05/2026 | 1.1    | Adiciona Sprint 1                           | [Vitor Hoffmann](https://github.com/vitor-hoffmann)         |

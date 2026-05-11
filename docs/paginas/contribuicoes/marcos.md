# Diário de Bordo - Marcos Bezerra

Esta seção tem como objetivo registrar, ao longo das sprints, o acompanhamento individual das atividades realizadas por cada integrante do grupo.

A cada sprint, cada membro irá documentar sua experiência no projeto, descrevendo as tarefas realizadas, dificuldades encontradas, decisões tomadas e aprendizados adquiridos durante o processo de contribuição no MEPA. Além disso, o diário de bordo funciona como um histórico do desenvolvimento do projeto, tornando rastreável o processo de contribuição em um ambiente de software livre.

---
## Sprint 0 - Documentação
**Duração**: 06/04/2026 - 22/04/2026

### Resumo da Sprint

Nesta sprint, o foco principal foi preparar a base para as próximas contribuições no projeto MEPA. Além de conseguir subir o ambiente e compreender melhor a estrutura do repositório, também foi necessário iniciar a documentação do nosso próprio grupo, organizando o espaço onde serão registradas as sprints, atas e demais entregas da disciplina.

### Atividades Realizadas

| Data | Atividade | Tipo | Referência | Status |
| ----- | --------- | ---------------------------------------- | --------------- | ------ |
| 16/04 | Configuração do MkDocs no repositório do grupo | Código/Doc | [GitHub](https://github.com/matheusperillo03/GCES-MEPA-GH_PAGES-2026-1) | Concluído✅ |
| 16/04  | Criação da branch `docs` e organização da documentação | Código/Doc | [Branch Docs](https://github.com/matheusperillo03/GCES-MEPA-GH_PAGES-2026-1/tree/docs) | Concluído✅ |
| 17/04  | Configuração de CD para build automático da documentação | Código | [Código](https://github.com/matheusperillo03/GCES-MEPA-GH_PAGES-2026-1/blob/docs/.github/workflows/CD-DeployMkdocs.yml) | Concluído✅ |
| 17/04  | Estudo da estrutura do repositório MEPA | Estudo | [Repositório MEPA](https://gitlab.com/lappis-unb/projetos-energia/mepa) | Concluído✅ |
| 17/04  | Análise dos 3 repositórios do grupo MEPA no GitLab | Estudo | [Repositório MEPA](https://gitlab.com/lappis-unb/projetos-energia/mepa) | Concluído✅ |
| 17/04  | Levantamento inicial de issues do projeto | Estudo | [Repositório MEPA](https://gitlab.com/lappis-unb/projetos-energia/mepa) | Concluído✅ |
| 18/04  | Criação da página da Sprint 0 na documentação | Doc | [Sprint 0](../sprints/sprint0.md) | Concluído✅ |
| 20/04  | Redação da ata da reunião 1 do grupo | Doc | [Ata 1](../atas//ata1.md) | Concluído✅ |

### Maiores Avanços

Consegui estruturar a base da documentação do grupo, deixando o MkDocs funcionando no repositório e com deploy automático configurado. Isso ajudou a organizar melhor o fluxo de trabalho da equipe e facilitou a construção das páginas que serão usadas ao longo da disciplina.

Além disso, o estudo inicial do repositório MEPA foi importante para entender como o projeto está dividido e como as partes do sistema se relacionam. Ao identificar que o projeto é separado em três repositórios principais, ficou mais claro onde cada tipo de contribuição pode acontecer e como o trabalho do grupo deve ser direcionado.

Também foi possível iniciar o levantamento de issues e entender melhor o perfil das tarefas disponíveis, o que será útil para definir contribuições mais adequadas nas próximas sprints.

### Dificuldades

Uma das dificuldades dessa sprint foi na comunicação e entendimento da disciplina. Demorou um tempo para eu entender de fato do que de fato seria abordado na disciplina e o que era esperado na Sprint 0. Após estudar um pouco repositórios de grupos passados essa dúvida foi sanada

Outra questão foi o onboarding com o MEPA, houve um pouco de dificuldade para marcar a reunião devido as demandas da universidade e os horários disponíveis dos mantenedores.

### Aprendizados

Durante essa sprint, aprendi mais sobre a estrutura de um projeto de software livre em um contexto real, principalmente sobre a divisão entre frontend, backend e infraestrutura. Também tive contato mais prático com a configuração do MkDocs e com a automação de deploy da documentação, o que ajudou bastante na organização do repositório do grupo.


### Plano Pessoal para a Próxima Sprint

Na próxima sprint, pretendo começar a me aprofundar mais nas issues do MEPA para identificar possíveis contribuições mais simples e adequadas ao nosso nível de familiaridade com o projeto.

---

## Sprint 1 - Primeira Contribuição
**Duração**: 27/04/2026 - 11/05/2026

### Resumo da Sprint

Nesta sprint, realizei minha primeira contribuição efetiva ao projeto MEPA, focada em documentação. A tarefa consistiu em corrigir erros de ortografia e acentuação no `README.md` do repositório `mepa-infra`. Além disso, durante o processo de submissão da contribuição, identifiquei um problema consistente no pipeline de CI/CD relacionado à autenticação do Terraform com o backend remoto. 

Devido ao alto volume de demandas e à agenda corrida dos mantenedores, não foi possível que eles preparassem issues específicas para nossa equipe(que seriam relacionadas a testes), conforme havia sido alinhado inicialmente. Diante disso, fomos orientados a buscar por issues simples, como por exemplo aquelas com ênfase na documentação do MEPA (web, api e infra). Foi nos dado um certo grau de liberdade para escolher como contribuir.

### Atividades Realizadas

| Data | Atividade | Tipo | Referência | Status |
|------|-----------|------|------------|--------|
| 28/04 | Análise de issues disponíveis nos repositórios MEPA | Estudo | [MEPA Infra](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-infra/-/tree/main) | Concluído ✅ |
| 08/05 | Correção de erros de português no README do repositório fork `mepa-infra` | Código/Doc | [Commit](https://gitlab.com/marcoslbz/mepa-infra/-/commit/81edad51fb7f77f252e572b9762add80101bc1b6) | Concluído ✅ |
| 08/05 | Criação de branch `docs/fix-readme` e abertura de Merge Request | Código/Doc | [MR !1](https://gitlab.com/lappis-unb/projetos-energia/mepa/mepa-infra/-/merge_requests/1) | Concluído ✅ |
| 08/05 | Identificação e análise do erro de pipeline (`Error loading state: HTTP remote state endpoint requires auth`) | Estudo | [Pipeline #2510707040](https://gitlab.com/marcoslbz/mepa-infra/-/pipelines/2510707040) | Concluído ✅ |

### Maiores Avanços

- **Primeira contribuição efetiva**: Consegui abrir um Merge Request com correções reais no README do projeto.
- **Identificação de problema estrutural**: Ao tentar validar o pipeline, percebi que o job `init_backend` falha com erro de autenticação no estado remoto do Terraform. Esse erro não tem relação com minha alteração – ele ocorre em qualquer commit, incluindo a branch `main` do repositório original. Essa descoberta pode se transformar em uma issue futura de infraestrutura, com bom potencial de contribuição para as próximas sprints.
![alt text](assets/pipeline.png)
![alt text](assets/pipeline2.png)
- **Aprendizado sobre fluxo de MR**: Como tenho mais familiaridade com o Github, nessa issue pude aprender melhor como funciona o fluxo no Gitlab com criação e exclusão de forks e abertura de Merge Requests.

### Dificuldades

- **Processo de exclusão e recriação do fork**: Por engano, deletei meu fork para tentar resolver o problema do pipeline, o que gerou atraso (o fork ficou agendado para exclusão). Aprendi que é melhor restaurar o fork ao invés de deletá-lo.

### Aprendizados

- **Boas práticas de nomenclatura de branches**: Pude aplicar o padrão `docs/fix-readme` para refletir o tipo de mudança, seguindo o padrão de boas práticas adotado amplamente por repositórios Open Source. A correta nomeação de branchs e commits pode facilitar o aceite de MRs em qualquer repositório.
- **Resiliência**: Contribuir em um projeto ativo com mantenedores ocupados exige paciência e autonomia para investigar problemas não documentados.

### Plano Pessoal para a Próxima Sprint

- **Acompanhar o MR aberto**: Verificar se os mantenedores irão revisar e aprovar a correção do README, respondendo a eventuais pedidos de alteração.
- **Propor uma issue para corrigir o erro do Pipeline**: Com base na análise feita, pretendo redigir uma issue detalhada no repositório `mepa-infra` sugerindo a correção do pipeline `init-backend`.
- **Buscar nova tarefa de documentação**: Caso haja tempo, procurar outros arquivos com problemas semelhantes (acentuação, clareza) nos repositórios `mepa-web` e `mepa-api`.

---

## Histórico de Versão
| Data     | Versão | Descrição             | Autor               |
| -------- | ------ | --------------------- | ------------------  |
| 20/04/2026 | 1.0.0    | Versão inicial - Sprint 0        | [Marcos Bezerra](https://github.com/marcoslbz)    |
| 10/05/2026 | 1.1.0    | Sprint 1     | [Marcos Bezerra](https://github.com/marcoslbz)    |
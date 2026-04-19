# Objetivo

A Sprint 0 teve como principal objetivo preparar o grupo para iniciar as contribuições no projeto MEPA, estabelecendo um ponto de partida para o entendimento tanto do sistema quanto do fluxo de trabalho utilizado pela equipe mantenedora.

Durante essa sprint, buscamos inicialmente subir o ambiente de desenvolvimento na máquina de todos os integrantes do grupo, seguindo a [documentação oficial do projeto](https://gitlab.com/lappis-unb/projetos-energia/mepa), assim todos estariam prontos para contribuir e também já seria possível identificar possíveis dificuldades, inconsistências na documentação e dependências necessárias para novos contribuidores.

Além disso, foi realizado um processo de onboarding com os mantenedores do repositório, com o intuito de entender como o projeto está organizado, quais tecnologias são utilizadas e como ele funciona.

Foi feito o mapeamento do fluxo de contribuição adotado pelo projeto. Foram analisados aspectos como a criação de branches, abertura de Merge Requests, padrões de commits utilizados e boas práticas esperadas pelos mantenedores.

Também foi realizada uma análise inicial das issues disponíveis no repositório, com o objetivo de identificar tarefas classificadas como mais simples ou adequadas para iniciantes e consequentemente para a disciplina. Esse mapeamento servirá como base para a definição das atividades individuais nas próximas sprints, permitindo que cada integrante contribua no projeto.

---

# Sobre o repositório

O projeto MEPA está organizado em um grupo no GitLab mantido pelo LabLivre, laboratório de software da Universidade de Brasília, que anteriormente era conhecido como LAPPIS. Esse grupo concentra os repositórios relacionados ao sistema, separando as responsabilidades entre **Web, API e infraestrutura**.

<p align="center">
  <img src="../assets/MEPArepo.png" alt="Repositório GitLab MEPA" width="800">
</p>

Essa organização em múltiplos repositórios ajuda a deixar o projeto mais modular e também permite que cada parte do sistema evolua de forma mais independente. Para a disciplina, isso é importante porque nos dá contato com uma estrutura real de software livre, onde não existe apenas uma aplicação isolada, mas sim um ecossistema de componentes que trabalham juntos.

---

## MEPA API

<p align ="center">
    <img src="../assets/MEPAAPI.png" alt="Painel Web do MEPA">
</p>

O grupo do MEPA é composto por três repositórios principais. O primeiro é o **MEPA API**, responsável pela camada de backend e pelo processamento das regras de negócio do sistema. Esse repositório utiliza Python, Django e Django REST Framework, e concentra as rotas, a autenticação, a integração com o banco de dados e a exposição dos dados consumidos pelo frontend.

---

## MEPA Web

<p align ="center">
    <img src="../assets/MEPAweb.png" alt="Painel Web do MEPA">
</p> 

O segundo é o **MEPA Web**, que representa o [frontend da aplicação](https://mepaenergia.org).

<p align ="center">
    <img src="../assets/MEPAfrontend.png" alt="Painel Web do MEPA">
</p> 

É nele que está a interface visual utilizada pelos usuários, desenvolvida com Next.js, React, TypeScript e Tailwind CSS. Esse repositório é o que mais se relaciona com a experiência de uso do sistema, já que é por meio dele que os dados energéticos são exibidos em painéis, gráficos e telas de navegação.

---

## MEPA Infra

<p align ="center">
    <img src="../assets/MEPAinfra.png" alt="Painel Web do MEPA">
</p> 

O terceiro é o **MEPA Infra**, que cuida da infraestrutura e do processo de deploy da aplicação. Esse repositório é responsável por automatizar a configuração do ambiente, o provisionamento da infraestrutura e a publicação dos serviços que compõem o sistema. Ele utiliza ferramentas como Terraform e Ansible, além de conter as configurações relacionadas ao Nginx, Docker e demais componentes de execução.

---

# Subir ambiente
Como subir ambiente e a experiencia do grupo ao subir ambiente (Quem conseguiu e etc)

---

# Como contribuir
É em formato de issue?

---

# Mapa de Issues
Mapear as issues disponíveis e ranquear as "faceis"

---

# Onboarding
Descrever como foi o Onboarding com o MEPA (por a gravação talvez)

---
## Histórico de Versão

| Data     | Versão | Descrição             | Autor               |
| -------- | ------ | --------------------- | ------------------  |
| 18/04/2026 | 0.1  | Estruturando a Sprint | Marcos Bezerra      |
| 19/04/2026 | 0.2  | Adicionando Objetivo e descrição dos repositórios MEPA | Marcos Bezerra      |



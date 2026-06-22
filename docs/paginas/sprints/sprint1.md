## Objetivo

A Sprint 1 teve como objetivo revisar a documentação disponível dos três repositórios, avaliar e propor mudanças a partir de Merge Requests.

## MEPA Infra

## MEPA Web

No MEPA WEB, foram propostas as seguintes informações no README:

- Nota alertando sobre o .env.example;
- Pré-requisitos para rodar o projeto sem a presença de Docker;
- Acréscimo de um passo no passo-a-passo de como contribuir no projeto;

Essas alterações visam deixar claros algumas etapas do projeto que podem causar dúvidas em um usuário comum que não tem muito contexto do projeto.

## MEPA API

No MEPA API, foram propostas as seguintes melhorias no README:

* Mapeamento visual da estrutura de diretórios para facilitar a navegação no código;
* Tabela de referência rápida com os principais endpoints (Autenticação, Medidores, Leituras e Tarifas);
* Guia de padronização com instruções para o uso de ferramentas de qualidade como **Ruff** e **pre-commit**;
* Seção dedicada a monitoramento e depuração, incluindo comandos para visualização de logs e uso do modo interativo (PDB);

Essas alterações visam elevar a experiência do desenvolvedor (DX), tornando o processo de configuração, uso da API e manutenção do backend muito mais ágil e intuitivo para quem está chegando ao projeto.

## MEPA Web

No MEPA WEB, foram propostas as seguintes informações no README:

- Adição da seção **"Problemas comuns" (Troubleshooting)** com soluções práticas para erros frequentes durante a configuração do ambiente de desenvolvimento:
  - Porta 3001 já está em uso (comando para identificar e matar o processo);
  - API não responde (verificação de container e variável `NEXT_PUBLIC_API_URL`);
  - Limpar cache e rebuildar containers (`make clean-dev`, `make build-dev`, `make start-dev`);
  - Ver logs em tempo real (`docker compose logs -f`);
  - Pular hooks do Git em situações de emergência (`HUSKY=0 git commit`).

Essas alterações visam reduzir a dependência de mantenedores para dúvidas repetitivas, oferecendo um guia rápido de autoatendimento para novos contribuidores que enfrentarem problemas na primeira configuração do projeto.
---
## Histórico de Versão

| Data     | Versão | Descrição             | Autor               |
| -------- | ------ | --------------------- | ------------------  |
| 08/05/2026 | 1.0  | Estruturando a Sprint e adicioando a colaboração | [Caio Sabino](https://github.com/caiomsabino) |
| 10/05/2026 | 1.1  | Adicionando as melhorias propostas no MEPA API | [Ranni heler](https://github.com/Akaeranni) |
| 11/05/2026 | 1.2 | Adicionando seção de Problemas Comuns no README do MEPA Web | [Bruno Vasconcelos](https://github.com/brunocva) |


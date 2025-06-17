[![Status do Pipeline CI](https://img.shields.io/github/actions/workflow/status/luisMSAmorim/appmonitor-pipeline/ci.yml?branch=main)](https://github.com/luisMSAmorim/appmonitor-pipeline/actions/workflows/ci.yml)

## Este é o assessment da disciplina Pipelines de CI/CD e DevOps

### O papel do Git na Entrega Contínua

O Git é uma ferramenta fundamental para a Entrega Contínua, permitindo:

- Controle de Versão: Rastreamento completo das mudanças no código
- Colaboração: Desenvolvimento paralelo e seguro entre equipes
- Automação: Integração com pipelines de CI/CD
- Rastreabilidade: Histórico completo de alterações e releases

#### Branches e Tags

Branches (Ramificações):
- Permitem desenvolvimento paralelo e isolado de features
- Facilitam a organização do trabalho em equipe
- Protegem a branch principal (main/master)
- Possibilitam estratégias como GitFlow

Tags:
- Marcam pontos específicos no histórico
- Facilitam o versionamento semântico
- Permitem rollback
- Auxiliam na documentação

### Variáveis e Segredos no GitHub Actions

#### Variables (vars)
- Armazenam dados não-sensíveis
- Visíveis nos logs do workflow
- Podem ser reutilizadas em múltiplos workflows
- Acessadas via contexto vars: ${{ vars.NOME_DA_VARIAVEL }}
- Exemplo: SUPPORT_EMAIL e APP_ENV

#### Secrets (secrets)
- Armazenam dados sensíveis
- Exemplo: API_KEY

#### Environment Variables (env)
- Definidas no nível do workflow, job ou step
- Disponíveis durante a execução
- Podem referenciar vars e secrets
- Exemplo: APP_ENV

### Pipelines com Logs e Resumos

Logs detalhados e resumos de execução são ferramentas essenciais para identificar e resolver problemas de CI/CD.

#### Logs de Debug
- O que são: Fornecem uma visão dos passos da execução do workflow. Ao ativar RUNNER_DEBUG: true, o executor exibe informações detalhadas sobre as configurações, chamadas de API e comandos que foram executados.
- Como ajudam: Permitem a identificação de onde estão as falha. Por exemplo, se um comando falhar, o log de debug vai mostrar os argumentos completos, variáveis de ambiente e a saída de erro, facilitando a correção.

#### Job Summaries
- O que são: São painéis personalizados gerados ao final de um workflow, que exibem informações de forma visual.
- Como ajudam: Oferecem uma visão do resultado do pipeline.

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

# Resumo — Aula 06: Revisão de Ferramentas e Pipelines

**Aluno:** Andreus Vinícius Araújo de Andrade

---

### Ciclo Infinito do DevOps (Revisão Geral)
Integração entre Desenvolvimento (**DEV**) e Operações (**OPS**) em 8 etapas contínuas para entregar software rápido e com qualidade:
1. **Plan:** Planejamento ágil de tarefas e prioridades (Jira, Trello, Azure Boards).
2. **Code:** Escrita, revisão, testes e versionamento colaborativo do código.
3. **Build:** Compilação e geração de artefatos executáveis (`.jar`, pacote NPM, imagem Docker) + análise estática (SonarQube).
4. **Test:** Execução automática de testes no pipeline para barrar erros antes da produção.
5. **Release:** Validação via *Quality Gates* e geração de versão semântica (`Major.Minor.Patch`).
6. **Deploy:** Publicação automática em produção com reversão (*rollback*) em caso de falha.
7. **Operate:** Gestão de infraestrutura como código para manter estabilidade e escalabilidade (Kubernetes, Ansible).
8. **Monitor:** Observabilidade contínua via **Métricas** (CPU, memória, latência), **Logs** (registros de eventos) e **Traces** (rastreamento de requisições).

---

### Estrutura e Etapas de uma Pipeline
Uma **pipeline** automatiza as validações do *commit* até o *deploy* (Desenvolvimento → Homologação → Produção), seguindo três regras: **gerar o build uma única vez**, **padronizar o deploy nos ambientes** e **interromper tudo se houver erro**.

* **Build:** Compila o projeto, verifica a integridade inicial e gera o artefato.
* **Testes:** Roda validações automáticas para garantir que nada quebrou.
* **Qualidade:** Checa padrões de código antes de seguir adiante.
* **Segurança:** Busca vulnerabilidades, dependências inseguras e dados sensíveis expostos.
* **Artefatos (Package):** Empacota, versiona e armazena os arquivos gerados.
* **Deploy:** Prepara o ambiente e publica o artefato automaticamente.
* **Release e Monitoramento:** Controla as versões oficiais publicadas e acompanha o sistema em produção.

---

### GitHub Actions e Marketplace
* **GitHub Actions:** Plataforma nativa do GitHub para criar *workflows* automatizados disparados por gatilhos (*triggers*) como `push`, `pull request`, `tags` ou `releases`.
  ```yaml
  on: [push]
  jobs:
    build:
      runs-on: ubuntu-latest
  ```
* **GitHub Marketplace:** Catálogo com *Actions* prontas (oficiais e da comunidade) para integrar build, testes, segurança e deploy direto na pipeline.

---

### Atividade da Semana
* Integrar uma pipeline usando **GitHub Actions** ao projeto, configurada para rodar automaticamente a cada novo `push` na branch `main`.
* Buscar e analisar pelo menos **3 repositórios no GitHub** que utilizem pipelines, destacando suas características, funcionalidades, gatilhos e histórico.
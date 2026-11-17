# Resumo — Aula 04: Ferramentas de Integração e Entrega Contínua

**Aluno:** Andreus Vinícius Araújo de Andrade

---

### Revisão: Ciclo Infinito do DevOps
O DevOps une Desenvolvimento (**DEV**) e Operações (**OPS**) em um fluxo contínuo de 8 etapas para entregar software com mais velocidade, qualidade e menos falhas:
1. **Plan:** Planejamento ágil de tarefas e prioridades (Jira, Trello, Azure Boards).
2. **Code:** Escrita, revisão e versionamento colaborativo do código.
3. **Build:** Transformação do código em artefato executável (JAR, pacote NPM, imagem Docker) e análise estática (SonarQube).
4. **Test:** Execução automática de testes no pipeline para barrar erros antes da produção.
5. **Release:** Validação via *Quality Gates* e geração de versão semântica (`Major.Minor.Patch`).
6. **Deploy:** Implantação automática em produção, rápida e com reversão (*rollback*) em caso de falha.
7. **Operate:** Gestão de infraestrutura como código para manter estabilidade e escalabilidade (Kubernetes, Ansible).
8. **Monitor:** Observabilidade contínua via **Métricas** (CPU, memória, latência), **Logs** (registros de eventos) e **Traces** (rastreamento de requisições) para retroalimentar o planejamento.

---

### Ferramentas de CI/CD e Pipelines
* **Pipeline:** Sequência automatizada de etapas que leva o software do *commit* até o *deploy* de forma confiável, garantindo qualidade contínua ao longo da entrega.
* **Para que servem as ferramentas de CI/CD:**
  * Integrar alterações de código automaticamente e compilar versões;
  * Rodar testes automatizados e checar qualidade/segurança do código;
  * Gerar e armazenar artefatos, controlar releases e fazer deploy em diferentes ambientes;
  * Monitorar resultados, identificar falhas e integrar serviços do projeto.

---

### GitHub Actions
* Plataforma de automação integrada diretamente ao **GitHub**.
* Permite criar fluxos de trabalho (**workflows**) que rodam automaticamente a partir de eventos do repositório, como `push`, `pull request`, criação de `tags` ou `releases`.

---

### Atividade da Semana
* Analisar e comparar ferramentas de **CI/CD** (características, funcionalidades, vantagens, limitações e cenários de uso) com base no artigo *"Practical Comparison Between the CI/CD Platforms Azure DevOps and GitHub"* (Manolov, Gotseva e Hinov, 2025).
* Identificar todas as ferramentas citadas pelos autores e montar uma análise comparativa entre elas.
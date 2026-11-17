# Resumo — Aula 05: Pipeline de Integração Contínua

**Aluno:** Andreus Vinícius Araújo de Andrade

---

### Estrutura e Regras de uma Pipeline
Uma **pipeline** é uma sequência de validações automatizadas que leva o código do *commit* até o *deploy* (passando por Desenvolvimento → Homologação → Produção). Três regras guiam seu funcionamento:
* **Build uma única vez:** O mesmo artefato gerado é promovido entre os ambientes.
* **Mesmo deploy em todos os ambientes:** Padroniza a implantação para evitar diferenças entre testes e produção.
* **Falhou? Para tudo:** Se qualquer etapa der erro, o fluxo é interrompido na hora.

---

### Etapas de uma Pipeline na Prática
1. **Build:** Compila o projeto, verifica a integridade inicial e gera o artefato (`.jar`, `.war`, `.apk`, imagem Docker, etc.).
2. **Testes:** Roda validações automáticas logo após o build para garantir que o código novo não quebrou o que já funcionava.
3. **Qualidade:** Checa se o código segue os padrões definidos antes de avançar.
4. **Segurança:** Procura vulnerabilidades no código, dependências desatualizadas/inseguras e senhas ou dados sensíveis expostos.
5. **Artefatos (Package):** Empacota, versiona e guarda os arquivos de distribuição em repositórios de artefatos.
6. **Deploy:** Prepara o ambiente de destino, configura variáveis e publica o artefato automaticamente.
7. **Release e Monitoramento:** Cria e controla as versões oficiais liberadas aos usuários e acompanha o sistema rodando em produção.

---

### GitHub Actions e Marketplace
* **GitHub Actions:** Ferramenta nativa do GitHub que automatiza workflows a partir de gatilhos (*triggers*) no repositório, como `push`, `pull request`, criação de `tags` ou `releases`.
  ```yaml
  on: [push]
  jobs:
    build:
      runs-on: ubuntu-latest
  ```
* **GitHub Marketplace:** Catálogo com soluções prontas (criadas pelo GitHub, parceiros ou comunidade) para encaixar direto nas etapas de build, testes, segurança, cache e deploy.

---

### Atividade da Semana
* Escolher **3 Actions** no GitHub Marketplace e montar um projeto com uma pipeline automatizada no **GitHub Actions**, aplicando cada Action em uma etapa adequada.
* Executar e validar o funcionamento da pipeline e documentar no projeto quais Actions foram usadas, suas funções e como ajudaram na automação.
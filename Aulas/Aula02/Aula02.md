# Resumo — Aula 02: Conceitos de Integração e Entrega Contínua de Software

**Aluno:** Andreus Vinícius Araújo de Andrade

---

### DevOps e o Ciclo Infinito
Antigamente, quem desenvolvia (**DEV**) e quem cuidava dos servidores (**OPS**) trabalhavam separados, o que atrasava entregas e gerava o clássico *"na minha máquina funciona"*. O **DevOps** une as duas áreas em um ciclo contínuo de 8 etapas:

1. **Plan:** Planejar tarefas e prioridades (Jira, Trello, Azure Boards).
2. **Code:** Escrever, revisar e versionar o código com boas práticas.
3. **Build:** Transformar o código em algo executável (ex.: pacote NPM, imagem Docker) e checar qualidade (SonarQube).
4. **Test:** Rodar testes automatizados para barrar erros antes da produção.
5. **Release:** Validar qualidade, aprovar e gerar uma versão oficial.
6. **Deploy:** Publicar o sistema em produção de forma automática e rápida.
7. **Operate:** Manter o sistema estável e escalável no servidor (ex.: Kubernetes, Ansible).
8. **Monitor:** Acompanhar o sistema rodando usando **Métricas** (CPU, memória, latência), **Logs** (registros de eventos/erros) e **Traces** (caminho das requisições) para melhorar o próximo ciclo.

---

### CI vs. Delivery vs. Deployment
* **Integração Contínua (CI):** A cada *commit* no repositório, o sistema roda *build* e testes automáticos para pegar erros logo no início.
* **Entrega Contínua (Continuous Delivery):** Automação prepara tudo e deixa a versão pronta para ir ao ar, faltando só um clique/aprovação final.
* **Deploy Contínuo (Continuous Deployment):** Passou nos testes do pipeline, vai direto para produção automaticamente.

---

### Versionamento Semântico (SemVer)
Padrão **`MAJOR.MINOR.PATCH`** (ex.: `2.1.3`) para identificar o tamanho da mudança:
* **MAJOR (`X.0.0`):** Mudança grande que quebra compatibilidade com versões antigas.
* **MINOR (`0.X.0`):** Nova funcionalidade, mas sem quebrar o que já existia.
* **PATCH (`0.0.X`):** Correção de bug (*bug fix*).

---

### Git, Tags e Deploy na Prática
* **Git e GitHub:** Git controla as versões localmente no PC; GitHub guarda o repositório online.
* **Tags no Git:** Servem para marcar versões importantes no histórico (ex.: `git tag 1.0.0` e `git push origin 1.0.0`).
* **Vercel:** Plataforma usada para hospedar e fazer deploy automático de projetos web toda vez que enviamos código novo (`git push`) para o GitHub.

---

### Atividade da Semana
* Configurar VS Code + Git, criar os arquivos (`index.html`, `style.css`, `script.js`) e subir no GitHub.
* Alterar o projeto, fazer novos *commits*, criar uma **tag** de versão e enviar a documentação da atividade no Teams.
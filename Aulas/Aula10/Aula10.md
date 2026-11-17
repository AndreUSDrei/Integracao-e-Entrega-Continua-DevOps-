# Resumo — Aula 10: Projeto DevOps

**Aluno:** Andreus Vinícius Araújo de Andrade

---

### Objetivo do Projeto Final
* Desenvolver uma **aplicação web funcional em grupo** (com tema livre que resolva um problema real), colocando na prática tudo o que foi visto na disciplina: versionamento colaborativo, testes automatizados, CI/CD, containers e monitoramento.

---

### Requisitos Técnicos Obrigatórios
* **Arquitetura da Aplicação:** Front-end (interface), Back-end (regras de negócio/endpoints), Banco de Dados e Middleware (autenticação/validação, se aplicável).
* **Git e GitHub:** Uso de *branches* para features/correções, *commits* organizados, *Pull Requests* com revisão de código entre os integrantes e documentação clara.
* **Testes Automatizados:** Cobertura com testes **unitários**, de **integração**, **E2E** (fluxos do usuário) e de **performance** (latência/carga).
* **Integração Contínua (CI):** Pipeline (ex.: GitHub Actions) que instala dependências, valida estrutura/qualidade, roda os testes e gera o *build*.
* **Docker:** `Dockerfile` (para back-end e front-end, quando aplicável), configuração de portas/variáveis e instruções para subir os contêineres.
* **Entrega Contínua e Deploy (CD):** Geração e publicação automatizada da aplicação com identificação da versão e checagem pós-deploy.
* **Observabilidade e Segurança:** Registro de logs (eventos/erros), monitoramento de disponibilidade/métricas e proteção de segredos usando variáveis de ambiente + arquivo `.env.example` (sem senhas/tokens reais no repositório).

---

### Entregáveis e Apresentação Técnica
* **O que entregar:**
  * Repositório completo no GitHub (código, histórico, PRs e `README.md` detalhado);
  * Pipeline CI/CD funcionando com evidências dos testes automatizados;
  * Arquivos Docker configurados;
  * Aplicação implantada (link público ou ambiente reproduzível).
* **Apresentação Técnica:** Demonstrar na prática o objetivo/arquitetura do sistema, fluxo de Pull Requests, execução dos testes, subida dos contêineres Docker e o processo de deploy.
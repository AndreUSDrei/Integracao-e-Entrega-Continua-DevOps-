# Resumo — Aula 01: Apresentação da Disciplina e Introdução ao DevOps

**Aluno:** Andreus Vinícius Araújo de Andrade

---

### Como funciona a disciplina
* **Foco:** Unir desenvolvimento web com práticas de versionamento, automação e entrega contínua (DevOps).
* **Portfólio:** O professor reforçou a importância de manter os projetos organizados no GitHub para mostrar na prática o que sabemos fazer (ajuda muito para estágio e emprego).
* **Avaliação:** $\text{Média} = (P1 \times 0,25) + (P2 \times 0,25) + ((PJ + AT) \times 0,25)$
  * **P1 e P2:** Provas | **PJ:** Projeto | **AT:** Atividades semanais em grupo.

---

### Principais Conceitos
* **Controle de Versão:** Guarda o histórico de alterações do código, permite voltar atrás se der erro e trabalhar em equipe usando *branches* (ex.: GitHub, GitLab, Bitbucket).
* **Pipelines (CI/CD):** Sequência automatizada que compila, testa e publica o código sozinho, evitando erro manual.
  * **CI (Integração Contínua):** Juntar o código no repositório com frequência, rodando testes automáticos a cada alteração.
  * **CD (Entrega Contínua):** Deixar o sistema sempre testado e pronto para ser publicado com segurança.
* **Qualidade e Testes Automatizados:** Quanto antes achar o bug, mais barato e fácil é resolver. Os testes (unitários, integração, funcionais e *end-to-end*) rodam sozinhos no pipeline.
* **Containers (Docker) e Deploy:** Containers empacotam o sistema e suas dependências para rodar igual em qualquer máquina/servidor. Estratégias como *Rolling Update*, *Blue-Green* e *Canary* ajudam a atualizar o sistema sem tirar do ar e facilitam voltar versão (*rollback*).

---

### Atividade da Semana
* Formar grupo de 3 a 5 pessoas (fixo para o semestre).
* Criar o repositório da disciplina no GitHub e subir este resumo em `.md`.
* Responder à avaliação diagnóstica da Aula 01.
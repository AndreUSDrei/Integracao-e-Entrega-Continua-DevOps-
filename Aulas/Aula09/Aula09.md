# Resumo — Aula 09: Documentação de Software

**Aluno:** Andreus Vinícius Araújo de Andrade

---

### Por que Documentar Projetos
* **O objetivo:** Permitir que qualquer pessoa entre no GitHub e consiga entender, instalar, testar e rodar o projeto sem depender de explicações informais da equipe.
* **Problemas sem documentação:** Dependência de devs específicos, perda de conhecimento quando alguém sai, configurações feitas de jeito diferente, dificuldade para novos integrantes e perda de tempo com dúvidas repetitivas.
* **Pilares da documentação:** **Comunicação** (compartilhar conhecimento), **Manutenção** (facilitar correções), **Colaboração** (trabalho em equipe) e **Continuidade** (não depender de uma única pessoa).

---

### Tipos de Documentação e Áreas Envolvidas
A documentação conecta várias áreas do projeto (Engenharia de Software, Gestão, DevOps, Segurança, QA e Produto/UX) e se divide em três frentes principais:
1. **Documentação Técnica:** Arquitetura, APIs, banco de dados, componentes e configurações.
2. **Documentação de Projeto:** Objetivos, requisitos, escopo e decisões tomadas.
3. **Documentação de Processo (DevOps):** Padrões de *branches*, *commits*, *Pull Requests*, testes, pipelines CI/CD e deploy.

---

### Estrutura de um Bom `README.md`
É a porta de entrada do repositório no GitHub e deve trazer de forma clara e reproduzível:
* **Propósito e Tecnologias:** O que o sistema faz, stack utilizada e pré-requisitos (linguagem, banco, Node, Docker, versões recomendadas).
* **Instalação e Execução:** Passo a passo direto (clonar repositório → entrar na pasta → instalar dependências → configurar ambiente → rodar projeto).
* **Configuração e Variáveis:** Explicar quais variáveis de ambiente são necessárias e dar exemplos fictícios (`PORT=3000`, `DATABASE_URL=sua_url_aqui`).
* **Execução de Testes:** Comandos para rodar testes unitários, de integração e performance.
* **Estrutura de Pastas:** Visão geral dos diretórios principais (`src/`, `tests/`, `docs/`, `.github/workflows/`) sem precisar listar arquivo por arquivo.

---

### O que NÃO Colocar na Documentação (Segurança)
* Senhas reais de usuários, administradores ou bancos de dados;
* Chaves de API, tokens ou credenciais privadas;
* Arquivos `.env` reais ou segredos de configuração;
* Dados pessoais/confidenciais de clientes ou detalhes restritos de infraestrutura.

---

### Atividade da Semana
* Escolher um projeto de software e elaborar sua documentação completa (objetivo, problema, escopo, requisitos funcionais/não funcionais, tecnologias, arquitetura e componentes).
* Criar ou atualizar o **`README.md`** no GitHub com pré-requisitos, instalação, configuração, variáveis de ambiente, execução, testes e deploy (além de APIs e banco de dados, quando houver).
# Resumo — Aula 03: Gerência de Configuração

**Aluno:** Andreus Vinícius Araújo de Andrade

---

### O que é Gerência de Configuração
* **O problema:** Quando cada desenvolvedor ou servidor usa versões diferentes de código, bibliotecas, variáveis ou banco de dados, surge o clássico erro do *"na minha máquina funciona"* (ex.: rodar com Node 20 no PC e falhar com Node 18 em produção).
* **Configuração:** É tudo o que define como o sistema funciona e precisa ser controlado para manter todos os ambientes iguais:
  * **Código:** Arquivos fonte (`.js`, `.java`, `.py`) e versões da aplicação.
  * **Dependências:** Bibliotecas e versões (`package.json`, `pom.xml`).
  * **Parâmetros/Ambiente:** Arquivos `.env`, `JSON`, `YAML`, portas e URLs.
  * **Banco e Infraestrutura:** Scripts SQL, Docker, Terraform, README e scripts de build/deploy.

---

### Node.js e NPM
* **Node.js:** Ambiente que permite rodar JavaScript fora do navegador (no servidor/backend), unificando a linguagem entre front e back. (Teste no terminal: `node --version`).
* **NPM (Node Package Manager):** Gerenciador de pacotes que já vem com o Node. Usa o arquivo **`package.json`** para listar as dependências do projeto — assim, qualquer pessoa da equipe só precisa rodar `npm install` para baixar tudo na versão certa.

---

### Criando e Entendendo um Projeto React
* **Comandos principais:**
  ```bash
  npx create-react-app meu-projeto-react   # Cria o projeto com Webpack, Babel e servidor local
  cd meu-projeto-react                     # Entra na pasta
  npm start                                # Sobe o projeto localmente no navegador
  ```
* **Estrutura básica de pastas e arquivos:**
  * `node_modules/`: Bibliotecas instaladas pelo NPM.
  * `public/`: Arquivos estáticos (HTML base, imagens, JSON).
  * `src/`: Código React do projeto (`index.js` renderiza o app, `App.js` é o componente principal, `App.css` e `index.css` cuidam dos estilos).
  * `.gitignore`: Define o que o Git deve ignorar (como `node_modules` e senhas em `.env`).
  * `package.json` / `package-lock.json`: Registram scripts e versões exatas dos pacotes.

---

### Templates e Atividade da Semana
* **Templates prontos:** Em vez de começar sempre do zero, podemos buscar projetos base no **GitHub** (`git clone`), **Vercel Templates** ou **CodeSandbox**.
* **Atividade:**
  * Buscar um template de projeto em React, importar, fazer alterações personalizadas e subir em um repositório no **GitHub**.
  * Documentar todo o passo a passo (com descrições, prints e os links do GitHub e da **Vercel**) em um arquivo único.
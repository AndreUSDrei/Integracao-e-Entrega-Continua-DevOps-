# Resumo — Aula 07: Testes Automatizados

**Aluno:** Andreus Vinícius Araújo de Andrade

---

### O que são e Por que Automatizar Testes
* **Testes Automatizados:** São verificações feitas automaticamente por ferramentas para garantir que o sistema se comporta como esperado, sem depender de testes manuais a cada alteração no código.
* **Vantagens principais:**
  * Reduz erros humanos e aumenta a velocidade de validação;
  * Identifica falhas logo após um *commit* ou *push*;
  * Garante consistência e confiabilidade (evita que alterações novas quebrem funcionalidades antigas).
* **Na Pipeline de CI:** Rodam logo após o *build*. Se qualquer teste ou validação falhar, a pipeline para na hora, impedindo que código com erro avance para homologação ou produção.

---

### Tipos de Testes na Prática (Exemplo: Sistema de Descontos)
Para ilustrar, a aula usou um sistema web de cálculo de descontos (10% para compras abaixo de R$ 100 e 5% para compras iguais ou acima de R$ 100):

1. **Testes Unitários:** Validam funções, métodos ou componentes isolados do código.
   * *Exemplo de falha:* Mudar a regra de desconto para 15% quando o teste unitário espera 10% ou 5%.
2. **Testes de Integração:** Verificam o funcionamento conjunto entre módulos, interface, APIs e banco de dados.
   * *Exemplo de falha:* Trocar o texto de um botão para `"Calcular"` quando o teste procura o botão `"Calcular Desconto"`.
3. **Testes de Performance:** Avaliam tempo de resposta, comportamento sob carga e consumo de recursos para evitar lentidão ou gargalos.
   * *Exemplo de falha:* Exigir que a resposta ocorra em no máximo `1ms` e a aplicação estourar esse tempo.

---

### Qualidade de Código e ESLint
* **Qualidade no DevOps:** Não fica restrita só aos testes; faz parte de todo o ciclo de desenvolvimento e entrega.
* **ESLint:** Ferramenta de análise estática para JavaScript que roda na pipeline para barrar códigos fora do padrão ou com inconsistências (ex.: declarar uma variável `const x = 1;` e não usar — erro `no-unused-vars`).

---

### Atividade da Semana
* Criar um projeto contendo os **3 tipos de testes automatizados** (unitário, integração e performance), organizados para rodarem de forma independente.
* Configurar um arquivo `.yml` no **GitHub Actions** para rodar automaticamente a cada `push` na branch `main`, instalando as dependências, executando os três testes e exibindo os resultados.
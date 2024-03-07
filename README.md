# Testes unitários com C#
## Teste 1
- caso de teste: "verifica que um valor válido (ou seja, um que seja menor que o saldo da conta e maior que zero) retira a quantidade correta da conta."

![img 1](/assets/img1.png)

### primeira tentativa
- resultado: não passou

![img 2](/assets/img2.png)

- problema: O saldo deveria diminuir, mas em vez disso, ele aumentou pelo valor do saque.

- motivo: problema no método Debit, que adiciona o valor, ao invés de subtrair

![img 3](/assets/img3.png)

### segunda tentativa
- mudanças: erro no método Debit foi resolvido:

![img 4](/assets/img4.png)

- resultado: teste passou

![img 5](/assets/img5.png)

## Teste 2
- caso de teste: "verifica se o método Debit gera uma ArgumentOutOfRangeException se o valor do débito é menor que zero."

![img 6](/assets/img6.png)

- resultado: teste passou 

![img 7](/assets/img7.png)

## Teste 3
- caso de teste: "verifica se o método Debit gera uma ArgumentOutOfRangeException se o valor do débito é maior que o saldo."

![img 8](/assets/img8.png)

- resultado: teste passou

![img 9](/assets/img9.png)

## Teste 2 - refatorado
- caso de teste: "verifica se o método Debit gera uma ArgumentOutOfRangeException (com a mensagem especifica DebitAmountLessThanZeroMessage) se o valor do débito é menor que zero."
- alterações: alteramos a validação da Exception lançada, para que o caso fique mais específico e assertivo. Ou seja, o teste só vai passar se a Exception com a mensagem especificada for lançada, e não quando qualquer outra Exception for lançada.
  
![img 10](/assets/img10.png)

resultado: teste passou

![img 11](/assets/img11.png)

## Teste 3 - refatorado
- caso de teste: "verifica se o método Debit gera uma ArgumentOutOfRangeException(com a mensagem especifica DebitAmountExceedsBalanceMessage) se o valor do débito é maior que o saldo."
- alterações: alteramos a validação da Exception lançada, para que o caso fique mais específico e assertivo. Ou seja, o teste só vai passar se a Exception com a mensagem especificada for lançada, e não quando qualquer outra Exception for lançada.
  
![img 12](/assets/img12.png)

resultado: teste passou

![img 13](/assets/img13.png)

# Tecnologias e conceitos aprendidos

A partir do entendimento do artigo https://learn.microsoft.com/pt-br/visualstudio/test/walkthrough-creating-and-running-unit-tests-for-managed-code?view=vs-2022 , da Microsoft, os testes descritos acima foram realizados utilizando as seguintes tecnologias e ferramentas:

- Rider (IDE)
- .NET 8.0
- MSTest Framework

O projeto em que os testes foram baseados é um Console App, e os testes foram realizados utilizando do MSTest Framework - uma estrutura de teste fornecida pela Microsoft para realizar testes unitários em aplicativos .NET. O MSTest da suporte para várias funcionalidades que facilitam a criação e execução de testes, como declaração de métodos de teste, organização de testes em classes e categorias, além de recursos de asserção.

### Testes unitários
Em relação aos testes unitários - que são extremamente importantes no desenvolvimento de softwares - foi possivel notar essa importância na prática, ja que, a partir dos testes, foi possivel identificar problemas no código, além formas de otimizá-lo. 
Um exemplo de identificação de problema a partir dos testes é o Teste 1(descrito a cima), em que o teste ajuda a identificar um erro no método Debit.
Além disso, um exemplo de identificação de possibilidade de melhoria a partir dos testes foi a otimização dos testes 2 e 3(descrito a cima) e da classe Debit, para que tratasse das Exceções de forma mais assertiva.

### Atributos

No contexto do MSTest, aprendi a utilizar os atributos/marcadores especiais que servem para identificar classes e métodos como testes ([TestClass] e [TestMethod]), e a criar a estrutura lógica de um teste de unidade, que verifica unidades individuais de código, como o método "Debit", de forma isolada.


### Asserções

Aprendi também sobre a utilização das Asserçõe dentro dos testes, que possibilitam a verificação de determinadas condições, validando e comparando o comportamento esperado e obtido pelo código durante os testes. Elas são essenciais para o funcionamento do teste, e um exemplo de asserção utilizada é o "Assert.AreEqual".

### Conclusão

A realização do passo-a-passo contribuiu muito para o meu entendimento de testes unitários (tanto conceitualmente como na prática), facilitando a aplicação desse conceito para outros projetos e contextos, incluindo o que está sendo desenvolvido para a Track.co.


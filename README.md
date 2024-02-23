# testes-unitarios-pond-s3m9
 Realização da atividade de criação de testes unitários com C#
 Aluna: Ana Clara Loureiro Muller Zaidan
# Testes realizados
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

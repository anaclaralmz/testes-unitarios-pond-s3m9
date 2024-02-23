# testes-unitarios-pond-s3m9
 Realização da atividade de criação de testes unitários com C#
# Testes realizados
## Teste 1
caso de teste: "verifica que um valor válido (ou seja, um que seja menor que o saldo da conta e maior que zero) retira a quantidade correta da conta."

![img 1](/assets/img1.png)

### primeira tentativa
resultado: não passou

![img 2](/assets/img2.png)

problema: O saldo deveria diminuir, mas em vez disso, ele aumentou pelo valor do saque.

motivo: problema no método Debit, que adiciona o valor, ao invés de subtrair

![img 3](/assets/img3.png)

### segunda tentativa
mudanças: erro no método Debit foi resolvido:

![img 4](/assets/img4.png)

resultado: teste passou

![img 5](/assets/img5.png)

## Teste 2
caso de teste: "verifica se o método Debit gera uma ArgumentOutOfRangeException se o valor do débito é menor que zero."

![img 6](/assets/img6.png)

resultado: teste passou 

![img 7](/assets/img7.png)

## Teste 3
caso de teste: "verifica se o método Debit gera uma ArgumentOutOfRangeException se o valor do débito é maior que o saldo."

![img 8](/assets/img8.png)

resultado: teste passou

![img 9](/assets/img9.png)

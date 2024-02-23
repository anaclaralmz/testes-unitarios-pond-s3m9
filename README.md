# testes-unitarios-pond-s3m9
 Realização da atividade de criação de testes unitários com C#
# Testes realizados
## Teste 1
caso de teste: "verifica que um valor válido (ou seja, um que seja menor que o saldo da conta e maior que zero) retira a quantidade correta da conta.
//imagem1
### primeira tentativa
resultado: não passou
//imagem2
problema: O saldo deveria diminuir, mas em vez disso, ele aumentou pelo valor do saque.
motivo: problema no método Debit, que adiciona o valor, ao invés de subtrair
//imagem3
### segunda tentativa
mudanças: erro no método Debit foi resolvido:
//imagem4
resultado: teste passou
//imagem5

# Solução - Fatorar um número

```javascript
function factorialize(num) {
  if (num === 0) { return 1; }
  
  return num * factorialize(num - 1);
}

factorialize(5);
```

### Explicação do código
- Para solucionar esse problema, utilizamos [funções recursivas](http://blog.da2k.com.br/2015/02/27/javascript-como-funcionam-as-funcoes-recursivas/) que de modo geral, é quando você chama um método ou função para ela mesma. Neste caso, chamamos funcão `factorialize(num - 1)` dentro da própria função `factorialize()`.
- Primeiro verificamos se o número é 0, se for, interrompemos a recursão e retornamos 1, já que `0! = 1`.
- Se o número for maior que zero, nós retornamos o número múltiplicado pelo retorno da própria função, passando como parâmetro o número menos 1.

---

##### Exemplo da interação
Dando como exemplo o `5!`. Vamos chamar a função `factorialize(5)`.

O número 5 é igual a 0 ou 1? **Não** -> Vamos continuar com a função...

**Retorno**
(5 (_segunda execucao: 4 (_terceira execucao: 3 (_quarta execucao: 2 (_quinta execucao: 1)))))

Podemos interpretar o retorno como `(5 * (4 * (3 * (2 * 1))))` ou `5 * 4 * 3 * 2 * 1` e o retorno da operação será `120`.

[Informação detalhada](https://github.com/freeCodeCamp/freeCodeCamp/wiki/Algorithm-Factorialize-A-Number)

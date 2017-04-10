# Solução - Reverta uma string

### Solução básica - Passo a passo
```javascript
function reverseString(str) {
  var strSplited = str.split('');
  var arrayReverse = strSplited.reverse();
  var stringReverse = arrayReverse.join('');
  
  return stringReverse;
}

reverseString('javascript');
```

### Solução enxuta
```javascript
function reverseString(str) {
  return str.split('').reverse('').join('');
}

reverseString('javascript');
```

### Explicação do código
- Nosso objetivo é receber uma string e retornar o valor revertido.
- O primeiro passo é dividir a string em para que possamos transformá-la em array. Para isso, nós utilizamos a função `split()`.
- Depois revertemos a array obtida utilizando a função `reverse`.
- Por último, utilizamos a função `join()` para juntar todos os caracteres e formar nossa string revertida.
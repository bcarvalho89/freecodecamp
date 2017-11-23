# Solução - Retorne o maior número do array

### Solução básica - Passo a passo
```javascript
function largestOfFour(arr) {
  var largestArr = [];
  
  for (var i = 0; i < arr.length; i++) {
    var largestNumber = arr[i][0];
    
    for (var j = 0; j < arr[i].length; j++) {
      if (arr[i][j] > largestNumber) {
        largestNumber = arr[i][j];
      }
    }
    
    largestArr.push(largestNumber);
  }
  
  return largestArr;
}

largestOfFour([[4, 5, 1, 3], [13, 27, 18, 26], [32, 35, 37, 39], [1000, 1001, 857, 1]]);
```

### Solução enxuta
```javascript
return arr.map(function(item) {
    return item.reduce(function(prev, current) {
      return (current > prev) ? current : prev;
    });
});

largestOfFour([[4, 5, 1, 3], [13, 27, 18, 26], [32, 35, 37, 39], [1000, 1001, 857, 1]]);
```

### Explicação do código
- Primeiro iremos criar um `array` temporário vazio para armazenar nossos números.
- Vamos iterar em cada item do `array` fornecido e atribuir a váriavel `largestNumber` para o primeiro item do `array`.
- Temos que iterar novamente, agora para cada item dentro do `array`, no qual fazemos a verificação: Se o valor atual for maior do que o armazenado em `largestNumber`, definimos `largestNumber` com o novo valor.
- Por último, adicionamos o número maior ao `array` temporário e retornamos esse `array`.
# Solução - Primeira letra maiúscula na frase

### Solução básica
```javascript
function titleCase(str) {
  var strSplited = str.toLowerCase().split(' ');
  
  for (var i = 0; i < strSplited.length; i++) {
    strSplited[i] = strSplited[i].charAt(0).toUpperCase() + strSplited[i].slice(1);
  }
  
  return strSplited.join(' ');
}

titleCase("I'm a little TEA pOt");
```

### Explicação do código
- Devemos dividir a frase (string) em um array de palavras.
- Definimos a palavra atual no loop sendo ela o primeiro caracter da palavra `charAt(0)` em letra maiúscula. Depois concatenamos a mesma palavra, removendo o primeiro caracter.
- Por último, retornamos a frase completa.
# Solução - Encontre a palavra mais longa numa string

### Solução básica
```javascript
function findLongestWord(str) {
  var wordsOfString = str.split(' ');
  var longest = '';
  
  for (var i = 0; i < wordsOfString.length; i++) {
    if (wordsOfString[i].length > longest.length) {
      longest = wordsOfString[i];
    }
  }
  
  return longest.length;
}

findLongestWord("The quick brown fox jumped over the lazy dog");
```

### Explicação do código
- Devemos dividir a frase (string) em um array de palavras. Declaramos a variável `longest` para guardar a palavra mais comprida.
- Criamos um loop em `for` para verificar o comprimento de cada palavra do array.
- Se a palavra atual do `for` for mais comprida que a palavra guardada na variável `longest`, defimos essa palavra como sendo o novo valor de `longest`.
- Por último, retornamos o comprimento da palavra.
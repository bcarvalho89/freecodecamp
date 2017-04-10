# Solução - Verificar palíndromos

### Solução básica - Passo a passo
```javascript
function palindrome(str) {
  var strOriginalNonAlpha = str.replace(/[\W_]/g, '');
  var strToCompare = strOriginalNonAlpha.split('').reverse().join('');
  
  if (strOriginalNonAlpha.toLowerCase() === strToCompare.toLowerCase()) {
    return true;
  }
  
  return false;
}

palindrome('A man, a plan, a canal. Panama');
```

### Solução enxuta
```javascript
function palindrome(str) {
  return str.replace(/[\W_]/g, '').toLowerCase() === 
         str.replace(/[\W_]/g, '').toLowerCase().split('').reverse().join('');
}

palindrome('A man, a plan, a canal. Panama');
```

### Explicação do código
- Começamos usando expressões regulares para substituir qualquer espaço em branco ou caracteres que não sejam alfanuméricos por vazio `''`. O código da expressão regular `/[\W_]/g` significa: encontre todas as ocorrências de caracteres que não sejam alfanuméricos `\W` e underline `_`.
- Depois usamos o a lógica do exercício [Reverta uma string](https://github.com/bcarvalho89/freecodecamp/tree/master/pt_BR/reverta-uma-string) para reverter a string na qual já removemos os caracteres indesejados.
- Por fim, comparamos a string original e a string reversa em caixa baixa. Se as strings forem iguais, é um palíndromo.
# Operador de propagação (Spread Operator)

> [TODO - FINALIZAR]

> [TODO - REVISAR]

O Operador Propagação permite que uma expressão seja expandida em locais onde são esperados vários argumentos (chamadas de função) ou múltiplos elementos (arrays literais).

Para entender melhor este recurso observe o seguinte exemplo:

```typescript
function myFunc(...val: string[]) {
    //...
}

var values = ['dog', 'cat'];

myFunc('dog', 'cat');

myFunc(...values);
```

Veja que a função `myFunc` possui um parâmetro do tipo rest parameter. Esta função pode ser chamada opcionalmente passando um array seguindo a mesma sintaxe usada na assinatura da função `...`.

Podemos facilmente recuperar os valores dentro da função `myFunc` utilizando um recurso chamado `Destructuring` (Veremos este recurso com mais detalhes em outro capitulo). Exemplo:


```typescript
function myFunc(...val: string[]) {
    var [val1, val2] = val;
    //...
}
```

Este recurso também pode ser utilizado na construção de arrays:


```typescript
fvar array1 = [1, 2, 3];
var array2 = [0, ...array1, 4, 5, 6];
```

Exemplo concatenando 2 arrays usando a função `push`:


```typescript
var arr1 = [0, 1, 2];
var arr2 = [3, 4, 5];
arr1.push(...arr2);
```

> [TODO] O seguinte exemplo não está funcionando ainda com a versão 1.5-beta do ts
```typescript
function foo(x, y, z) { }
var args = [0, 1, 2];
foo(...args);
```

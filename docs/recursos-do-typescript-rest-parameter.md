# Rest Parameters

> [TODO - REVISAR]

Este recurso nos permite recuperar todos os parâmetros informados para uma função como um unico argumento do tipo array. Para entender melhor vamos a um exzemplo:

```typescript
function buildName(firstName: string, ...restOfName: string[]) {
	return firstName + " " + restOfName.join(" ");
}

var employeeName = buildName("Joseph", "Samuel", "Lucas", "MacKinzie");
```

Note que a assinatura desta função declara 2 parâmetros diferentes: `firstName: string` e `...restOfName: string[]`. Ao utilizarmos o símbolo `...` na declaração do segundo argumento estamos dizendo ao compilador que todos os argumentos passados a para a função `buildName` partir do segundo serão agrupados em um array. Note que o operador `...` só pode ser aplicado a um argumento do tipo array e que este precisa ser sempre o ultimo argumento da função. Este recurso é chamado de `Rest Parameter`.

{% include "./footer.md" %}

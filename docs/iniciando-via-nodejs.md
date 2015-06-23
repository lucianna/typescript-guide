# Via NodeJS

> [TODO - REVISAR]

> [TODO - FINALIZAR]

A forma mais rapida de iniciar ŕ usando o [nodejs](https://nodejs.org/).

> [TODO] Falar um pouco mais sobre o node

Acesse o site https://nodejs.org/ e baixe a versão do nodejs mais recente para o seu sistema operacional.

Feita a instalação vamos agora instalar o typescript. Use a seguinte linha de comando:

```shell
npm install -g typescript
```

crie um arquivo com o seguinte código TypeScript:

```typescript
class Person {
    private _name: string;

    constructor(name: string) {
        this._name = name;
    }

    public getName() {
        return this._name;
    }
}

var person = new Person('joão');

console.log(person.getName());
```

Salve este arquivo com o nome: `person.ts`. Agora para compilar este arquivo use o comando:

```shell
tsc person.ts
```

Note que um arquivo chamado `person.js` será gerado. Este novo arquivo possui o código javascript gerado pelo compilador do TypeScript. Para executar este arquivo utilize o próprio nodejs via linha de comando:

```shell
node person.js
```

{% include "./footer.md" %}

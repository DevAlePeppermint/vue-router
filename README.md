# rotas-exercicios
Repositorio contendo meus exercicios de rotas
## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Run your tests
```
npm run test
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
## Informações

Criando uma nova função Router construtora, passando um objeto como parametro.
Esse parametro, routes, é um array de objetos com um par de parametros:
 -path, que é o caminho
 -component, que é o componente que será renderizado.

Depois disso, é necessario registrar ele em main.js

Por ultimo, setar aonde queremos que, no nosso template, o conteudo do router 
será exibido. Nós vamos colocar em App.vue

### Navegação (ou Modos de Rota)

Existem dois possiveis modos de navegação
-Hash: localhost:8080/#/...
-History: localhost:8080/...

Basicamente, a diferença entre os dois é a passagem pelo "index.html". No modo hash,
garantimos que a requisição vá para o index e tambem que o servidor nao saiba o que tem
depois do hash (fica salvo localmente). A request q vai pro browser vai ate o /#/,
o restante fica somente sob conhecimento do navegador.

O modo History precisa de uma configuração adicional no servidor, pois o conteudo 
depois da hash será enviado. Nesse caso, o servidor toma conhecimento e ele precisa 
redirecionar todas as requisições pro index.html

Para trocar o modo, você precisa colocar no seu objeto-parametro da função Router:
```
{ 
    mode: 'hash',
    router: [{
        ...
    }]
}
```
OU
```
{ 
    mode: 'history',
    router: [{
        ...
    }]
}
```
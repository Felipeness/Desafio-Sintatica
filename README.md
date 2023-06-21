# Desafio-Sintática
Desafio para vaga de full stack developer na empresa Sintática.
Este é um repositorio para versionar e organizar o projeto do desafio 

## Como funciona

Esta é uma aplicação JS que utiliza o Vite como bundler e o Bootstrap como framework CSS sendo alinhado ao SASS.

## Como executar

Acesse o diretório do projeto e execute o comando:

```bash
npm install
npm preview
```

## Passo a passo

1. [x] Criar o projeto com o Vite
2. [x] Instalar e configurar o Bootstrap. Site caso precise: https://getbootstrap.com/docs/5.3/getting-started/vite/
3. [x] Criar as sessões da página Home
4. [x] Criando cada sessão/componente


### Passo 1: Criar o projeto com o Vite

Para criar o projeto, vamos utilizar o [Vite](https://vitejs.dev/), um bundler extremamente rápido e simples de configurar.

```bash
npm create vite@latest
```

E depois escolher as seguintes opções:

- `? Project name: › Js-Super Mario-form`
- `? Select a framework: › Vanilla`
- `? Select a variant: › Javascript`

Referências:

- <https://vitejs.dev/guide/>

### Passo 2: Instalar e configurar o TailwindCSS

Para instalar o Bootstrap, vamos utilizar o [PostCSS](https://postcss.org/), um processador de CSS que nos permite utilizar plugins para transformar nosso CSS.

```bash

npm i --save-dev vite
npm i --save bootstrap @popperjs/core
npm i --save-dev sass

```

Na sequência, vamos ajustar o arquivo `vite.config.js` com o seguinte conteúdo:

```js
/** @type {import('tailwindcss').Config} */
const path = require('path')

export default {
  root: path.resolve(__dirname, 'src'),
  build: {
    outDir: '../dist'
  },
  server: {
    port: 8080
  }
}
```

E adicionar os plugins Prettier para o Bootstrap:

```bash
npm install -D prettier prettier-plugin-bootstrap eslint-plugin-prettier
```



```js

Importar Bootstrap 
Importe o CSS do Bootstrap. Adicione o seguinte para importar todo o Sass de origem do Bootstrap.src/scss/styles.scss

```bash
// Import all of Bootstrap's CSS
@import "bootstrap/scss/bootstrap";
Você também pode importar nossas folhas de estilo individualmente, se desejar.
```

Em seguida, carregamos o CSS e importamos o JavaScript do Bootstrap. Adicione o seguinte para carregar o CSS e importar todos os JSs do Bootstrap. O Popper será importado automaticamente através do Bootstrap.src/js/main.js

```bash
// Import our custom CSS
import '../scss/styles.scss'
```

```bash
// Import all of Bootstrap's JS
import * as bootstrap from 'bootstrap'
```

Você também pode importar plug-ins JavaScript individualmente, conforme necessário, para manter os tamanhos dos pacotes baixos:

```bash
import Alert from 'bootstrap/js/dist/alert';

// or, specify which plugins you need:
import { Tooltip, Toast, Popover } from 'bootstrap';
```

 Identique e remova todos os arquivos desnessarios.

E finalmente vamos executar o projeto com o comando:

```bash
npm start
```

E abrir o endereço [http://localhost:8080/](http://localhost:8080/) no navegador:

![Hello World](./docs/images/hello-world.png)

Referências:

- [<https://tailwindcss.com/docs/guides/vite>](https://getbootstrap.com/docs/5.3/getting-started/vite/)

## Passo 3: Criar as sessões da página Home

Estrutura do projeto 
Já criamos a pasta e inicializamos o npm. Agora também criaremos nossa pasta, folha de estilo e arquivo JavaScript para completar a estrutura do projeto. Execute o seguinte a partir do , ou crie manualmente a estrutura de pastas e arquivos mostrada abaixo.my-projectsrcmy-project

```bash
mkdir {src,src/js,src/scss}
touch src/index.html src/js/main.js src/scss/styles.scss vite.config.js
Quando terminar, seu projeto completo deve ter a seguinte aparência:
```

```bash
my-project/
├── src/
│   ├── js/
│   │   └── main.js
│   └── scss/
│   |   └── styles.scss
|   └── index.html
├── package-lock.json
├── package.json
└── vite.config.js
```

Dessa forma já temos todas as sessões/componentes da página inicial criadaa e pronto para iniciar a criação de um formulario simples.

## Passo 4: Criando cada sessão/componente

Chegou o momento de criamos cada sessão do nosso site, para isso vamos utilizar o TailwindCSS para nos ajudar com os estilos e estilizar cada uma para que possamos ter a seguinte aparência final.

Você pode consultar cada componente para que entenda como foi feito, mas não se preocupe, pois explicamos cada detalhe no vídeo.

![Site final](./docs/images/site-final.png)

Referências:

- <https://pages.github.com/>
- <https://vitejs.dev/guide/static-deploy.html#github-pages>

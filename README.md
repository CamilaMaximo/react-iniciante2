
# React para Iniciantes

## Ferramentas de Automação

### Conteúdo Extra

#### Linha de Comando  
[Link para o conteúdo: Linha de Comando](https://www.origamid.com/curso/javascript-completo-es6/1001-linha-de-comando)

#### NPM  
[Link para o conteúdo: NPM](https://www.origamid.com/curso/javascript-completo-es6/1002-npm)

### Empacotador

- Agrupa (bundle) o código do seu aplicativo.
- Permite definir os componentes em diferentes arquivos para melhor organização.
- Facilita a importação de código externo instalado via NPM.

## ESBuild Mínimo

[Site Oficial do ESBuild](https://esbuild.github.io/)

### Passos para Configuração

1. Abra um pacote npm na pasta do seu aplicativo:
   ```bash
   npm init -y
   ```

## Instalar o ESBuild

1. Instale o ESBuild:
   ```bash
   npm install esbuild
   ```

2. Adicione os scripts de desenvolvimento e build ao arquivo `package.json`:
   ```json
   "scripts": {
     "start": "esbuild --bundle src/main.jsx --outfile=main.js --servedir=./ --watch",
     "build": "esbuild --bundle src/main.jsx --outfile=main.js"
   },
   ```

---

### Reagir

1. Instale as dependências do React:
   ```bash
   npm install react react-dom
   ```

2. Crie o arquivo `./src/main.jsx`:
   ```javascript
   import ReactDOM from 'react-dom/client';
   import React from 'react';
   import App from './App';

   ReactDOM.createRoot(document.getElementById('root')).render(<App />);
   ```

3. Crie o componente `App` no arquivo `./src/App.jsx`:
   ```javascript
   import React from 'react';

   const App = () => {
     return <a href="https://www.origamid.com">Origamid</a>;
   };

   export default App;
   ```

---

### Inicie o Desenvolvimento

Para iniciar o ambiente de desenvolvimento:
```bash
npm start
```

Para realizar uma compilação final:
```bash
npm run build
```

---

### Recarga ao Vivo

Para atualizar automaticamente a página durante o desenvolvimento, adicione o seguinte script ao final do arquivo HTML:
```html
<script>
  new EventSource('/esbuild').addEventListener('change', () =>
    location.reload(),
  );
</script>
```
```

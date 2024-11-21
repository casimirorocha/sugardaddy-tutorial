
## Requerimentos
* [Laravel Framework (API)](https://laravel.com)
* [Quasar Framework (Frontend)](https://quasar.dev/)
* [Vue.js](https://vuejs.org/)

## Instalar dependências
#### *Abra o terminal/prompt de comando e execute o código abaixo:*
##### Para isso você deve ter instalado o nodejs https://nodejs.org/pt
```bash
cd frontend/quasar-app
npm install ou yarn install
```

### Para rodar o app em um servidor local de desenvolvimento use o comando:
```bash
npx quasar dev ou yarn dev ou yarn quasar dev
```
### Para compilar o app para produção use o comando:
```bash
npx quasar build ou yarn quasar build
```
- Após rodar este comando será criada chamada: dist

## Configurar o Laravel
- Altere as variáveis de ambiente no arquivo da pasta raiz laravel-api/.env

## Conectar o frontend com o laravel
```javascript
// Altere os dados do arquivo: frontend/quasar-app/quasar.config.js

env: {
    API: ctx.dev
    ? 'http://localhost:8000' // URL DA API DE DESENVOLVIMENTO
    : 'https://api.seusite.com.br' // URL DA API DE PRODUÇÃO
}
```

## Alterar o nome do app no frontend
```javascript
// Altere os dados do arquivo: frontend/quasar-app/src/boot/config.js

const API_URL = PUBLIC_PATH + '/api/'

// "async" is optional
export default async ({ store, Vue, firebase }) => {
  AddressbarColor.set('#ee111') // COR EM HEXADECIMAL PARA A BARRA DE NAVEGAÇÃO EM DISPOSITIVOS MÓVEIS
  Vue.prototype.$appName = 'Meu App Tal' // ALTERE PARA O NOME DO SEU APP
  Vue.prototype.$storagePath = ''
  Vue.prototype.$pusherAuthEndpoint = `${API_URL}broadcasting/auth`
  Vue.prototype.$usernamePlayStore = 'playstore_user'
}
```

## Support

Caso sinta dificuldades em configurar e instalar, me avise no whatsapp que eu te ajudo:

* [+55 (98) 99150 - 4942](https://web.whatsapp.com/send?phone=5598991504942)

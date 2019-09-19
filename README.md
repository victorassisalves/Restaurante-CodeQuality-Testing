# Nadia’s Garden Restaurant

Esse é um site construido em Node.js e Express que aceita uma lista de reservas para o restaurante. Estou melhorando a estrutura do site com testes e qualidade de código com o curso do Linkedin "Node.js: Testing and Code Quality" feito pelo Jon Peck.

O site começa com erros intencionais no backend como não validação de endereços de email. Inconsistências no estilo o código também são intencionais.

## Começando o Projeto

```bash
npm install
npm start
```
O servidor roda na porta 3000.

O site tem 3 rotas:

- http://localhost:3000/ - Página inicial
- http://localhost:3000/reservations - Manda as requisições de reserva
- http://localhost:3000/admin - Veja todas as requisições de reserva; Autorização básica login/senha `admin/admin`

O Banco de dados no site é feito usando SQLite3 com o arquivo `database.sqlite`

## Development

### Debugging

This project uses https://www.npmjs.com/package/debug for development logging. To start `nodemon` and enable logging:

```bash
npm run debug
```

## FAQ

- Q: Why didn't you store the time submitted?
  - A: I wanted to reduce the number of fields and simplify testing.
- Q: Wouldn't it be easier if the form submitted a datetime string instead of building and parsing one?
  - A: Yes, it would, but the form logic is simpler. Either way, someone has to do the work.
- Q: Why did you mix a callback and a Promise in `lib/reservations.js`?
  - A: `Joi` doesn't support Promises, but it does support callbacks. I wanted to show how to test both kinds of asynchronous code.
- Q: How'd you handle cross-platform support?
  - A: Avoided relative directories, used `cross-env` to transform environmental variables.

## Credits

This is an adaptation of a WordPress site hosted at http://587672.youcanlearnit.net/

The conversion:

- Archive original with wget
- Strip out unrelated functionality
- Reorganize JavaScript and Stylesheets into logical directories
- Converted HTML into Jade / Pug templates using http://html2jade.org/

The front end should be mostly unchanged from the original.

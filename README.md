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

## Informações Gerais

### Qualidade do código:

  Qualidade de pode ser dividida em:

  #### Funcionalidade:

  - O código faz o que deveria ser feito?
     > Armazenar email: Não armazenar representa falha no armazenamento de dados, armazenar um não email representa falha na validação dos dados.

  ### Sem Deficiências

  Não podem apresentar falhas ou erros, isso pode ser resumido de duas formas:

  - #### Utilidade
    - Flexível e reutilizável 
        > Ter a possibilidade de reutilizar, e com mais de uma forma possível. 
        > Ex.  Função que soma um número X com 1 (return x +1). É reutilizável porém inflexível.
        > Ex. Função que soma um número X a qualquer número N (return x + n). É reutilizável e muito mais flexivel. Muito mais útil.
  - #### Possibilidade de Manutenção
    
    Existem três perguntas para definir se um código é `Sustentável` (Maintainable):
    - Você consegue dar manutenção no código?
    - Outra pessoa consegue dar manutenção no código sem sua ajuda?
    - Outras pessoas conseguem ler e entender o estilo e intenções do código?
    
    > Caso a resposta para as três perguntas acima seja sim, ***Parabéns, você já está melhor que quase todos os desenvolvedores do mundo HEHE.

  Note que pode começar com um código ruim e ir melhorando ao longo do tempo. Sempre tente voltar em códigos antigos e fazer mudanças pequenas para não acarretar em problemas no software.



## Credits

This is an adaptation of a WordPress site hosted at http://587672.youcanlearnit.net/

The conversion:

- Archive original with wget
- Strip out unrelated functionality
- Reorganize JavaScript and Stylesheets into logical directories
- Converted HTML into Jade / Pug templates using http://html2jade.org/

The front end should be mostly unchanged from the original.

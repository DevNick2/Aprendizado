# Aprendizado
> Este projeto é uma documentação do meu trajeto de aprendizado no mundo do desenvolvimento, abaixo está disponível todas as informações que pesquisei, estudei e testei ao longo de minha jornada no mundo da programação.
> Como foram muitos conteúdos lidos, resumidos e testados podem haver divergências nos conteúdos aqui descritos com o que talvez você conheça, assim peço a gentileza de me enviar sugestões de correções ou adição de conteúdo e texto.
> O objetivo deste projeto é poder ajudar outras pessoas que também estão no mundo da programação e precisam de algo um pouco mais detalhado e objetivo.
> O que me motivou a criar este documento foi justamente encontrar a resposta para diversos problemas que eu tive ao longo do trajeto, espalhados pela web, assim decidi criar um documento registrando minha jornada.

## Sumario 
1. [API](#api)
2. [ESLINT](#eslint)
3. [Azure](#azure)
4. [Readme.md](#readme)
5. [GIT](#git)
6. [Javascript](#javascript)
7. [PHP](#php)
8. [NodeJS](#nodejs)
9. [React](#react)
10. [React Native](#react-native)
11. HTML5
12. CSS3
13. SASS
14. Programação Funcional
15. Pattern Strategy
16. Pattern MVC
17. Pattern Factory
18. Pattern Sigleton
19. Atomic Design
20. Webpack
21. Axios
22. JWT
23. DevOps
24. Gulp
25. PM2
26. Mysql
27. Postgree
28. MongoDB
29. Mongoose
30. Sequelize
31. Arquitetura de Software
32. Modelagem de Dados
33. SWAGGER
34. HAPI
35. Express
36. Angular
37. JSPOO
38. Joi
39. BoomJs
40. CORS
41. Links

## 1 - API 
É um conjunto de rotinas e padrões de programação para acesso a um aplicativo baseado na Web.

Responsavel por estabelecer a comunicação entre diferentes serviços, assim pode-se criar e comunicar com várias outras aplicações  sem a necessidade principal de construir novas API's ou novas estruturas de back-end.

**Endpoint:** O conceito de ENDPOINT dentro de Web Services é a URL onde seu serviço pode ser acessado por uma aplicação cliente, em outros casos pode ser considerado como **algo que está nas pontas**, como no caso do par de cada ponta da conexão TCP.

### 1.2 - REST -> REpresentational State Transfer(Transferencia de Estado Representativo)
A transferencia de dados é feita de uma maneira **simbólica**, **figurativa**, **representativa**, de maneira didática.
A transferencia de dados é geralmente usando protocolo **HTTP**.

**Resource:** É a abstração sobre um determinado tipo de informação que uma aplicação gerencia, para que se aplique ao padrão REST __cada recurso precisa ter uma identificação única__ exemplo: __http://URI/RESOURCE_NAME/INFO__

### 1.3 - RESTFul
É a aplicação de todos os padrões REST na API.

### 1.4 - Padrões para ser RESTFul 

- Cliente separado do Servidor: Separação do cliente e do servidor, dessa forma, podemos ter uma portabilidade do sistema;
- Stateless (Sem estado): Cada requisição que o cliente faz para o servidor, deverá conter todas as informações necessárias para o servidor entender e responder a requisição, Exemplo: a sessao do usuario devera ser enviada em todas as requisições para saber se aquele usuario esta autenticado e apto a usar os serviços, o servidor não pode armazenar que o cliente foi autenticado antes;
- Cacheable: As respostas para uma  requisição deverão ser explicitas ao dizer se aquela requisição pode ou não ser cacheada pelo cliente;
- Layered System (Sistema em camadas): o cliente acessa a um endpoint sem precisar saber da complexidade de quais passos estão sendo necessários para o servidor responder a requisição, ou quais outras camadas o servidor estará lidando para que seja respondido;
- Code on Demand (Opcional): Da a possibilidade da nossa aplicação pegar codigos como javascript no lado do cliente;
- Uniform Interface (Interfacec uniforme): Manter o padrão na construção da API, consistente, constante, padrão ou coerente.

### 1.5 Verbos HTTP
Existem diversos porém os mais utilizados são:
- GET: Buscar dados, pode ser usado com parâmetros;
- POST: Enviar dados ou informações para serem processadas, utiliza-se de um corpo (body);
- PUT: Atualizar dados, com um parâmetro de identificação obrigatório e um corpo com novos dados, no caso de usar este verbo indica-se que **envie no corpo todos os dados** independente de qual de fato foi alterado, para enviar apenas um dado alteardo por convenção utilizar o verbo PATCH;
- PATCH: Usado para editar o recurso sem a necessidade de enviar todos os atributos, com um parâmetro de indicação obrigatório;
- DELETE: Deletar, remover ou apagar dados, com um parâmetro de identificação obrigatório.

### 1.6 Boas Práticas na criação de API's
- Utlizar verbos HTTP adequados para as requisições;
- Não utilizar barras no final da recursos;
- Use o mesmo padrão de URI na identificação dos recursos;
- Nunca deixe o cliente sem resposta;
- Na construcao da chave secreta do token usar o mesmo numero de bits do token.

### 1.7 Status das respostas
- 1xx: Informação
- 2xx: Sucesso
    - 200: OK
    - 201: CREATED
    - 204: NOT CONTENT (PUT POST DELETE)
- 3xx: Redirection
- 4xx: Client Error
    - 400: Bad Request
    - 404: Not Fund:
- 5xx: Server Error
    - 500: Internal Server Error

## 2 - ESLINT  
Comandos úteis:
- eslint --init: Inicia uma configuração, respondendo as perguntas, ao finalizar gera um arquivo .eslintrc||.json||.js||.yaml
- eslint [file.js]: Efetua a verificação do arquivo e mostra um log com os erros no formato [line]:[column] error [message]
- eslint --fix [file.js]: Executa a correção dos erros que forem encontrados

## 3 - Azure 
Armazenar informações uteis acerca da utilização do AZURE e de como construir e fazer o deploy de uma API.

### 3.1 Estrutura base para a API for Azure (AFA - API For Azure)
Existem diversas maneiras de fazer o deploy de uma aplicação para o AZURE vou descrever apenas 1:

- Deploy via GIT, VSCode ou CLI: 
    - Ao realizar o deploy por alguns destes modelos o AZURE vai buscar pelos arquivos de iniciailização do projeto: app.js, server.js ou comando no package.json na raiz do projeto.
- É obrigatório o uso do .gitignore;
- No arquivo de inicialização: Manter o host como automático ou remove-lo da configuração e manter a porta como: process.env.PORT || [LOCAL_PORT]
- O arquivo process.json faz parte da orquestracao do PM2 e pode ser opcional.

## 5 - Links 
1. https://blog.caelum.com.br/rest-principios-e-boas-praticas/
2. https://github.com/mysqljs/mysql#introduction
3. https://eslint.org/
4. https://pt.stackoverflow.com/questions/86399/qual-a-diferen%C3%A7a-entre-endpoint-e-api
5. https://www.devmedia.com.br/servicos-restful-verbos-http/37103

###### Anotações em Geral

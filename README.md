# Aprendizado
> Este projeto é uma documentação do meu trajeto de aprendizado no mundo do desenvolvimento, abaixo está disponível todas as informações que pesquisei, estudei e testei ao longo de minha jornada no mundo da programação.
>
> Como foram muitos conteúdos lidos, resumidos e testados podem haver divergências nos conteúdos aqui descritos com o que talvez você conheça, assim peço a gentileza de me enviar sugestões de correções ou adição de conteúdo e texto.
>
> O objetivo deste projeto é poder ajudar outras pessoas que também estão no mundo da programação e precisam de algo um pouco mais detalhado e objetivo.
>
> O que me motivou a criar este documento foi justamente encontrar a resposta para diversos problemas que eu tive ao longo do trajeto, espalhados pela web, assim decidi criar um documento registrando minha jornada.

## Sumario 
1. [API](#1---api)
2. [ESLINT](#2---eslint)
3. [Azure](#3---azure)
4. [Readme.md (Em breve)]
5. [GIT (Em breve)]
6. [Javascript (Em breve)]
7. [PHP] (#7---php)
8. [NodeJS (Em breve)]
9. [React](#9---react)
10. [React Native] (#10---react_native)
11. [HTML5 (Em breve)]
12. [CSS3 (Em breve)]
13. [SASS (Em breve)]
14. [Programação Funcional (Em breve)]
15. [Pattern Strategy (Em breve)]
16. [Pattern MVC (Em breve)]
17. [Pattern Factory (Em breve)]
18. [Pattern Sigleton (Em breve)]
19. [Atomic Design (Em breve)]
20. [Webpack (Em breve)]
21. [Axios (Em breve)]
22. [JWT (Em breve)]
23. [DevOps (Em breve)]
24. [Gulp (Em breve)]
25. [PM2 (Em breve)]
26. [Mysql (Em breve)]
27. [Postgree (Em breve)]
28. [MongoDB (Em breve)]
29. [Mongoose (Em breve)]
30. [Sequelize (Em breve)]
33. [SWAGGER (Em breve)]
34. [HAPI (Em breve)]
35. [Express] (#35---express)
36. [Angular (Em breve)]
37. [JSPOO (Em breve)]
38. [Joi (Em breve)]
39. [BoomJs (Em breve)]
40. [CORS (Em breve)]
41. [AdonisJS] (#41---adonisjs)
42. [PubNub](#41---PubNub)
43. [Links](#42---links)

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

## 7 - PHP

## 9 - React
Toda vez que for embutir javascript dentro do html pelo JSX precisa usar chaves sem aspas.

A sintax **<>html</>** é chamada de fragment, permite criar as divs invisiveis para poder utilizar múltiplos componentes ou tags html dentro de um mesmo componente, essa técnica ajuda quando você não precisa aninhar diversas divs ou esta trabalhando com componentização (quando separa as camadas em componentes).

Ao executar uma funcao de repeticao (map, forEach e etc) precisa inserir a propriedade [key] dentro do elemento html pai:
ex: 
```
    <tr key='indice'>
        map(func())
    </tr>
```
Cada componente do React recebe como parametro um objeto chamado __props__, quando instalamos outras bibliotécas, alguns de seus métodos são acessados através deste parametro, como é o caso da bibliotéca __react-router-dom__, você pode usar a desestruturação para pegar apenas as propiedades que for usar, como exemplo:
Para usar navegacao usamos o __history__ ou __location__, ambas propriedades da bibliotéca __react-router-dom__: 
```
    import React from 'react'
    export default function App({history, location}){
        console.log(history)
        console.log(location)

        return (<h1>Hello World!</h1>)
    }
```
Alguns métodos do history:
```
    history.push('/uri'): Redireciona o usuário
```
Um stateless componente tem a seguinte sintax:
```
export default () => ( jsx )
```

### 9.1 Ferramentas:
**State:**
Para trabalhar com state react:
```
    import React, {useState} from 'react'
    export default function App(){
        const [var, setVar] = useState(valorInicial)

        return (<h1>Hello World</h1>)
    }
```
Funciona parecido com um get and set, o valor inicial pode ser um array vazio, uma string vazia, um valor boolean dentre outros.

**Effect:**
O useEffect é um método que pode executar blocos de códigos antes renderizar o componente, para seu uso considere:
```
    import React, {useEffect} from 'react'
    export default function App(){
        useEffect(function(){
            console.log('Effect em funcionamento!')
        },[])

        return (<h1>Hello World!</h1>)
    }
```
Ao declarar o useEffect com a dependencia vazia ele executa apenas uma vez, se você precisa que execute o mesmo bloco de código baseado em alguma dependencia, inserir esta no array de dependências.

Sintax: useEffect(func(), [array de dependencias]), 

**React Router Dom:**
A biblioteca react-router-dom permite criar rotas dentro de uma aplicação React.
O componente __Switch__ restring a executar apenas uma rota por vez, evitando assim que por acidente a aplicação tente renderizar 2 rotas ao mesmo tempo.

A propriedade __exact__ dentro de __Route__ configura a rota para acessar apenas o valor da __uri__ exatamente igual ao definido em __path__

### 10 - React Native
Muitos dos conceitos utilizados no React JS você pode utilizar aqui no React Native.

Aplicativos moveis usam o conceito de densidade de pixel, usar sempre 3 tamanhos de logo com quantidade de pixels diferentes superiores.

Cada componente precisa ter estilizacao propria.

Todas os componentes __View__ criadas ja possuem [display:'flex'] e [flexDirection:'column'] e todos os componentes de texto precisam ser estilizados.

O React Native, diferentemente do React JS, não utiliza tags html ele é totalmente baseado em componentes, o estilo continua sendo css porém para definição dos estilos usa-se o componente __StyleSheet__ nativo do React Native, abaixo um exemplo:
```
    import {StyleSheet} from 'react-natvie'

    const styles = StyleSheet.create({
        className: {
            ...styles
        }
    })    
```
**Obs:**
As propriedades nao possuem hifens [-], diferentemente de arquivos.css, e os valores sao atribuidos usando aspas simples [''].
Para usar os estilos precisa definir a propriedade __style__ dentro de cada componente:
```
    import React from 'react'
    import {View, StyleSheet} from 'react-native'

    export default function App(){

        return (
            <View style={styles.estilo}>
                <Text>Hello World</Text>
            </View>
        )
    }
```
Você também pode querer utilizar dois estilos dentro de um mesmo componente, para isto basta usar um array para chamar os estilos:
```
    import React from 'react'
    import {View, StyleSheet} from 'react-native'

    export default function App(){

        return (
            <View style={[styles.estilo1, styles.estilo2]}>
                <Text>Hello World</Text>
            </View>
        )
    }
```

### 10.1 Componentes
* Text 
    * Pode colocar texto:
    ```
        import React from 'react'
        import {Text} from 'react-native'

        export default function App(){

            return (
                <Text>Hello World</Text>            
            )
        }
    ```
* View:
    * Container visual, funciona como se fosse uma div, você não pode adicionar textos sem usar o componente text:
    ```
        import React from 'react'
        import {View, Text} from 'react-native'

        export default function App(){

            return (
                <View>
                    <Text>Hello World</Text>       
                </View>            
            )
        }
    ```
* KeyboardAvoidingView:
    * Usado para que a __View__ se desloque ao abrir o teclado, usado apenas para o IOS, no Android é uma ação padrão do sistema, ao declarar este componente precisa definir a propriedade behavior="padding", você pode também definir uma propriedade com condicional para habilitar este componente apenas em dispositivos com IOS:
    ```
        import React from 'react'
        import {KeyboardAvoidingView} from 'react-native'

        export default function App(){

            return (
                <KeyboardAvoidingView enabled={Platform.OS === 'ios'} behavior="padding" >
                    <Text>Hello World</Text>       
                </KeyboardAvoidingView>            
            )
        }
    ```
* AsyncStorage 
    * Método que armazena dados direto no dispositivo, é asincrono, por tanto precisa utilizar async/await ou .then.catch ao utilizar:
    ```
        import React, {useEffect} from 'react'
        import {AsyncStorage} from 'react-native'

        export default function App(){
            useEffect(()=>{
                setItem()

                AsyncStorage.getItem('user').then(resolve=>{
                    console.log(resolve)
                })
            })

            async function setItem(){
                AsyncStorage.setItem('key', 'value')
            }

            return (
                <View>
                    <Text>Hello World</Text>       
                </View>            
            )
        }
    ```

Para usar redirecionamento e navegacao usar o a propriedade do objeto { navigation } = navigation.navigate('NomeRota')
- SafeAreaView
  Cria uma box/view na parte segura de visualizacao dos dispositivo

Para buscar itens e montar em forma de lista ou padrao de sequencia e bom criar um componente para isto
Componentes que nao sao paginas nao tem acesso a propriedade [navigation] por padrao para contornar isto usar a lib [withNavigation] do [react-navigation] que adiciona a propriedade navigation a qualuqer componente que n seja pagina, basta envolver a funcao/componente no metodo [withNavigation(funcname)]

Para usar dois estilos em um elemento usar array [style1, styleN]

###### Erros Comuns:
**Erro da extensão intl:** Este erro ocorreu comigo quando fui instalar o Codigniter 4, assim que iniciou a instalação apresentou o erro abaixo:

```
Problem 1
    - codeigniter4/framework v4.0.0-rc.3 requires ext-intl * -> the requested PHP extension intl is missing from your system.
    - codeigniter4/framework v4.0.0-rc.2.1 requires ext-intl * -> the requested PHP extension intl is missing from your system.
    - codeigniter4/framework v4.0.0-rc.2 requires ext-intl * -> the requested PHP extension intl is missing from your system.
    - codeigniter4/framework v4.0.0-rc.1 requires ext-intl * -> the requested PHP extension intl is missing from your system.
    - Installation request for codeigniter4/framework ^4@rc -> satisfiable by codeigniter4/framework[v4.0.0-rc.1, v4.0.0-rc.2, v4.0.0-rc.2.1, v4.0.0-rc.3].

  To enable extensions, verify that they are enabled in your .ini files:
    - C:\xampp\php\php.ini
  You can also run `php --ini` inside terminal to see which files are used by PHP in CLI mode.
```

**Solução:** Caso você esteja utilizando o XAMPP com a versão PHP 7, abra o php.ini e busque pelo trecho: extension=intl, caso esteja com ponto e virgula na frente (;extension=intl) remova, salve o arquivo e reinicie o servidor.


## 41 - PubNub 

## 42 - Links 
1. https://blog.caelum.com.br/rest-principios-e-boas-praticas/
2. https://github.com/mysqljs/mysql#introduction
3. https://eslint.org/
4. https://pt.stackoverflow.com/questions/86399/qual-a-diferen%C3%A7a-entre-endpoint-e-api
5. https://www.devmedia.com.br/servicos-restful-verbos-http/37103
6. https://www.pubnub.com/blog/realtime-geo-tracking-app-react-native/

###### Anotações em Geral
Para testar se esta conseguindo acessar a porta usar o link: portquiz.net:30000[porta_desejada]

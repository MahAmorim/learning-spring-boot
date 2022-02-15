# Spring Quickstart

## O que você construirá
Você construirá um clássico “Hello World!” endpoint ao qual qualquer navegador pode se conectar.

Você pode até dizer seu nome e ele responderá de uma maneira mais amigável.

## O que você precisará
Um ambiente de desenvolvedor integrado (IDE)

- As opções populares incluem IntelliJ IDEA, Spring Tools, Visual Studio Code ou Eclipse e muito mais.
- Um Kit de Desenvolvimento Java™ (JDK)

Recomende o JDK versão 8 ou versão 11.

## Passo a passo
1. Inicie um novo projeto Spring Boot
Use `start.spring.io` para criar um projeto “web”. ]
Na caixa de diálogo “Dependencies”, procure e adicione a dependência “web” conforme mostrado na captura de tela. 
Clique no botão “Gerar”, baixe o zip e descompacte-o em uma pasta no seu computador.

2. Adicione seu código
Abra o projeto em seu IDE e localize o arquivo `DemoApplication.java` na pasta `src/main/java/com/example/demo`.
Altere o conteúdo do arquivo adicionando o método extra e as anotações. 

O método hello() que adicionamos foi projetado para receber um parâmetro String chamado name e, em seguida, combinar esse parâmetro com a palavra "Hello" no código.

Isso significa que, se você definir seu nome como “Amy” na solicitação, a resposta será “Hello Amy”.

A anotação @RestController informa ao Spring que este código descreve um endpoint que deve ser disponibilizado na web.

O @GetMapping(“/hello”) diz ao Spring para usar nosso método hello() para responder a solicitações que são enviadas para o endereço `http://localhost:8080/hello`.

O @RequestParam está dizendo ao Spring para esperar um valor de nome na solicitação, mas se não estiver lá, ele usará a palavra “Mundo” por padrão.

3. Executar e experimentar
Abra uma linha de comando (ou terminal) e navegue até a pasta onde você tem os arquivos do projeto. 
Podemos construir e executar o aplicativo emitindo o seguinte comando:

- MacOS/Linux: `./mvnw spring-boot:run`
- Windows: `mvnw spring-boot:run`

Com o servidor Apache Tomcat integrado do Spring Boot age como um servidor web e escutando solicitações na porta localhost 8080. 
Na barra de endereços do navegador digite `http://localhost:8080/hello`.
Para testar você pode adicionar algum nome como "Amy" `?name=Amy` no final da URL e ver como a aplicação se comporta.
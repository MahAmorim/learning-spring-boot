# Arquivos de configuração

Na pastar `src>main>resources` encontraremos o arquivo **application** aonde podemores adicionar todas as dependências de configurações do nosso projeto como: 

- Informações de banco de dados, 

- portas que desejamos rodar no nosso servidor, 

- habitilitar e desabilitar logs e etc.


### Categorias

- `application.properties` definido para o perfil padrão
- `application-[perfil].properties` para os arquivos que não são o perfil padrão. 

Exemplo: 
  - arquivo application-dev.properties para o perfil “dev”

  - arquivo application-prod.properties para o perfil “prod”

### Ordem de Carregamento

O Spring Boot, tal como descrito em sua documentação, carrega estes arquivos na seguinte ordem:

1. Arquivo application.properties embarcado na aplicação (classpath) para o perfil padrão.

2. Arquivo application-[perfil].properties para perfis específicos (exemplo: application-dev.properties para o perfil dev) embarcados no projeto.

3. Arquivo application.properties externo ao seu projeto.

4. Arquivo application-[perfil].properties externo ao seu projeto.
# API Clientes

### Configurações iniciais

Para subir a aplicação local, execute a classe **App.java**, localizada dentro do módulo **ms-cliente-app**.

### Testando o microsserviço
O projeto faz uso do **actuator**, portanto, após rodar a classe principal, execute o comando a seguir:
>
> curl --location --request GET 'http://localhost:9091/management/info'

### Arquitetura do projeto

O projeto está desenvolvido em gradle organizado em módulos da seguinte forma:

#### ms-cliente-api
> Contém as classes POJO, DTO, Enums e demais classes que podem ser compartilhadas com outros projetos.

#### ms-cliente-app
> Contém a classe main e demais configurações do projeto. Também deve conter 
> o arquivo application.yml ou liquibase/flyway se houver.


#### ms-cliente-impl
> Core do microsserviço, deve conter as classes de controller, service, business, repository 
> e demais classes destinadas ao core.

#### config-server
O projeto também faz uso do config-server, basta adicionar o 
endereço do servidor dentro do arquivo *application.yml*

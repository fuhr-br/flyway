# Versinamento de banco de dados com Flyway
##  Esta API mostra um exemplo de implementação do Flyway em java com SpringBoot
### Flyway é uma ferramenta de migração e versionamento de banco de dados, que permite aos desenvolvedores gerenciar e automatizar alterações no esquema do banco de dados em projetos de software.

[Saiba mais: por que utilizar e como o Flyway funciona](https://flywaydb.org/documentation/getstarted/why "Link para Documentação oficial - Flyway")

[Configurações básicas para uso em um projeto Java/Spring](/Configura%C3%A7%C3%A3o%20inicial%20-%20Spring%20Boot.md "Link com as configurações básicas do flyway em java com springboot")

[Documentação oficial - Flyway](https://flywaydb.org/documentation/ "Link para Documentação oficial - Flyway")

[PDF da apresentação](./arquivos/Flyway.pdf "Link com PDF da apresentação")

[Slides da apresentação](./arquivos/Flyway.pptx "Link com Slides da apresentação")

[GoogleDrive da apresentação](https://docs.google.com/presentation/d/1Wg32bjSA5k6fjs5JoFUI8ldwVvbBDlan2GmcSmZiY3w/edit?usp=sharing "Link no googledrive da apresentação")

# Configurações para rodar esta API
A API deste projeto é um modelo de implementação básico do flyway.<br>
A API usa um banco em memória que ja está configurado e pode ser acessado via URL no seu navegador conforme descrição abaixo.

### Pré-requisito
* java 11

## Como acessar o DataBase

Para acessar o banco em memória via URL acesse: **http://localhost:8080/h2** <br>
Setar o campo JDBC URL para:  **jdbc:h2:mem:flyway**

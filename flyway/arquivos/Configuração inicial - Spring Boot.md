## Para configurar o Flyway em um projeto Java/Spring, você pode seguir os seguintes passos:

### Pré-requisito
- O banco de dados já deve estar configurado e com as dependências necessárias adicionadas ao projeto.

### 1. Adicione o Flyway como uma dependência em seu projeto. 

Se você estiver usando o Gradle, adicione o seguinte ao seu arquivo <code>build.gradle</code>:

```
dependencies {
    implementation 'org.flywaydb:flyway-core'
}
```

Se você estiver usando o Maven, adicione o seguinte ao seu arquivo <code>pom.xml</code>:

```
<dependency>
  <groupId>org.flywaydb</groupId>
  <artifactId>flyway-core</artifactId>
</dependency>
```
### 2. Configure o Flyway no <code>application.properties</code> do projeto:

```
spring.flyway.url=${database_url}
flyway.baseline-on-migrate=true
spring.flyway.baseline-version=1
spring.flyway.user=${usuario_do_banco_de_dados}
spring.flyway.password=${senha_do_banco_de_dados}
flyway.locations=classpath:/db/migration
```

OBS: é importante que você configure o JPA no <code>application.properties</code> para que ele não gerencie o banco de dados para criação das tabelas:

```
spring.jpa.hibernate.ddl-auto=none
spring.jpa.generate-ddl=false
```
### 3. Crie o diretório onde serão colocados os arquivos de migração utilizados:

O diretório <code>"db/migration"</code> deve ser criado na pasta <code>"src/main/resources/"</code>

O nome do arquivo de migração deve seguir o seguinte formato:

![img.png](img.png "Imagem que mostra a divisão na nomeclatura do arquivo v1.0__create_user_table.sql")

- Parte 1: É a letra "v" maiúscula.
- Parte 2: É a versão de migração; pode ser 1, 001, 1.2.3, etc.
- Parte 3: São os dois sublinhados (_)
- Parte 4: A descrição da migração; você pode separar as palavras com um sublinhado ou traço.
- Parte 5: É a extensão do arquivo.sql
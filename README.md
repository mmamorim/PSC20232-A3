# Avaliação A3
## UC - Programação de Soluções Computacionais - 2023/2

<img src="./assets/dev.gif" width="300px" height="220px" />

### professor
>Marcelo Amorim

Descrição e documentação do projeto **A3 2023/2** da **Unidade curricular de Programação de Soluções Computacionais**. 

## Objetivo
	
Desenvolver em **Java** um sistema Desktop (usando janelas) simples de cadastro com as funcionalidades **CRUD** utilizando como persistencia das informações o banco de dados **SQLite**.

>**O que é CRUD?**
>Acrônimo para representar as operações a serem realizadas com as informações representadas por uma entidade do modelo de dados. (Create, Read, Update, Delete)

>**O que é o SQLite?**
>O SQLite é uma base de dados relacional de código aberto e que dispensa o uso de um servidor na sua atuação. Armazenando seus arquivos dentro de sua própria estrutura, ele é capaz de funcionar muito bem em aplicações diversas, principalmente, websites de tráfego médio e sistemas mobile.

## FASE 1: Por onde começar? Conhecendo um projeto padrão de exemplo

Para auxiliar no desenvolvimento e aprendizagem que será adquira com este projeto, nesta fase é apresentado um modelo de projeto utilizando o **netbeans** como IDE de desenvolvimento. O projeto será desenvolvido e detalhado durante as aulas e a medida que as aulas avançam, as atualizações são realizadas podendo ser acessado na pasta deste repositório localizado em [ProjetoA3](./ProjetoA3/). 

### E se eu quiser desenvolver do zero? Quais foram os passos durante a construção deste modelo de projeto?

Vamos lá. 

#### 1. Criando o projeto netbeans
> O projeto que desenvolvemos em aula utilizou o tipo de projeto **Java with Ant**. Escolher no momento da criação do projeto:

<img src="./assets/tela01.png" width="400px" height="280px" />

#### 2. Adicionar as bibliotecas JAR para o SQLite
> Fizemos o download dos seguintes arquivos armazenando na pasta raiz do projeto criado no passo anterior (conforme pode ser encontrado em [ProjetoA3](./ProjetoA3/).):
> * [slf4j-api-1.7.36.jar](./ProjetoA3/slf4j-api-1.7.36.jar).
> * [slf4j-simple-1.7.25.jar](./ProjetoA3/slf4j-simple-1.7.25.jar).
> * [sqlite-jdbc-3.44.0.0.jar](./ProjetoA3/sqlite-jdbc-3.44.0.0.jar).
>
> Para adicionar as bibliotecas (arquivos .jar) ao projeto, clicar (botão direita) sobre o item **Libraries** e escolher opção **Add jar/folder** e escolher os arquivos acima que deverão ser localizados na pasta raiz do seu projeto. 
> <img src="./assets/tela02.png" width="200px" height="120px" /> <img src="./assets/tela03.png" width="200px" height="120px" />

#### 3. Classes **COM SUPER PODERES** desenvolvidas em aula para ajudar no projeto
> **Classe [BD.java](./ProjetoA3/src/projetoa3/BD.java)**
##### Como usar? Exemplos?
```~java
DB db = new DB("bancodados.db");
db.query("SELECT * FROM times");
while(db.next()) {
    int codigo = db.getInt("codigo");
    String nome = db.getString("nome");
    System.out.println("CODIGO: "+codigo+" NOME: "+nome);
}
db.closeConnection();
```
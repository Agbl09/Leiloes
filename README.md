# 🏷️ Sistema de Leilão Online

Este é um sistema básico de leilões, desenvolvido em Java com integração a um banco de dados MySQL. Ele permite o cadastro, listagem e gerenciamento de produtos em leilão. O projeto foi criado com o objetivo de consolidar conceitos de programação orientada a objetos e manipulação de banco de dados.

## 📌 Funcionalidades

- **Cadastro de Produtos**: Permite inserir novos produtos para leilão, especificando nome e valor inicial.
- **Listagem de Produtos**: Exibe todos os produtos cadastrados com detalhes como ID, nome, valor e status.
- **Gerenciamento de Leilões**: Altera o status dos produtos para "vendido" após realizar uma venda.
- **Persistência de Dados**: Utiliza o banco de dados MySQL para armazenar informações.

## 🛠️ Tecnologias Utilizadas

- **Java**: Linguagem principal do projeto.
- **Swing**: Para a interface gráfica.
- **MySQL**: Banco de dados relacional para armazenar os produtos.
- **JDBC**: Para conexão e manipulação do banco de dados.

## 🚀 Como Executar o Projeto

### Pré-requisitos

- [Java JDK](https://www.oracle.com/java/technologies/javase-jdk-downloads.html) instalado.
- [MySQL](https://dev.mysql.com/downloads/mysql/) instalado.
- Um IDE com suporte a Java Swing, como **NetBeans**.

### Passos

1. **Clone este repositório**:
   ```bash
   git clone https://github.com/Agbl09/Leiloes.git

2. **Configure o banco de dados**:
   - Crie um banco de dados chamado uc11:
     ```sql
     CREATE DATABASE uc11;
     
   - Crie a tabela de produtos com o seguinte script SQL:
     ```sql
     CREATE TABLE produtos (id INT AUTO_INCREMENT PRIMARY KEY, nome VARCHAR(100) NOT NULL, valor INT NOT NULL, status VARCHAR(20) DEFAULT 'A Venda');
     
3. **Configure a conexão com o bando de dados**:
   - Edite o arquivo _conectaDAO.java_ para ajustar as credenciais do bando de dados:
     ```java
     conn = DriverManager.getConnection("jdbc:mysql://localhost/uc11?user=root&password=");
     
4. **Implemente o projeto na sua IDE**:
   - Importe o projeto em sua IDE(por exemplo, NetBeans).
   - Compile e execute a classe principal para iniciar o sistema.

## 📂 Estrutura do Projeto
   ```plaintext
Leiloes/
├── cadastroVIEW.java       # Interface para cadastro de produtos
├── listagemVIEW.java       # Interface para listagem e gerenciamento de produtos
├── conectaDAO.java         # Classe para conexão com o banco de dados
├── ProdutosDAO.java        # Lógica de acesso e manipulação dos dados
└── README.md               # Documentação do projeto
````
## 📋 Como Contribuir
   1. Faça um fork deste repositório.
      
   2. Crie uma branch para sua feature:
      ```bash
      git checkout -b minha-feature
      
   3. Faça suas alterações e realize um commit:
      ```bash
      git commit -m "Adicionada nova feature"
      
   4. Envie para o repositório remoto:
      ```bash
      git push origin minha-feature
   5. Abra um Pull Request neste repositório.

## 📝 Licença
   Este projeto foi desenvolvido para fins educacionais e está disponível para uso e modificação conforme necessário.

   Feito por [Gabriela Rodrigues](https://github.com/Agbl09)
   
![](https://private-user-images.githubusercontent.com/74038190/371756373-fddcdbcd-5ea2-4416-9f59-ca7fd9394aca.gif?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MzM4NDE1NjEsIm5iZiI6MTczMzg0MTI2MSwicGF0aCI6Ii83NDAzODE5MC8zNzE3NTYzNzMtZmRkY2RiY2QtNWVhMi00NDE2LTlmNTktY2E3ZmQ5Mzk0YWNhLmdpZj9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDEyMTAlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQxMjEwVDE0MzQyMVomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTllMjE0NzJlNjM4MWU1ZWM0OTJlZWVlZGQ3ZDI2NGU4ZjZiMmM1MzU1YjVkNGYzOTQ1NWNkODE5YWZlZGFkNGYmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.A-eSTJfvF1HcjnSMa5jIr1SvHTZdim5MPwuTv4Cngb4)
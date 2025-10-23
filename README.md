🛠️ CrudEquip

Sistema de CRUD para gerenciamento de equipamentos com backend em Spring Boot.

📋 Descrição

O CrudEquip é uma aplicação Spring Boot para gerenciar equipamentos, oferecendo operações de criação, leitura, atualização e exclusão (CRUD).
O projeto conta com testes unitários, testes de integração via JMeter e utiliza o banco H2 em memória para facilitar o desenvolvimento e os testes.

🚀 Tecnologias Utilizadas

Linguagem: Java

Framework: Spring Boot

Banco de Dados: H2 (em memória)

Build: Maven

Testes Unitários: JUnit 5

Testes de Performance/Integração: JMeter

⚙️ Como Executar

Clone o repositório:

git clone https://github.com/Phhenrique3/CrudEquip.git
cd CrudEquip


Execute a aplicação:

./mvnw spring-boot:run


A aplicação estará disponível em: http://localhost:8080

⚠️ O banco H2 roda em memória. Para acessar o console do H2, abra: http://localhost:8080/h2-console.
Usuário: sa | Senha: (vazio) | JDBC URL: jdbc:h2:mem:testdb

🧪 Testes
Testes Unitários

O projeto possui testes unitários usando JUnit 5, cobrindo serviços e repositórios.
Para rodar os testes:

./mvnw test

Testes de Integração / Performance

Também é possível testar rotas utilizando JMeter. Um exemplo de script está disponível no repositório para validar POST, GET, PUT e DELETE.

📄 Endpoints

A aplicação expõe as seguintes rotas:

1️⃣ Listar todos os equipamentos
GET /equipamentos


Resposta:

[
{
"descricao": "Gerador Elétrico 220v - Modelo Novo",
"valor": 1999.99,
"tipoEquipamento": "Gerador",
"marca": "VarioPower Pro"
}


2️⃣ Obter equipamento por ID
GET /equipamentos/{id}


Exemplo:

GET /equipamentos/1

3️⃣ Criar um novo equipamento
POST /equipamentos


Exemplo de corpo JSON:

{
"descricao": "Gerador Elétrico 220v - Modelo Novo",
"valor": 1999.99,
"tipoEquipamento": "Gerador",
"marca": "VarioPower Pro"
}


4️⃣ Atualizar um equipamento existente
PUT /equipamentos/{id}


Exemplo de corpo JSON:

{
"descricao": "Gerador Elétrico 220v - Modelo Novo",
"valor": 1999.99,
"tipoEquipamento": "Gerador",
"marca": "VarioPower Pro"
}


5️⃣ Deletar um equipamento
DELETE /equipamentos/{id}

📌 Contribuindo

Fork o repositório

Crie uma branch: git checkout -b feature/nome-da-feature

Faça commit das alterações: git commit -m "Descrição clara da feature"

Envie para o repositório remoto: git push origin feature/nome-da-feature

Abra um Pull Request
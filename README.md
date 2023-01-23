# sql.js

Implemente e trate uma conexão com o seu banco de dados, usando JavaScript. Caso a conexão com o banco tenha sucesso, ele deve retornar uma frase positiva. Se isso não ocorrer, retorne uma frase informando o erro.

const mysql = require('mysql');

const connection = mysql.createConnection({
    host: 'hostname',
    user: 'username',
    password: 'password',
    database: 'database'
});

connection.connect((error) => {
    if (error) {
        console.log("Erro ao conectar com o banco de dados: " + error.message);
    } else {
        console.log("Conexão com o banco de dados estabelecida com sucesso!");
    }
});

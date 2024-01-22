# Doc_Banco_de_Dados
- MySQL
- MariaDB
- MySQLWorkBench

- para acessar o my sql no cmd --> mysql -h localhost -u root -p
---
Básico do banco de dados
---
/* Aqui eu criei meu banco de dados */
---
-- CREATE DATABASE TesteCarrinhoCompra;
---
/* Validando se ele existe */
---
-- SHOW DATABASES;
---
/*Usando meu banco de dados */
---
USE TesteCarrinhoCompra;
---

/* Criando uma tabela */
---
/*
CREATE TABLE Produtos(
	id INT AUTO_INCREMENT PRIMARY KEY, -- chave primaria
	nome VARCHAR(255) NOT NULL,
	preco DECIMAL (10,2) NOT NULL -- 20.10
);
*/
---
/* Create */
---
/*
INSERT INTO produtos (nome, preco) 
VALUES
	('TV', 1000.99) , 
	("Telefone", 999.99)
*/
---
/* Traga tudo da tabela de produtos */
---
-- SELECT id, nome, preco FROM produtos;
---
/* Traga apenas o primeiro produto da tabela de produtos */
---
SELECT id, nome, preco FROM produtos WHERE id = 2;
---
/* Atualizar produto */
---
UPDATE produtos SET nome = 'Tv-led'  WHERE id = 2;
---
/* Deletar produtos */
---
DELETE FROM produtos WHERE id = 4
---
/* SEM WHERE */
UPDATE produtos SET nome = 'Tv-led';

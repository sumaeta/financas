# finanças
## Sobre o projeto
   O projeto tem o objetivo de simular como uma pessoa faria no processo de fazer transação numa agência bancária

### Criando a o banco

   create table if not exists banco (
	numero INTEGER Not NULL,
	nome VARCHAR(50) NOT NULL,
	ativo BOOLEAN NOT NULL DEFAULT TRUE,
	datacriacao TIMESTAMP NOT NULL DEFAULT CURRENT_TIMESTAMP,
	PRIMARY KEY(numero)
);

### Criando a tabela Cliente

CREATE TABLE IF NOT EXISTS cliente (
	numero BIGSERIAL PRIMARY KEY,
	nome VARCHAR(100) NOT NULL,
	email VARCHAR(250) NOT NULL,
	ativo BOOLEAN NOT NULL DEFAULT TRUE,
	data_criacao TIMESTAMP NOT NULL DEFAULT CURRENT_TIMESTAMP
);

### Criando a agência 

CREATE TABLE IF NOT EXISTS agencia(
	banco_numero INTEGER NOT NULL,
	numero INTEGER NOT NULL,
	nome VARCHAR(80),
	ativo BOOLEAN NOT NULL DEFAULT TRUE,
	datacriacao TIMESTAMP NOT NULL DEFAULT CURRENT_TIMESTAMP,
	PRIMARY KEY(banco_numero, numero), 
	FOREIGN KEY(banco_numero) REFERENCES banco (numero)
);

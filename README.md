# financas
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


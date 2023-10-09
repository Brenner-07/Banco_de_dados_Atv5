# Banco_de_dados_Atv5

Código descrito e com visualização prévia em: https://docs.google.com/document/d/1AiHtMfPRswPlb4Z3WZeI4yvkWyVpMRn5BA8hhA7Nqb4/edit

Código SQL utilizado, com ALTER TABLE, por ter faltado na criação da tabela a coluna email:

CREATE TABLE aluno(
    ID SERIAL PRIMARY KEY,
    Nome VARCHAR(20) not NULL,
    Matricula VARCHAR(45) NOT NULL,
    Endereco VARCHAR(50) NOT NULL,
    Telefone VARCHAR(15) not NULL
);

ALTER TABLE aluno ADD COLUMN Email VARCHAR(30) NOT NULL;

INSERT INTO aluno(nome,matricula,email,endereco,telefone) VALUES 
	  ('João Carlos','1234','jcarlos@gmail.com','Rua 13 de maio','(11) 7825-4489'),
    ('José Vitor','2345','jvitor@gmail.com','Rua da Saudade','(11) 7825-6589'),
    ('Paulo André','3456','pandr@gmail.com','Rua Pôr do Sol','(11) 7825-4495');

SELECT * from aluno;

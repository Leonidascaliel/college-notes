## Inner Join
	select * from java 
	inner join dotnet
	on java.professor = dotnet.professor
## Left Join
##### Retorna **todos os registros da tabela da esquerda**, mesmo que não haja correspondência na direita.
	select * from java 
	left join dotnet
	on java.professor = dotnet.professor
## Left Join Exclusivo
	select * from java
	left join dotnet
	on java.professor = dotnet.professor
	where dotnet.professor is null
## Right Join
	select * from java
	right join dotnet 
	on java.professor = dotnet.professor
## Outer Join
	select * from java
	full outer join dotnet
	on java.professor = dotnet.professor
## Outer Join Exclusivo
	select * from java
	full outer join dotnet
	on java.professor = dotnet.professor
	where java.professor is null 
	or dotnet.professor is null

## Comando Completo Exemplo
	create table java
	(
	professor varchar(20) null
	);

	create table dotnet 
	(
	professor varchar(20) null
	);

	insert into java values ('Fabrício'), 
	('Dimas'), ('Glauco')

	insert into dotnet values ('Fabrício'), ('Ricardo')

	--inner join
	select * from java 
	inner join dotnet
	on java.professor = dotnet.professor

	--left join
	select * from java 
	left join dotnet
	on java.professor = dotnet.professor

	-- left join exclusivo
	select * from java
	left join dotnet
	on java.professor = dotnet.professor
	where dotnet.professor is null

	--right join
	select * from java
	right join dotnet 
	on java.professor = dotnet.professor

	--right join exclusivo
	select * from java
	right join dotnet
	on java.professor = dotnet.professor
	where java.professor is null
	
	--outer join
	select * from java
	full outer join dotnet
	on java.professor = dotnet.professor
	
	--outer join exclusivo
	select * from java
	full outer join dotnet
	on java.professor = dotnet.professor
	where java.professor is null 
	or dotnet.professor is null
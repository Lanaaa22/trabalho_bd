# TRABALHO 01:  Flash Açai 
Trabalho desenvolvido durante a disciplina de Banco de dados

# Sumário

### 1. COMPONENTES<br>
> Integrantes do grupo<br>
Ilanna dos Reis Cardoso cardosoilanna96@gmail.com<br>
Mariana Lopes marianalopesgovea@gmail.com<br>
Bruna Ramos Rocha brunaramosrocha72@gmail.com<br>
Daianny Maria dadaymaria1@hotmail.com<br>
...<br>

### 2.INTRODUÇÃO E MOTIVAÇÃO

> A empresa "Flash Açai" visa colaborar com prestador de serviço na distribuição de açaí para o instituto federal do espiríto		Santo,tendo em vista que o local não tem acesso há muitos comércios e que certamente será sucesso, o propretário deseja que 		desde o início de seu negócio tenha total controle de vendas e entradas para que assim tenha maior controle no estoque e em nenhuma hipótese falte matéria prima e etc,visando também ser um ambiente acadêmico é necessário horários estratégicos. Para que as aplicações sejam feitas adequadamente é necessário um sistema com o cadastro do cliente pois assim pode ser feito o controle dos mesmos,já do produto será armazenado código,valor,tamanho e complementos ;outra forma de conseguir saber quais 	produtos<br> e tamanhos são mais vendidos ou não.Nesta aplicação manteremos também informações do funcionário ao proprietário,vizamos essa informação importante pois uma vez que haja erros na entrega do produto será possível que saiba o responsável e assim corrigí-las de<br> maneira mais direta e controle também da data de contratação e etc deste pois entendemos que é muito mais provável alcançar o<br> sucesso se houver uma equipe unida e organizada.<br>
-------- Nossa motivação é a união da equipe pois acreditamos que é o que faz o trabalho alcançar o sucesso -------- 

 

### 3.MINI-MUNDO<br>

>  No sistema desenvolvido para melhor controle do delivery de sua açaiteria "Flash Açai" o dono deseja armazenar informações sobre sua loja e todo o funcionamento.
Nesse sistema será necessário armazenar as informações de cada cliente, que possuirá nome, cpf e telefone. Além disso, será armazenado as informações sobre cada pedido realizado pelo cliente, sendo elas código, valor unitário, quantidade e data_hora. O pedido possuirá também as informações acerca de outras entidades, ou seja as chaves estrangeiras, sendo elas: tamanho do produto, complemento, fruta, calda, forma de pagamento e endereço daquele pedido. Um cliente poderá fazer vários ou nenhum pedido e um pedido poderá ser feito somente por um cliente. Para melhor supervisão, será armazenado nesse sistema as informações de cada funcionario que realiza os pedidos, ele possuirá nome, código, quantidade de dias que ele trabalha semanalmente, e o valor da diária recebida. Um funcionario realiza vários ou nenhum pedido e o pedido é realizado por apenas um funcionário. Além disso o funcionário será responsável pela entrega dos pedidos.


### 4.PERGUNTAS A SEREM RESPONDIDAS E TABELA DE DADOS<br>
#### 4.1 QUAIS PERGUNTAS PODEM SER RESPONDIDAS COM O SISTEMA PROPOSTO?
    a) O sistema proposto poderá fornecer quais tipos de relatórios e informações? 
    b) Crie uma lista com os 5 principais relatórios que poderão ser obtidos por meio do sistema proposto!
    
> A Açaiteria "Açaifes" precisa inicialmente dos seguintes relatórios:

* Relatório que mostre o valor total do pedido de cada cliente.<br>

* Relatório que mostre o nome do funcionário que realizou o pedido. <br>

* Relatório que traga o código de todos os pedidos realizados por cada funcionário e o código do cliente responsável por esse 		pedido.<br>

 * Relatório com a quantidade de pedidos por cada tamanho de Açai, para obter uma relação de demanda.<br>

 * Relatório de obtenha a quantidade de pedidos por Endereço


 > informe quais são as 3 principais entidades do sistema em densenvolvimento<br>(se houverem mais de 3 entidades, pense na importância da entidade para o sistema)   
 
* Pessoa
* Pedido
* Açai

 ### 5 MODELO CONCEITUAL
 ![image](https://user-images.githubusercontent.com/92120359/201478570-eaf82df0-c4c7-40b6-8005-4be313409a82.png)
       
    
#### 5.1 Validação do Modelo Conceitual
> GRUPO 1: Camila,yasmim,Isabellay e Davi nunes<br> GRUPO 2: Eduardo, Paulo Cezar, Nycooly e Elisa<br>

#### 5.2 Descrição dos dados 
* FORMA_CONTATO: Tabela que armazena a forma de contato relativa (e-mail ou número) a cada cliente<br>
* PEDIDO: Tabela que armazena todas as informações de cada pedido feito por um cliente<br>
* ENDERECO: Tabela referente ao endereço de cada Cliente<br>
* PAGAMENTO: Tabela que armazena a forma de pagamento que cada cliente optou<br>
* ACAI: Tabela referente ao açai que foi escolhido por cada cliente<br>
* PESSOA: Tabela referente a pessoa (FUNCIONÁRIO OU CLIENTE) de cada setor. <br>
* CLIENTE: Tabela que armazena as informações do cliente (vinda da tabela pessoa)<br>
* FUNCIONARIO: Tabela que armazena as informações referente ao funcionário (vinda da tabela pessoa)<br>
* ACAI_PEDIDO: Relacionamento referente ao pedido e ao açai escolhido no pedido por cada cliente<br>
* PESSOA_PEDIDO: Relacionamento referênte a pessoa (que pode ser o cliente ou o funcionário) e o pedido<br>

### 6	MODELO LÓGICO
![image](https://user-images.githubusercontent.com/92120359/201478999-d6bfef06-8f9e-4259-ad4e-07a0a6e13090.png)

### 7	MODELO FÍSICO<br>

	drop table if exists FORMA_CONTATO;
	CREATE TABLE FORMA_CONTATO (
	    codigo INTEGER PRIMARY KEY,
	    nome VARCHAR(255),
	    contato VARCHAR(40)
	);

	drop table if exists ENDERECO;
	CREATE TABLE ENDERECO (
	    cep VARCHAR(25),
	    nome_logradouro VARCHAR(255),
	    numero INTEGER,
	    codigo INTEGER PRIMARY KEY,
	    tipo_logradouro VARCHAR(25),
	    bairro VARCHAR(25),
	    estado VARCHAR(25),
	    municipio VARCHAR(25)
	);

	drop table if exists ACAI;
	CREATE TABLE ACAI (
	    codigo INTEGER PRIMARY KEY,
	    tamanho VARCHAR(25),
	    nome VARCHAR(25),
	    descricao VARCHAR(255)
	);

	drop table if exists PAGAMENTO;
	CREATE TABLE PAGAMENTO (
	    codigo INTEGER PRIMARY KEY,
	    forma_pagamento VARCHAR(25)
	);

	drop table if exists PESSOA;
	CREATE TABLE PESSOA (
	    codigo INTEGER PRIMARY KEY,
	    nome VARCHAR(255)
	);

	drop table if exists CLIENTE;
	CREATE TABLE CLIENTE(
		cpf varchar(25),
		FK_PESSOA_codigo INTEGER,
		FK_FORMA_CONTATO_codigo INTEGER,
		FOREIGN KEY (FK_PESSOA_codigo)
	    REFERENCES PESSOA (codigo),
		FOREIGN KEY (FK_FORMA_CONTATO_codigo)
	    REFERENCES FORMA_CONTATO (codigo)
	);

	drop table if exists FUNCIONARIO;
	CREATE TABLE FUNCIONARIO(
		qtd_dia integer,
		diaria float,
		FK_PESSOA_codigo INTEGER,
		FOREIGN KEY (FK_PESSOA_codigo)
	    REFERENCES PESSOA (codigo)
	);

	drop table if exists PEDIDO;
	CREATE TABLE PEDIDO (
	    codigo INTEGER PRIMARY KEY,
	    valor_uni FLOAT,
	    qtd_acai INTEGER,
	    data_hora TIMESTAMP,
	    FK_ENDERECO_codigo INTEGER,
	    FK_PAGAMENTO_codigo INTEGER,
	    FK_PESSOA_cliente_codigo INTEGER,
	    FK_PESSOA_funcionario_codigo INTEGER,
		FOREIGN KEY (FK_ENDERECO_codigo)
	    REFERENCES ENDERECO (codigo),
		FOREIGN KEY (FK_PAGAMENTO_codigo)
	    REFERENCES PAGAMENTO (codigo),
		FOREIGN KEY (FK_PESSOA_cliente_codigo)
	    REFERENCES PESSOA (codigo),
		FOREIGN KEY (FK_PESSOA_funcionario_codigo)
	    REFERENCES PESSOA (codigo)
	);

	drop table if exists ACAI_PEDIDO;
	CREATE TABLE ACAI_PEDIDO (
	    fk_ACAI_codigo INTEGER,
	    fk_PEDIDO_codigo INTEGER,
		FOREIGN KEY (fk_ACAI_codigo)
	    REFERENCES ACAI (codigo),
		FOREIGN KEY (fk_PEDIDO_codigo)
	    REFERENCES PEDIDO (codigo)
	);

	drop table if exists PESSOA_PEDIDO;
	CREATE TABLE PESSOA_PEDIDO (
	    fk_PESSOA_codigo INTEGER,
	    fk_PEDIDO_codigo INTEGER,
		FOREIGN KEY (fk_PESSOA_codigo)
	    REFERENCES PESSOA (codigo),
		FOREIGN KEY (fk_PEDIDO_codigo)
	    REFERENCES PEDIDO (codigo)
	);

           
### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>

	insert into forma_contato(codigo, nome, contato)
	values(1, 'E-mail', 'gustavo43@gmail.com'),
	(2, 'Telefone', '(27) 3419-5155'),
	(3, 'Telefone', '(27) 2250-6347'),
	(4, 'E-mail', 'Eduarda123_l@gmail.com'),
	(5, 'E-mail', 'MariaVa_32@gmail.com'),
	(6, 'Telefone','(27) 2332-2719'),
	(7, 'Telefone','(27) 3750-9836'),
	(8, 'Telefone','(27) 2725-2842'),
	(9, 'Telefone','(27) 2854-2690'),
	(10,'Telefone','(27) 2785-4410');

	insert into endereco(cep, nome_logradouro, numero, codigo, tipo_logradouro, bairro, estado, municipio)
	values ('29024-043', '21 de Novembro', 1110, 51, 'rua', 'São Pedro', 'Espírito Santo', 'Vitória'),
	('29984-023', 'Serafim Derenze', 2213, 52, 'Rodovia', 'Grande Vitória ','Espírito Santo','Vitória'),
	('29876-865', 'Abdo Saad', 5333, 53, 'Rodovia', 'Jacaraípe','Espírito Santo', 'Serra'),
	('29446-048', 'Encanto das Ostras', 4921, 54, 'Residencial', 'São Francisco','Espírito Santo','Serra'),
	('29764-958', '22 de Novembro', 6235, 55, 'rua', 'São Pedro','Espírito Santo','Vitória'),
	('29473-764', 'Das Jandaias', 1267, 56, 'rua', 'Das Laranjeiras', 'Espírito Santo', 'Serra'),
	('29745-140', 'dos Colibris', 354, 57, 'Avenida', 'Morada de Laranjeiras','Espírito Santo', 'Serra'),
	('29465-434', 'Vila Sol', 6077, 58, 'Residencial', 'Morada de Laranjeiras','Espírito Santo','Serra'),
	('29435-724', 'Atlântica', 56445, 59, 'Avenida', 'Morada de Laranjeiras','Espírito Santo','Serra'),
	('29862-867', 'Gardenia', 8788, 50, 'rua', 'Jardim Limoeiro','Espírito Santo','Serra');

	insert into acai(codigo, tamanho ,nome, descricao)
	values (10, '1L','Gulozão Açai' , 'Leite em Pó, Disquete, Sucrilhos, Morango, kiwi, manga e Caramelo'),
	(20, '300ml', 'Gulozin Açai', 'Amendoim, Granola, Banana, Leite Condensado'),
	(30, '500ml','Gula Açai', 'Granola, Leite em pó, Manga, Kiwi e Menta'),
	(40, '300ml', 'Açafit', 'Granola, Amendoim, Banana e Mel'),
	(50, '700ml', 'Gulão Açai', 'Paçoca, Ovomaltine, Abacaxi, Kiwi, Manga, Chocolate'),
	(60, '1L','Gulozão Açai','Shocobow,Amendoim,Disquete, Morango, Abacaxi, Banana, Doce de Leite'),
	(70, '1L','Gulozão Açai', 'Leite em Pó, Granola, Disquete, Morango, Banana, Kiwi e Mel'),
	(80,'700ml', 'Açafit', 'Granola, Amendoim, Banana e Mel' ),
	(90, '300ml', 'Gulozin Açai', 'Paçoca, Granola, Morango e Caramelo'),
	(100,'500ml', 'Açafit', 'Granola, Amendoim, Banana, Manga e Mel');


	insert into pagamento (codigo, forma_pagamento)
	values(61, 'cartão'),
	(62, 'dinheiro'),
	(63, 'pix'),
	(64, 'Pic Pay');

	insert into pessoa(codigo, nome)
	values (001,'Gustavo'),
	(002,'Eduarda'),
	(003,'Maria'),
	(004,'Luiz'),
	(005,'Roberto'),
	(006,'Fernando'),
	(007,'Vitória'),
	(008,'Carlos'),
	(009,'Fábiana'),
	(010,'Marcos');

	insert into cliente(cpf, FK_PESSOA_codigo, FK_FORMA_CONTATO_codigo)
	values('333.752.060-03', 001, 1),
	('232.275.170-78', 006, 6),
	('820.944.040-30', 008, 8),
	('182.691.910-43', 010, 10),
	('994.981.150-36', 005, 7);

	insert into funcionario(qtd_dia, diaria, FK_PESSOA_codigo)
	values(4, 80.00, 2),
	(6, 75.00, 3),
	(3, 20.00, 4),
	(7, 40.00, 7),
	(3, 35.00, 9);

	insert into pedido(codigo, valor_uni, qtd_acai, data_hora, FK_ENDERECO_codigo, FK_PAGAMENTO_codigo, FK_PESSOA_cliente_codigo, FK_PESSOA_funcionario_codigo)
	values(150, 15.00, 2, '2022-06-03 07:04:21', 50, 62, 1, 2),
	(152, 20.00, 1, '2022-04-01 01:07:22', 51, 61, 6, 2),
	(153,  18.00,'2022-06-07 07:06:01', 56, 62, 1, 5),
	(154, 23.00, '2022-04-12 03:05:03', 58, 64, 1, 2),
	(155, 13.00,'2022-03-03 09:08:21', 52, 61, 1, 2),
	(156, 15.00,'2022-12-05 04:01:12', 53, 61, 1, 3),
	(157, 18.00,'2022-11-12 05:08:04', 55, 61, 8, 2),
	(158, 23.00,'2022-10-04 03:05:06', 55, 63, 10, 2),
	(159, 13.00,'2022-03-02 15:02:07', 55, 64, 6, 2),
	(160, 15.00,'2022-09-22 04:45:32', 58, 62, 1, 3),
	(161, 13.00,'2022-06-03 07:04:21', 53, 62, 8, 3),
	(162, 15.00,'2022-04-01 01:07:22', 54, 62, 8, 4),
	(163, 18.00,'2022-06-07 07:06:01', 55, 62, 8, 9),
	(164, 23.00,'2022-04-12 03:05:03', 55, 62, 6, 9),
	(165, 13.00,'2022-03-03 09:08:21', 55, 61, 10, 2),
	(166, 15.00,'2022-12-05 04:01:12', 57, 64, 10, 2),
	(167, 18.00,'2022-11-12 05:08:04', 57, 64, 10, 9),
	(168, 23.00,'2022-10-04 03:05:06', 57, 64, 6, 9),
	(169, 13.00,'2022-03-02 15:02:07', 57, 61, 6, 9);

	insert into acai_pedido (fk_ACAI_codigo, fk_PEDIDO_codigo)
	values(10, 150),
	(20, 152),
	(30, 154),
	(50, 155),
	(90, 167),
	(50, 160),
	(40, 169);

	select * from forma_contato;
	select * from endereco;
	select * from acai;
	select * from pagamento;
	select * from pessoa;
	select * from cliente;
	select * from funcionario;
	select * from pedido;
	select * from acai_pedido;


### 9	TABELAS E PRINCIPAIS CONSULTAS<br>
LINK DO COLAB:
	https://colab.research.google.com/drive/11v6KojDP5KAxL2UXGq8W_K0EnAmODD45?usp=sharing <br>
	
># Marco de Entrega 01: Do item 1 até o item 9.1<br>

#### 9.2	CONSULTAS DAS TABELAS COM FILTROS WHERE (Mínimo 4)<br>

	select FK_PESSOA_codigo, (diaria*qtd_dia) as salario_total from funcionario WHERE (diaria * qtd_dia) > 200;
	
	select * from endereco where municipio = 'Serra';
	
	select * from funcionario where diaria > 50;
	
	select * from acai where tamanho = '1L';
  	
	
#### 9.3	CONSULTAS QUE USAM OPERADORES LÓGICOS, ARITMÉTICOS E TABELAS OU CAMPOS RENOMEADOS (Mínimo 11)
 a) Criar 5 consultas que envolvam os operadores lógicos AND, OR e Not
 	
	/* mostre os campos codigo e salario semanal de cada funcionario */
	select fk_pessoa_codigo, diaria * qtd_dia as salario_semanal from funcionario;

	/* mostre o codigo e o valor total de cada pedido */
	select codigo, valor_uni * qtd_acai as valor_total from pedido;

	/* selecione os dados dos funcionarios que trabalham 4 ou mais dias semanais e menos que 7 */
	select * from funcionario where qtd_dia >= 4 and qtd_dia < 7;

	/* selecione os contatos e o nome da forma de contato onde a forma de contato não é nula */
	select contato, nome from forma_contato where nome is not null;

	/* mostre o nome dos logradouros que pertencem aos bairros Jacaraipe e Morada de Laranjeiras */
	select nome_logradouro from endereco where bairro = 'Jacaraípe' or bairro = 'Morada de Laranjeiras';

	/* mostre o nome, tamanho e descricao dos acais que possuem o tamanho 1 litro */
	select nome, tamanho, descricao from acai where tamanho = '1L';

	/* mostre o codigo e o valor total dos pedidos realizados pelo cliente de codigo 1, renomeie para codigo_acai*/
	select codigo as codigo_acai, qtd_acai * valor_uni as valor_total from pedido where fk_pessoa_cliente_codigo = 1;

	/* selecione a chave do endereco renomeada para codigo_endereco, e a quantidade de acai, onde a quantidade de acai é maior que 2 e menor que 8 */
	select fk_endereco_codigo as codigo_endereco, qtd_acai from pedido where qtd_acai > 2 and qtd_acai < 8;

	/* mostre o codigo e o valor dos pedidos dos clientes que possuem o valor total maior que 60 e menor que 180 reais */
	select codigo, qtd_acai * valor_uni as valor_total from pedido where qtd_acai * valor_uni > 60 and qtd_acai * valor_uni < 180;

	/* mostre o nome do logradouro e o bairro dos enderecos que sao do municipio serra e seu tipo de logradouro é rua */
	select nome_logradouro, bairro from endereco where municipio = 'Serra' and tipo_logradouro = 'rua';

	/* selecione o codigo e a descricao dos acais que possuem tamanho 1L mas que também posssuem o nome de Gulozão Acai */
	select codigo, descricao from acai where tamanho = '1L' and nome = 'Gulozão Açai';


	
	

#### 9.4	CONSULTAS QUE USAM OPERADORES LIKE E DATAS (Mínimo 12) <br>
a) Criar outras 5 consultas que envolvam like ou ilike
b) Criar uma consulta para cada tipo de função data apresentada.

	/* Pessoas que utilizam o email como forma de contato */
	select * from forma_contato where nome like '%E-mail%' 

	/* Endereços que estao em Vitória */
	select * from endereco where municipio like '%Vitória%'

	/* Endereços que tem o tipo_logradouro igual a rua */
	select * from endereco where tipo_logradouro like '%Rua%'

	/* Tamanhos de Açais que mais pede 500ml */
	select tamanho, nome from acai where tamanho like '%500ml%'

	/* Pessoas que utilizam o Telefone como forma de contato */
	select * from forma_contato where nome like '%Telefone%' 

	/* Enderecos no bairro São Francisco */
	select * from endereco where bairro like '%São Francisco%'

	/* Enderecos que estão em uma rua */
	select * from endereco where tipo_logradouro like '%rua%'

	/* Açais de 700ml */
	select tamanho, nome, descricao from acai where tamanho like '%700ml%'

	/* Em quanto tempo foi feita o pedido */
	select codigo, data_hora,(age(current_date,data_hora)) as idade_pedido from pedido

	/* Mês em que foi feito o pedido */
	select codigo, data_hora, extract('month' from data_hora) from pedido

	/* Ano em que foi feito o pedido */
	select codigo, data_hora, extract('year' from data_hora) from pedido

	/* Dia em que foi feito o pedido */
	select codigo, data_hora, extract('day' from data_hora) from pedido


#### 9.5	INSTRUÇÕES APLICANDO ATUALIZAÇÃO E EXCLUSÃO DE DADOS (Mínimo 6)<br>
a) Criar minimo 3 de exclusão
b) Criar minimo 3 de atualização

	/* Aumentando a diaria do funcionario luiz */
	update funcionario set diaria = 100.00 where fk_pessoa_codigo = 004;

	/* diminuindo a carga horaria do funcionario 007 */
	update funcionario set qtd_dia = 5 where fk_pessoa_codigo = 007;

	/* Trocando a forma de pagamento do pedido 150 */
	update pedido set FK_PAGAMENTO_codigo = 61 where codigo = 150;

	/* Demitindo o funcionário 4 */
	delete from funcionario where fk_pessoa_codigo = 004;

	/* Cancelando um pedido */
	delete from pedido where codigo = 168;

	/* Apagando o pedido que já está sendo feito */
	delete from acai_pedido where fk_acai_codigo = 40;

#### 9.6	CONSULTAS COM INNER JOIN E ORDER BY (Mínimo 6)<br>
a) Uma junção que envolva todas as tabelas possuindo no mínimo 2 registros no resultado
b) Outras junções que o grupo considere como sendo as de principal importância para o trabalho
    
	select cliente.fk_pessoa_codigo as codigo_cliente, pessoa.nome as nome_cliente, contato, pedido.codigo as codigo_pedido, bairro, acai_pedido.fk_acai_codigo as codigo_acai, acai.nome, funcionario.fk_pessoa_codigo as funcionario
	from acai_pedido
	inner join pedido
	on(acai_pedido.fk_pedido_codigo = pedido.codigo)
	inner join pessoa
	on(pedido.fk_pessoa_cliente_codigo = pessoa.codigo)
	inner join funcionario
	on(pedido.fk_pessoa_funcionario_codigo = funcionario.fk_pessoa_codigo)
	inner join cliente
	on(pedido.fk_pessoa_cliente_codigo = cliente.fk_pessoa_codigo)
	inner join forma_contato
	on(cliente.fk_forma_contato_codigo = forma_contato.codigo)
	inner join endereco
	on(pedido.fk_endereco_codigo = endereco.codigo)
	inner join acai
	on(acai_pedido.fk_acai_codigo = acai.codigo)
	;

	/* Relatório que traga o codigo dos pedidos e o codigo do funcionario que realizou o pedido ordenados crescentemente pelo codigo dos pedidos. */
	select pedido.codigo, funcionario.fk_pessoa_codigo as funcionario
	from pedido
	inner join funcionario
	on(pedido.fk_pessoa_funcionario_codigo = funcionario.fk_pessoa_codigo)
	order by(codigo);

	select acai_pedido.fk_pedido_codigo as codigo_pedido, acai.tamanho, acai.nome
	from acai_pedido
	inner join acai
	on(acai_pedido.fk_acai_codigo = acai.codigo)
	order by(codigo_pedido);

	select pedido.codigo, pessoa.nome
	from pedido
	inner join pessoa
	on(pedido.fk_pessoa_funcionario_codigo = pessoa.codigo)
	order by(pedido.codigo);

	select pedido.codigo, pessoa.nome
	from pedido
	inner join pessoa
	on(pedido.fk_pessoa_cliente_codigo = pessoa.codigo)
	order by(pedido.codigo);

	select cliente.fk_pessoa_codigo as codigo_cliente, forma_contato
	from cliente
	inner join forma_contato
	on(cliente.fk_forma_contato_codigo = forma_contato.codigo)
	order by(codigo_cliente);


#### 9.7	CONSULTAS COM GROUP BY E FUNÇÕES DE AGRUPAMENTO (Mínimo 6)<br>
a) Criar minimo 2 envolvendo algum tipo de junção

	select funcionario.fk_pessoa_codigo as codigo_funcionario, count(codigo) as qtd_pedidos
	from pedido inner join
	funcionario on(pedido.FK_pessoa_funcionario_codigo = funcionario.fk_pessoa_codigo)
	group by(codigo_funcionario);

	select fk_pessoa_cliente_codigo as codigo_cliente, sum(qtd_acai) qtd_total_pedidos
	from pedido
	group by(codigo_cliente);

	/* Relatório com a quantidade de pedidos por cada tamanho do produto. */
	select tamanho, count(qtd_acai) as qtd_acai
	from acai_pedido
	inner join pedido
	on(acai_pedido.fk_PEDIDO_codigo = pedido.codigo)
	inner join acai
	on(acai_pedido.FK_acai_codigo = acai.codigo)
	group by(tamanho);

	/* Relatório de obtenha a quantidade de pedidos por bairro */
	select bairro, count(pedido.codigo) as qtd_pedido 
	from pedido
	inner join endereco
	on(endereco.codigo = pedido.fk_endereco_codigo)
	group by(bairro);

	/* Relatório de obtenha a quantidade de pedidos por cada forma de pagamento. */
	select pagamento.forma_pagamento, count(FK_PAGAMENTO_codigo) as qtd
	from pedido
	inner join pagamento
	on(pedido.FK_PAGAMENTO_codigo = pagamento.codigo)
	group by(pagamento.forma_pagamento);

	select fk_pessoa_cliente_codigo as codigo_cliente, sum(valor_uni) as valor_total
	from pedido
	group by(codigo_cliente);


#### 9.8	CONSULTAS COM LEFT, RIGHT E FULL JOIN (Mínimo 4)<br>
a) Criar minimo 1 de cada tipo

	/* Left */
	select pessoa.nome as nome_pessoa,
	pessoa.codigo,
	diaria,
	qtd_dia
	FROM pessoa LEFT OUTER JOIN funcionario
	ON (pessoa.codigo = funcionario.fk_pessoa_codigo)

	/*  Right */
	select forma_pagamento,
	pagamento.codigo
	FROM pedido RIGHT OUTER JOIN pagamento
	ON (pedido.codigo = pagamento.codigo)

	/* Full Join */
	select * from cliente right join pessoa on pessoa.codigo = cliente.fk_pessoa_codigo
	union 
	select * from cliente left join pessoa on pessoa.codigo = cliente.fk_pessoa_codigo


#### 9.9	CONSULTAS COM SELF JOIN E VIEW (Mínimo 6)<br>
        a) Uma junção que envolva Self Join (caso não ocorra na base justificar e substituir por uma view)
        b) Outras junções com views que o grupo considere como sendo de relevante importância para o trabalho
	
	create view salario_semanal_funcionario as
	(select fk_pessoa_codigo as codigo_funcionario,
	qtd_dia * diaria as salario_semanal
	from funcionario);
	select * from salario_semanal_funcionario;

	create view dados_do_cliente as
	(select fk_pessoa_codigo as codigo, pessoa.nome, contato
	from cliente
	inner join pessoa
	on(cliente.fk_pessoa_codigo = pessoa.codigo)
	inner join forma_contato
	on(cliente.fk_forma_contato_codigo = forma_contato.codigo));
	select * from dados_do_cliente;

	create view funcionario_fez_pedido as
	(select pedido.codigo as codigo_pedido, 
	funcionario.fk_pessoa_codigo as codigo_funcionario, 
	pessoa.nome as nome_funcionario
	from pedido
	inner join funcionario
	on(pedido.fk_pessoa_funcionario_codigo = funcionario.fk_pessoa_codigo)
	inner join pessoa
	on(funcionario.fk_pessoa_codigo = pessoa.codigo));
	select * from funcionario_fez_pedido;

	create view tamanho_nome_dos_pedidos as 
	(select acai_pedido.fk_pedido_codigo as codigo_pedido, acai.tamanho, acai.nome
	from acai_pedido
	inner join acai
	on(acai_pedido.fk_acai_codigo = acai.codigo));
	select * from tamanho_nome_dos_pedidos;

	create view codigoPedido_nomeCliente as
	(select pedido.codigo, pessoa.nome
	from pedido
	inner join pessoa
	on(pedido.fk_pessoa_cliente_codigo = pessoa.codigo));
	select * from codigoPedido_nomeCliente;

	create view qtd_pedidos_por_cliente as
	(select fk_pessoa_cliente_codigo as codigo_cliente, 
	sum(qtd_acai) qtd_total_pedidos
	from pedido
	group by(codigo_cliente));
	select * from qtd_pedidos_por_cliente;


#### 9.10	SUBCONSULTAS (Mínimo 4)<br>
a) Criar minimo 1 envolvendo GROUP BY
b) Criar minimo 1 envolvendo algum tipo de junção

	select codigo, tamanho, nome from acai where tamanho
	in ( select tamanho from acai where tamanho<>'500ml'
	group by tamanho)
	
	SELECT F.fk_pessoa_codigo as codigo_funcionario, AVG(diaria*qtd_dia) as media_salarial
	FROM funcionario F
	INNER JOIN
	pedido P
	ON (F.fk_pessoa_codigo=P.fk_pessoa_funcionario_codigo)
	WHERE F.fk_pessoa_codigo IN (
	 select distinct fk_pessoa_funcionario_codigo
	 from pedido
	 )
	GROUP BY codigo_funcionario;

	SELECT C.cpf as cpf_cliente, AVG(qtd_acai * valor_uni) as media_valor
	FROM cliente C
	INNER JOIN
	pedido P
	ON (C.fk_pessoa_codigo = P.fk_pessoa_cliente_codigo)
	WHERE C.fk_pessoa_codigo IN (
	 select distinct fk_pessoa_cliente_codigo
	 from pedido
	 )
	GROUP BY cpf_cliente;

	SELECT F.forma_pagamento, count(fk_pagamento_codigo) as qtd
	FROM pagamento F
	INNER JOIN
	pedido P
	ON (F.codigo = P.fk_pagamento_codigo)
	WHERE F.codigo IN (
	 select distinct fk_pagamento_codigo
	 from pedido
	 )
	GROUP BY F.forma_pagamento;


># Marco de Entrega 02: Do item 9.2 até o ítem 9.10<br>

### 10 RELATÓRIOS E GRÁFICOS (Usar template disponibilizado)
[Template de relatórios](https://github.com/discipbdint/public_samples/blob/main/BD_Exemplo_Relatorios_Empresa_VA.ipynb "Template relatórios")

#### a) análises e resultados provenientes do banco de dados desenvolvido (usar modelo disponível)
#### b) link com exemplo de relatórios será disponiblizado pelo professor no AVA
#### OBS: Esta é uma atividade de grande relevância no contexto do trabalho. Mantenha o foco nos 5 principais relatórios/resultados visando obter o melhor resultado possível.

    

### 11	AJUSTES DA DOCUMENTAÇÃO, CRIAÇÃO DOS SLIDES E VÍDEO PARA APRESENTAÇAO FINAL <br>

#### a) Modelo (pecha kucha)<br>
#### b) Tempo de apresentação 6:40 

># Marco de Entrega 03: Itens 10 e 11<br>
<br>
<br>
<br> 



### 12 FORMATACAO NO GIT:<br> 
https://help.github.com/articles/basic-writing-and-formatting-syntax/
<comentario no git>
    
##### About Formatting
    https://help.github.com/articles/about-writing-and-formatting-on-github/
    
##### Basic Formatting in Git
    
    https://help.github.com/articles/basic-writing-and-formatting-syntax/#referencing-issues-and-pull-requests
    
    
##### Working with advanced formatting
    https://help.github.com/articles/working-with-advanced-formatting/
#### Mastering Markdown
    https://guides.github.com/features/mastering-markdown/

    
### OBSERVAÇÕES IMPORTANTES

#### Todos os arquivos que fazem parte do projeto (Imagens, pdfs, arquivos fonte, etc..), devem estar presentes no GIT. Os arquivos do projeto vigente não devem ser armazenados em quaisquer outras plataformas.
1. <strong>Caso existam arquivos com conteúdos sigilosos<strong>, comunicar o professor que definirá em conjunto com o grupo a melhor forma de armazenamento do arquivo.

#### Todos os grupos deverão fazer Fork deste repositório e dar permissões administrativas ao usuário do git "profmoisesomena", para acompanhamento do trabalho.

#### Os usuários criados no GIT devem possuir o nome de identificação do aluno (não serão aceitos nomes como Eu123, meuprojeto, pro456, etc). Em caso de dúvida comunicar o professor.


Link para BrModelo:<br>
http://www.sis4.com/brModelo/download.html
<br>


Link para curso de GIT<br>
![https://www.youtube.com/curso_git](https://www.youtube.com/playlist?list=PLo7sFyCeiGUdIyEmHdfbuD2eR4XPDqnN2?raw=true "Title")



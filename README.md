# TRABALHO 01:  Açaifes
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

> A empresa "ACAIFES" visa colaborar com prestador de serviço na distribuição de açaí para o instituto federal do espiríto		Santo,tendo em vista que o local não tem acesso há muitos comércios e que certamente será sucesso, o propretário deseja que 		desde o início de seu negócio tenha total controle de vendas e entradas para que assim tenha maior controle no estoque e em nenhuma hipótese falte matéria prima e etc,visando também ser um ambiente acadêmico é necessário horários estratégicos. Para que as aplicações sejam feitas adequadamente é necessário um sistema com o cadastro do cliente pois assim pode ser feito o controle dos mesmos,já do produto será armazenado código,valor,tamanho e complementos ;outra forma de conseguir saber quais 	produtos<br> e tamanhos são mais vendidos ou não.Nesta aplicação manteremos também informações do funcionário ao proprietário,vizamos essa informação importante pois uma vez que haja erros na entrega do produto será possível que saiba o responsável e assim corrigí-las de<br> maneira mais direta e controle também da data de contratação e etc deste pois entendemos que é muito mais provável alcançar o<br> sucesso se houver uma equipe unida e organizada.<br>
-------- Nossa motivação é a união da equipe pois acreditamos que é o que faz o trabalho alcançar o sucesso -------- 

 

### 3.MINI-MUNDO<br>

>  No sistema desenvolvido para melhor controle do delivery de sua açaiteria "Açaifes" o dono deseja armazenar informações sobre sua loja e todo o funcionamento.
Nesse sistema será necessário armazenar as informações de cada cliente, que possuirá nome, cpf e telefone. Além disso, será armazenado as informações sobre cada pedido realizado pelo cliente, sendo elas código, valor unitário, quantidade e data_hora. O pedido possuirá também as informações acerca de outras entidades, ou seja as chaves estrangeiras, sendo elas: tamanho do produto, complemento, fruta, calda, forma de pagamento e endereço daquele pedido. Um cliente poderá fazer vários ou nenhum pedido e um pedido poderá ser feito somente por um cliente. Para melhor supervisão, será armazenado nesse sistema as informações de cada atendente que realiza os pedidos, ele possuirá nome, código, quantidade de dias que ele trabalha semanalmente, e o valor da diária recebida. Um atendente realiza vários ou nenhum pedido e o pedido é realizado por apenas um atendente.
Também será armazenado as informações de cada motoboy que entrega os pedidos, ele possuirá nome, código, quantidade de dias que ele trabalha semanalmente, e o valor da diária recebida. Além disso, o motoboy receberá o valor integral das taxas de cada entrega realizada por ele, a taxa será declarada de acordo com o bairro da entrega. Um motoboy entrega vários ou nenhum pedido e o pedido é entregue por apenas um motoboy.



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
![image](https://user-images.githubusercontent.com/109684951/198835905-aff59955-46de-4daa-bcd9-adfa2fe1341c.png)

### 7	MODELO FÍSICO<br>

	drop table if exists FORMA_CONTATO,ENDERECO,ACAI,PAGAMENTO,PEDIDO,PESSOA,ACAI_PEDIDO,PESSOA_PEDIDO;

	CREATE TABLE FORMA_CONTATO (
	    codigo INTEGER PRIMARY KEY,
	    nome VARCHAR(255),
	    contato VARCHAR(40)
	);

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

	CREATE TABLE ACAI (
	    codigo INTEGER PRIMARY KEY,
	    tamanho VARCHAR(25),
	    nome VARCHAR(25),
	    descricao VARCHAR(255)
	);

	CREATE TABLE PAGAMENTO (
	    codigo INTEGER PRIMARY KEY,
	    forma_pagamento VARCHAR(25)
	);

	CREATE TABLE PESSOA (
	    codigo INTEGER PRIMARY KEY,
	    nome VARCHAR(255)
	);

	CREATE TABLE CLIENTE(
	cpf varchar(25),
	FK_PESSOA_codigo INTEGER,
	FK_FORMA_CONTATO_codigo INTEGER,
	FOREIGN KEY (FK_PESSOA_codigo)
	    REFERENCES PESSOA (codigo),
	FOREIGN KEY (FK_FORMA_CONTATO_codigo)
	    REFERENCES FORMA_CONTATO (codigo)
	);

	CREATE TABLE FUNCIONARIO(
	qtd_dia integer,
	diaria float,
	FK_PESSOA_codigo INTEGER,
	FOREIGN KEY (FK_PESSOA_codigo)
	    REFERENCES PESSOA (codigo)
	);

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

	CREATE TABLE ACAI_PEDIDO (
	    fk_ACAI_codigo INTEGER,
	    fk_PEDIDO_codigo INTEGER,
	FOREIGN KEY (fk_ACAI_codigo)
	    REFERENCES ACAI (codigo),
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
	(10,'Telefone','(27) 2785-4410'),
	(11, 'E-mail', '(27) 2756-8864');

	select * from forma_contato;

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

	select * from endereco;

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

	select * from acai;

	insert into pagamento (codigo, forma_pagamento)
	values(61, 'cartão'),
	(62, 'dinheiro'),
	(63, 'pix'),
	(64, 'Pic Pay');

	select * from pagamento;

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

	select * from pessoa;

	insert into cliente(cpf, FK_PESSOA_codigo, FK_FORMA_CONTATO_codigo)
	values('333.752.060-03', 001, 1),
	('232.275.170-78', 006, 6),
	('820.944.040-30', 008, 8),
	('182.691.910-43', 010, 10),
	('994.981.150-36', 005, 7);

	select * from cliente;
	insert into funcionario(qtd_dia, diaria, FK_PESSOA_codigo)
	values(4, 80.00, 002),
	(6, 75.00, 003),
	(3, 20.00, 004),
	(7, 40.00, 007),
	(3, 35.00, 009);

	select * from funcionario;

	insert into pedido(codigo, valor_uni, qtd_acai, data_hora, FK_ENDERECO_codigo, FK_PAGAMENTO_codigo, FK_PESSOA_cliente_codigo, FK_PESSOA_funcionario_codigo)
	values(150, 15.00, 2, '2022-06-03 07:04:21', 50, 62, 1, 2),
	(152, 20.00, 1, '2022-04-01 01:07:22', 51, 61, 6, 2),
	(153,  18.00,5,'2022-06-07 07:06:01', 56, 62, 1, 5),
	(154, 23.00, 4,'2022-04-12 03:05:03', 58, 64, 1, 2),
	(155, 13.00,3,'2022-03-03 09:08:21', 52, 61, 1, 2),
	(156, 15.00,5,'2022-12-05 04:01:12', 53, 61, 1, 3),
	(157, 18.00,6, '2022-11-12 05:08:04', 55, 61, 8, 2),
	(158, 23.00,8,'2022-10-04 03:05:06', 55, 63, 10, 2),
	(159, 13.00,5,'2022-03-02 15:02:07', 55, 64, 6, 2),
	(160, 15.00,3,'2022-09-22 04:45:32', 58, 62, 1, 3),
	(161, 13.00,1,'2022-06-03 07:04:21', 53, 62, 8, 3),
	(162, 15.00,3,'2022-04-01 01:07:22', 54, 62, 8, 4),
	(163, 18.00,5,'2022-06-07 07:06:01', 55, 62, 8, 9),
	(164, 23.00,8,'2022-04-12 03:05:03', 55, 62, 6, 9),
	(165, 13.00,2,'2022-03-03 09:08:21', 55, 61, 10, 2),
	(166, 15.00,9,'2022-12-05 04:01:12', 57, 64, 10, 2),
	(167, 18.00,1,'2022-11-12 05:08:04', 57, 64, 10, 9),
	(168, 23.00,5,'2022-10-04 03:05:06', 57, 64, 6, 9),
	(169, 13.00,1,'2022-03-02 15:02:07', 57, 61, 6, 9);

	select * from pedido;

	insert into acai_pedido (fk_ACAI_codigo, fk_PEDIDO_codigo)
	values(10, 150),
	(20, 152),
	(30, 154),
	(50, 155),
	(90, 167),
	(50, 160),
	(40, 169);


### 9	TABELAS E PRINCIPAIS CONSULTAS<br>
> LINK DO COLAB:
	https://colab.research.google.com/drive/192W38yKOnMiJ8yQZ29hHF_u2P2n2EteT?usp=sharing <br>
	
># Marco de Entrega 01: Do item 1 até o item 9.1<br>

#### 9.2	CONSULTAS DAS TABELAS COM FILTROS WHERE (Mínimo 4)<br>
#### 9.3	CONSULTAS QUE USAM OPERADORES LÓGICOS, ARITMÉTICOS E TABELAS OU CAMPOS RENOMEADOS (Mínimo 11)
    a) Criar 5 consultas que envolvam os operadores lógicos AND, OR e Not
    b) Criar no mínimo 3 consultas com operadores aritméticos 
    c) Criar no mínimo 3 consultas com operação de renomear nomes de campos ou tabelas

#### 9.4	CONSULTAS QUE USAM OPERADORES LIKE E DATAS (Mínimo 12) <br>
    a) Criar outras 5 consultas que envolvam like ou ilike
    b) Criar uma consulta para cada tipo de função data apresentada.

#### 9.5	INSTRUÇÕES APLICANDO ATUALIZAÇÃO E EXCLUSÃO DE DADOS (Mínimo 6)<br>
    a) Criar minimo 3 de exclusão
    b) Criar minimo 3 de atualização

#### 9.6	CONSULTAS COM INNER JOIN E ORDER BY (Mínimo 6)<br>
    a) Uma junção que envolva todas as tabelas possuindo no mínimo 2 registros no resultado
    b) Outras junções que o grupo considere como sendo as de principal importância para o trabalho

#### 9.7	CONSULTAS COM GROUP BY E FUNÇÕES DE AGRUPAMENTO (Mínimo 6)<br>
    a) Criar minimo 2 envolvendo algum tipo de junção

#### 9.8	CONSULTAS COM LEFT, RIGHT E FULL JOIN (Mínimo 4)<br>
    a) Criar minimo 1 de cada tipo

#### 9.9	CONSULTAS COM SELF JOIN E VIEW (Mínimo 6)<br>
        a) Uma junção que envolva Self Join (caso não ocorra na base justificar e substituir por uma view)
        b) Outras junções com views que o grupo considere como sendo de relevante importância para o trabalho

#### 9.10	SUBCONSULTAS (Mínimo 4)<br>
     a) Criar minimo 1 envolvendo GROUP BY
     b) Criar minimo 1 envolvendo algum tipo de junção

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



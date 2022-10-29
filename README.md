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

> A empresa "ACAIFES" visa colaborar com prestador de serviço na distribuição de açaí para o instituto federal do espiríto		Santo,tendo em vista que o local não tem acesso há muitos comércios e que certamente será sucesso, o propretário deseja que 		desde o início de seu negócio tenha total controle de vendas e entradas para que assim tenha maior controle no estoque e em nenhuma hipótese falte matéria prima e etc,visando também ser um ambiente acadêmico é necessário horários estratégicos. Para que as aplicações sejam feitas adequadamente é necessário um sistema com o cadastro do cliente pois assim pode ser feito o controle dos mesmos,já do produto será armazenado código,valor,tamanho e complementos ;outra forma de conseguir saber quais 	produtos<br> e tamanhos são mais vendidos ou não.Nesta aplicação manteremos também informações do funcionário ao proprietário,vizamos essa informação importante pois uma vez que haja erros na entrega do produto será possível que saiba o responsável e assim corrigí-las de<br> maneira mais direta e controle também da data de contratação e etc deste pois entendemos que é muito mais provável alcançar o<br> sucesso se houver uma equipe unida e organizada.

--------Nossa motivação é a união da equipe pois acreditamos que é o que faz o trabalho alcançar o sucesso-----(frase motivacional necessária para que o empresário insira aos funcionários um controle de modo que os mesmos aceitem como algo bom e não como uma vigilancia constante e assim o cumpram com mais amor )----------

 

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

* Relatório que traga o código de todos os pedidos realizados por cada funcionário e o código do cliente responsável por esse 		pedido.<br>

* Relatório que mostre o valor total em taxas de entrega realizado por cada motoboy.<br>

 * Relatório com a quantidade de pedidos por cada tamanho do produto, para obter uma relação de demanda.<br>

 * Relatório de obtenha a quantidade de pedidos por bairro, quantidade de pedidos realizados para cada tamanho de acaí e a 		quantidade de pedidos por cada forma de pagamento. 



 > informe quais são as 3 principais entidades do sistema em densenvolvimento<br>(se houverem mais de 3 entidades, pense na importância da entidade para o sistema)   
 
* Cliente
* Pedido
* Produto

 ### 5 MODELO CONCEITUAL
 ![image](https://user-images.githubusercontent.com/109684951/198835219-9eb528e4-cd67-45ca-ae6b-1e9e501b2154.png)

        
    
#### 5.1 Validação do Modelo Conceitual
> GRUPO 1: Camila,yasmim,Isabellay e Davi nunes<br> GRUPO 2: Eduardo, Paulo Cezar, Nycooly e Elisa<br>

#### 5.2 Descrição dos dados 
* CLIENTE: Tabela que armazena as informações relativas ao cliente<br> 
* TELEFONE: Tabela que armazena o número de telefone de cada cliente e cada número tem um código<br> 
* PEDIDO: Tabela que armazena todas as informações de cada pedido feito por um cliente<br>
* ATENDENTE: Tabela que armazena as informações referida a cada atendente que monta o produto<br>
* MOTOBOY: Tabela que armazena as informações de cada motoboy que entrega o pedido<br>
* ENDERECO: Tabela referente ao endereço de cada Cliente<br>
* BAIRRO: Tabela que armazena o valor referente ao Bairro de cada Cliente<br>
* ESTADO: Tabela que armazena o valor referente ao Estado de cada Cliente<br>
* TIPO_LOGRADOURO: Tabela que armazena o tipo logradouro relacionado a cada Cliente<br>
* CIDADE: Tabela que armazena a cidade relacionada a cada cliente<br>
* PAGAMENTO: Tabela que armazena a forma de pagamento que cada cliente optou<br>
* PRODUTO: Tabela referente ao produto que foi escolhido por cada cliente<br>
* COMPLEMENTO: Tabela referente ao complemento do pedido de cada cliente<br>
* FRUTA: Tabela referente a opção da fruta do pedido de cada cliente<br>
* CALDA: Tabela referente a opção da calda do pedido de cada cliente<br>
* PEDIDO_PRODUTO: Relacionamento referente ao pedido e o produto escolhido no pedido por cada cliente<br>

### 6	MODELO LÓGICO
![image](https://user-images.githubusercontent.com/109684951/198835905-aff59955-46de-4daa-bcd9-adfa2fe1341c.png)

### 7	MODELO FÍSICO<br>

	
	DROP TABLE TELEFONE, CLIENTE, ATENDENTE, MOTOBOY, TIPO_LOGRADOURO,BAIRRO,CIDADE,ESTADO,ENDERECO,PAGAMENTO,CALDA,FRUTA,COMPLEMENTO,PEDIDO,PRODUTO,PEDIDO_PRODUTO;

	DROP TABLE IF EXISTS TELEFONE;
	CREATE TABLE TELEFONE(
	codigo INTEGER PRIMARY KEY,
	numero VARCHAR(25)
	);

	DROP TABLE IF EXISTS CLIENTE;
	CREATE TABLE CLIENTE (
	nome VARCHAR(255),
	cpf VARCHAR(25) PRIMARY KEY,
	FK_TELEFONE_codigo INTEGER,
	FOREIGN KEY (FK_TELEFONE_codigo)
	REFERENCES TELEFONE (codigo)
	);

	DROP TABLE IF EXISTS ATENDENTE;
	CREATE TABLE ATENDENTE (
	nome VARCHAR(255),
	codigo INTEGER PRIMARY KEY,
	diaria FLOAT,
	qtd_dia INTEGER
	);

	DROP TABLE IF EXISTS MOTOBOY;
	CREATE TABLE MOTOBOY (
	codigo INTEGER PRIMARY KEY,
	nome VARCHAR(255),
	diaria FLOAT,
	qtd_dia INTEGER
	);

	DROP TABLE IF EXISTS TIPO_LOGRADOURO;
	CREATE TABLE TIPO_LOGRADOURO (
	codigo INTEGER PRIMARY KEY,
	nome VARCHAR(255)
	);

	DROP TABLE IF EXISTS BAIRRO;
	CREATE TABLE BAIRRO (
	codigo INTEGER PRIMARY KEY,
	nome VARCHAR(255),
	taxa_entrega FLOAT
	);

	DROP TABLE IF EXISTS CIDADE;
	CREATE TABLE CIDADE (
	codigo INTEGER PRIMARY KEY,
	nome VARCHAR(255)
	);

	DROP TABLE IF EXISTS ESTADO;
	CREATE TABLE ESTADO (
	codigo INTEGER PRIMARY KEY,
	nome VARCHAR(255)
	);

	DROP TABLE IF EXISTS ENDERECO;
	CREATE TABLE ENDERECO (
	cep VARCHAR(25),
	nome_logradouro VARCHAR(255),
	numero INTEGER,
	codigo INTEGER PRIMARY KEY,
	FK_TIPO_LOGRADOURO_codigo INTEGER,
	FK_BAIRRO_codigo INTEGER,
	FK_CIDADE_codigo INTEGER,
	FK_ESTADO_codigo INTEGER,
	FOREIGN KEY (FK_TIPO_LOGRADOURO_codigo)
	REFERENCES TIPO_LOGRADOURO (codigo),
	FOREIGN KEY (FK_BAIRRO_codigo)
	REFERENCES BAIRRO (codigo),
	FOREIGN KEY (FK_CIDADE_codigo)
	REFERENCES CIDADE (codigo),
	FOREIGN KEY (FK_ESTADO_codigo)
	REFERENCES ESTADO (codigo)
	);

	DROP TABLE IF EXISTS PAGAMENTO;
	CREATE TABLE PAGAMENTO (
	codigo INTEGER PRIMARY KEY,
	forma_pagamento VARCHAR(255)
	);

	DROP TABLE IF EXISTS CALDA;
	CREATE TABLE CALDA (
	codigo INTEGER PRIMARY KEY,
	nome VARCHAR(255)
	);

	DROP TABLE IF EXISTS FRUTA;
	CREATE TABLE FRUTA (
	codigo INTEGER PRIMARY KEY,
	nome VARCHAR(255)
	);

	DROP TABLE IF EXISTS COMPLEMENTO;
	CREATE TABLE COMPLEMENTO (
	codigo INTEGER PRIMARY KEY,
	nome VARCHAR(255)
	);


	DROP TABLE IF EXISTS PEDIDO;
	CREATE TABLE PEDIDO (
	codigo INTEGER PRIMARY KEY,
	data_hora TIMESTAMP,
	valor_uni FLOAT,
	qtd_produto INTEGER,
	FK_CLIENTE_cpf VARCHAR(25),
	FK_ATENDENTE_codigo INTEGER,
	FK_ENDERECO_codigo INTEGER,
	FK_MOTOBOY_codigo INTEGER,
	FK_PAGAMENTO_codigo INTEGER,
	FK_CALDA_codigo INTEGER,
	FK_FRUTA_codigo INTEGER, 
	FK_COMPLEMENTO_codigo INTEGER,
	FOREIGN KEY (FK_CLIENTE_cpf)
	REFERENCES CLIENTE (cpf),
	FOREIGN KEY (FK_ATENDENTE_codigo)
	REFERENCES ATENDENTE (codigo),
	FOREIGN KEY (FK_ENDERECO_codigo)
	REFERENCES ENDERECO (codigo),
	FOREIGN KEY (FK_MOTOBOY_codigo)
	REFERENCES MOTOBOY (codigo),
	FOREIGN KEY (FK_PAGAMENTO_codigo)
	REFERENCES PAGAMENTO (codigo),
	FOREIGN KEY (FK_CALDA_codigo)
	REFERENCES CALDA (codigo),
	FOREIGN KEY (FK_FRUTA_codigo)
	REFERENCES FRUTA (codigo),
	FOREIGN KEY (FK_COMPLEMENTO_codigo)
	REFERENCES COMPLEMENTO (codigo)
	);


	DROP TABLE IF EXISTS PRODUTO;
	CREATE TABLE PRODUTO (
	codigo INTEGER PRIMARY KEY,
	tamanho VARCHAR(25)
	);

	DROP TABLE IF EXISTS PEDIDO_PRODUTO;
	CREATE TABLE PEDIDO_PRODUTO (
	fk_PRODUTO_codigo INTEGER,
	fk_PEDIDO_codigo INTEGER,
	FOREIGN KEY (fk_PRODUTO_codigo)
	REFERENCES PRODUTO (codigo),
	FOREIGN KEY (fk_PEDIDO_codigo)
	REFERENCES PEDIDO (codigo)
	);


           
### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>
        
	insert into telefone(codigo, numero)
	values(1,'(27)3242-6439'),
	(2, '(27) 3419-5155'),
	(3, '(27) 2250-6347'),
	(4, '(27) 3769-9583'),
	(5, '(27) 3304-4261'),
	(6, '(27) 2332-2719'),
	(7, '(27) 3750-9836'),
	(8, '(27) 2725-2842'),
	(9, '(27) 2854-2690'),
	(10, '(27) 2785-4410');

	select * from telefone;

	insert into cliente(nome, cpf, FK_TELEFONE_codigo)
	values ('Gustavo', '230.149.108-05', 1),
	('Eduarda', '072.424.817-02', 2),
	('Maria', '019.082.980-06', 3),
	('Luiz', '024.325.400-01', 4),
	('Roberto', '513-245.701-03', 5),
	('Fernando', '234.167.398-84', 6),
	('Vitória', '009.449.081-36', 7),
	('Carlos', '529.982.247-26', 8),
	('Fábiana', '570.415.611-05', 9),
	('Marcos', '425.863.098-32', 10);

	select * from cliente;

	insert into atendente(nome, codigo, diaria, qtd_dia)
	values ('Henrique', 10, 50.00, 5),
	('Davi', 20, 60.00, 4),
	('Lorena', 30, 50.00, 6),
	('Sthephany', 40, 70.00, 5),
	('Valter', 50, 50.00, 3),
	('Valéria', 60, 60.00, 4);

	select * from atendente;

	insert into motoboy(codigo, nome, diaria, qtd_dia)
	values(70, 'Roberto', 50.00, 4),
	(80, 'Samuel', 50.00, 5),
	(90, 'Carlos', 50.00, 4),
	(100, 'Paulo', 50.00, 5);

	select * from motoboy;

	insert into tipo_logradouro(codigo, nome)
	values(11, 'Rua'),
	(12, 'Rodovia'),
	(13, 'Avenida'),
	(14, 'Residencial');

	select * from tipo_logradouro;

	insert into bairro(codigo, nome, taxa_entrega)
	values(31, 'São Pedro', 10.00),
	(32, 'Grande Vitória', 8.00),
	(33, 'Jacaraípe', 5.00),
	(34, 'São Francisco', 6.00),
	(35, 'Morada de Laranjeiras', 4.00),
	(36, 'Jardim Limoeiro', 7.00);

	select * from bairro;

	insert into cidade(codigo, nome)
	values(21, 'Vitória'),
	(22, 'Serra');

	select * from cidade;

	insert into estado(codigo, nome)
	values(23, 'Espírito Santo');

	select * from estado;

	insert into endereco (cep, nome_logradouro, numero, codigo, FK_TIPO_LOGRADOURO_codigo, FK_BAIRRO_codigo, FK_CIDADE_codigo, FK_ESTADO_codigo)
	values ('29024-043', '21 de Novembro', 1110, 51, 11, 31, 21, 23),
	('29984-023', 'Serafim Derenze', 2213, 52, 12, 32,  21, 23),
	('29876-865', 'Abdo Saad', 5333, 53, 13, 33, 22, 23),
	('29446-048', 'Encanto das Ostras', 4921, 54, 14, 34, 22, 23),
	('29764-958', '22 de Novembro', 6235, 55, 11, 31, 21, 23),
	('29473-764', 'Das Jandaias', 1267, 56, 11, 35, 22, 23),
	('29745-140', 'dos Colibris', 354, 57, 13, 35, 22, 23),
	('29465-434', 'Vila Sol', 6077, 58, 14, 35, 22, 23),
	('29435-724', 'Atlântica', 56445, 59, 13, 35, 22, 23),
	('29862-867', 'Gardenia', 8788, 50, 11, 36, 22, 23);

	select * from endereco;

	insert into pagamento(codigo, forma_pagamento)
	values(61, 'cartão'),
	(62, 'dinheiro'),
	(63, 'pix'),
	(64, 'Pic Pay');

	select * from pagamento;

	insert into calda(codigo, nome)
	values (71, 'Leite Condensado'),
	(72, 'Caramelo'),
	(73, 'Mel'),
	(74, 'Chocolate'),
	(75, 'Menta'),
	(76, 'Doce de leite'),
	(77, 'Morango');

	select * from calda;

	insert into fruta(codigo, nome)
	values (81, 'Banana'),
	(82, 'Abacaxi'),
	(83, 'Kiwi'),
	(84, 'Manga'),
	(85, 'Morango');

	select * from fruta;

	insert into complemento(codigo, nome)
	values (91, 'Leite em pó'),
	(92, 'Paçoca'),
	(93, 'Amendoim'),
	(94, 'Shocobow'),
	(95, 'Sucrilhos'),
	(96, 'Ovomaltine'),
	(97, 'Granola'),
	(98, 'Disquete');

	select * from complemento;

	insert into pedido (codigo, data_hora, valor_uni, qtd_produto, FK_CLIENTE_cpf, FK_ATENDENTE_codigo, FK_ENDERECO_codigo, FK_MOTOBOY_codigo, FK_PAGAMENTO_codigo, FK_CALDA_codigo, FK_FRUTA_codigo, FK_COMPLEMENTO_codigo)
	values (151, '2022-06-03 07:04:21', 13.00, 5, '425.863.098-32', 10, 51, 70, 61, 71, 81, 91),
	(152, '2022-04-01 01:07:22', 15.00, 3, '570.415.611-05', 20, 52, 80, 62, 72, 82, 92),
	(153, '2022-06-07 07:06:01', 18.00, 3, '529.982.247-26', 30, 53, 90, 63, 73, 83, 93),
	(154, '2022-04-12 03:05:03', 23.00, 1, '009.449.081-36', 40, 54, 100, 64, 74, 84, 94),
	(155, '2022-03-03 09:08:21', 13.00, 4, '234.167.398-84', 50, 55, 70, 61, 75, 85, 95),
	(156, '2022-12-05 04:01:12', 15.00, 2, '513-245.701-03', 60, 56, 80, 62, 76, 81, 96),
	(157, '2022-11-12 05:08:04', 18.00, 5, '024.325.400-01', 10, 57, 90, 63, 77, 82, 97),
	(158, '2022-10-04 03:05:06', 23.00, 2, '019.082.980-06', 20, 58, 100, 64, 71, 83, 98),
	(159, '2022-03-02 15:02:07', 13.00, 7, '072.424.817-02', 30, 59, 70, 61, 72, 84, 91),
	(160, '2022-09-22 04:45:32', 15.00, 6, '230.149.108-05', 40, 50, 80, 62, 73, 85, 92),
	(161, '2022-06-03 07:04:21', 13.00, 5, '425.863.098-32', 10, 51, 70, 61, 74, 81, 93),
	(162, '2022-04-01 01:07:22', 15.00, 3, '570.415.611-05', 20, 52, 80, 62, 75, 82, 94),
	(163, '2022-06-07 07:06:01', 18.00, 3, '529.982.247-26', 30, 53, 90, 63, 76, 83, 95),
	(164, '2022-04-12 03:05:03', 23.00, 1, '009.449.081-36', 40, 54, 100, 64, 77, 84, 96),
	(165, '2022-03-03 09:08:21', 13.00, 4, '234.167.398-84', 50, 55, 70, 61, 71, 85, 97),
	(166, '2022-12-05 04:01:12', 15.00, 2, '513-245.701-03', 60, 56, 80, 62, 72, 81, 98),
	(167, '2022-11-12 05:08:04', 18.00, 5, '024.325.400-01', 10, 57, 90, 63, 73, 82, 91),
	(168, '2022-10-04 03:05:06', 23.00, 2, '019.082.980-06', 20, 58, 100, 64, 74, 83, 92),
	(169, '2022-03-02 15:02:07', 13.00, 7, '072.424.817-02', 30, 59, 70, 61, 75, 84, 93);

	select * from pedido;

	insert into produto(codigo, tamanho)
	values (001, '300ml'),
	(002, '500ml'),
	(003, '700ml'),
	(004, '1l');

	select * from produto;

	insert into pedido_produto(fk_PRODUTO_codigo, fk_PEDIDO_codigo)
	values(001, 151),
	(002, 151),
	(003, 152),
	(004, 152),
	(001, 153),
	(002, 154),
	(003, 155),
	(004, 155),
	(001, 155),
	(002, 156),
	(003, 157),
	(004, 158),
	(001, 159),
	(002, 160),
	(003, 161),
	(004, 162),
	(001, 162),
	(002, 163),
	(003, 164),
	(004, 164),
	(001, 165),
	(002, 165),
	(003, 165),
	(004, 166),
	(001, 167),
	(002, 168),
	(003, 169);

	select * from pedido_produto; 


### 9	TABELAS E PRINCIPAIS CONSULTAS<br>
	LINK DO COLAB: (https://colab.research.google.com/drive/1AhTAhI60FVkg8UhlZw7WZxFTq1wd2FuV?usp=sharing)
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



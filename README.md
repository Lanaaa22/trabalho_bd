# TRABALHO 01:  Açaifes
Trabalho desenvolvido durante a disciplina de Banco de dados

# Sumário

### 1. COMPONENTES<br>
Integrantes do grupo<br>
Ilanna dos Reis Cardoso cardosoilanna96@gmail.com<br>
Mariana Lopes marianalopesgovea@gmail.com<br>
Bruna Ramos Rocha brunaramosrocha72@gmail.com<br>
Daianny Maria dadaymaria1@hotmail.com<br>
...<br>

### 2.INTRODUÇÃO E MOTIVAÇÃO

>A empresa "ACAIFES" visa colaborar com prestador de serviço na distribuição de açaí para o instituto federal do espiríto Santo,tendo em vista que o local não tem acesso há muitos comércios e que certamente será sucesso, o propretário deseja que desde o início de seu negócio tenha total controle de vendas e entradas para que assim tenha maior controle no estoque e em nenhuma hipótese falte matéria prima e etc,visando também ser um ambiente acadêmico é necessário horários estratégicos. Para que as aplicações sejam feitas adequadamente é necessário um sistema com o cadastro do cliente pois assim pode er feito o controle dos mesmos,já do produto será armazenado código,valor,tamanho e complementos ;outra forma de conseguir saber quais produtos e tamanhos são mais vendidos ou não.Nesta aplicação manteremos também informações do funcionário ao proprietário,vizamos essa informação importante pois uma vez que haja erros na entrega do produto será possível que saiba o responsável e assim corrigí-las de maneira mais direta e controle também da data de contratação e etc deste pois entendemos que é muito mais provável alcançar o sucesso se houver uma equipe unida e organizada.
--------Nossa motivação é a união da equipe pois acreditamos que é o que faz o trabalho alcançar o sucesso-----(frase motivacional necessária para que o empresário insira aos funcionários um controle de modo que os mesmos aceitem como algo bom e não como uma vigilancia constante e assim o cumpram com mais amor )----------
 
 

### 3.MINI-MUNDO<br>

	Em uma açaiteria chamada "Açaifes" o dono deseja criar um sistema para melhor controle de seu delivery. Nesse sistema cada 		cliente possuirá um cadastro, para isso será armazenado as informações do cliente de nome e cpf. Do cadastro será armazenado as 	informações de codigo, telefone e endereço. Um cliente possui deve possuir um único cadastro e o cadastro pertencer a somente um 	 cliente. Além disso, será armazenado as informações sobre cada pedido relizado pelo cliente, sendo elas código, valor unitario de 	   cada produto, quantidade de cada produto, complementos, frutas e calda. Um cliente poderá comprar vários ou nehnum produto e um 	   produto poderá ser vendido para vários ou nenhum cliente. Um produduto possui código e tamanho, sendo que cada pedido possui um           ou vários produtos e cada produto pertence a vários ou nenhum pedido. Para melhor supervisão, será armazenado nesse sistema as 	    informações de cada  funcionário, ele possuirá nome, código, salário, data de contratação. Um funcioário realiza vários pedidos 	    ou nenhum pedido e o pedido é realizado por apenas um funcionário.


### 4.PERGUNTAS A SEREM RESPONDIDAS E TABELA DE DADOS<br>
#### 4.1 QUAIS PERGUNTAS PODEM SER RESPONDIDAS COM O SISTEMA PROPOSTO?
    a) O sistema proposto poderá fornecer quais tipos de relatórios e informações? 
    b) Crie uma lista com os 5 principais relatórios que poderão ser obtidos por meio do sistema proposto!
    
> A Açaiteria "Açaifes" precisa inicialmente dos seguintes relatórios:

     	* Relatório que mostre o valor total do pedido de cada cliente. (informação útil p/ o cliente e o açaí)<br>
 
 	* Relatório que traga o código de todos os pedidos realizados por cada funcionário e o código do cliente responsável por esse 		pedido.(útil p/ o dono do açaí caso ocorra erros nos pedidos)<br>
 
 	* Relatório que mostre para cada cliente as informações sobre seu pedido, sendo elas o tamanho, complemento, calda, fruta, 		quantidade e data_hora que realizou o pedido. (útil p/ o funcionário que realizará o pedido)<br>
 
	 * Relatório com os dados de cada cliente sobre: endereço e telefone (útil p/ o motoboy)<br>
 
	 * Relatório de obtenha a quantidade de pedidos por bairro, quantidade de pedidos realizados para cada tamanho de acaí e a 		quantidade de pedidos por cada forma de pagamento. (útil p/ controle do dono sobre o pedido)



 > informe quais são as 3 principais entidades do sistema em densenvolvimento<br>(se houverem mais de 3 entidades, pense na importância da entidade para o sistema)   
 
 	* Cliente
 	* Pedido
 	* Produto
    
 5. MODELO CONCEITUAL
    * informe quais são as 3 principais entidades do sistema em densenvolvimento<br>(se houverem mais de 3 entidades, pense na importância da entidade para o sistema)       
C) Principais fluxos de informação/entidades do sistema (mínimo 3). <br>Dica: normalmente estes fluxos estão associados as tabelas que conterão maior quantidade de dados 
D) Qualidade e Clareza
    Garantir que a semântica dos atributos seja clara no esquema (nomes coerentes com os dados).
    Criar o esquema de forma a garantir a redução de informação redundante, possibilidade de valores null, 
    e tuplas falsas (Aplicar os conceitos de normalização abordados).
        
    
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
    * COMPLEMENTO: Tabela referente aos complementos de cada produto de cada cliente<br>
    * FRUTA: Tabela referente a opção da fruta de cada produto de cada cliente<br>
    * CALDA: Tabela referente a opção da calda de cada produto de cada cliente<br>
    * PRODUTO_COMPLEMENTO: Relacionamento referente ao complemento e ao produto<br>
    * PRODUTO_FRUTA: Relacionamento referente ao produto e a escolha da fruta<br>
    * PRODUTO_CALDA: Relacionamento referente ao produto e a escolha da calda<br>
    * PEDIDO_PRODUTO: Relacionamento referente ao pedido e o produto escolhido no pedido por cada cliente<br>

### 6	MODELO LÓGICO
![image](https://user-images.githubusercontent.com/109684951/198706413-d59ead9d-5406-4c24-b6bc-ed5f56978403.png)

        a) inclusão do esquema lógico do banco de dados
        b) verificação de correspondencia com o modelo conceitual 
        (não serão aceitos modelos que não estejam em conformidade)

### 7	MODELO FÍSICO<br>

	DROP TABLE IF EXISTS TELEFONE;<br>
	CREATE TABLE TELEFONE (<br>
        	codigo INTEGER PRIMARY KEY,<br>
    		numero VARCHAR(25)<br>
	);<br>
	<br>
	DROP TABLE IF EXISTS CLIENTE;<br>
	CREATE TABLE CLIENTE (<br>
    		nome VARCHAR(255),<br>
    		cpf VARCHAR(25) PRIMARY KEY,<br>
    		FK_TELEFONE_codigo INTEGER,<br>
		FOREIGN KEY (FK_TELEFONE_codigo)<br>
	    	REFERENCES TELEFONE (codigo)<br>
	);<br>
	<br>
	DROP TABLE IF EXISTS ATENDENTE;<br>
	CREATE TABLE ATENDENTE (<br>
    		nome VARCHAR(255),<br>
    		codigo INTEGER PRIMARY KEY,<br>
    		diaria FLOAT,<br>
    		qtd_dia INTEGER<br>
	);<br>
	<br>
	DROP TABLE IF EXISTS MOTOBOY;<br>
	CREATE TABLE MOTOBOY (<br<
    		codigo INTEGER PRIMARY KEY,<br>
    		nome VARCHAR(255),<br>
    		diaria FLOAT,<br>
    		qtd_dia INTEGER<br>
	);<br>
	<br>
	DROP TABLE IF EXISTS TIPO_LOGRADOURO;<br>
	CREATE TABLE TIPO_LOGRADOURO (<br>
    		codigo INTEGER PRIMARY KEY,<br>
    		nome VARCHAR(255)<br>
	);<br>
	<br>
	DROP TABLE IF EXISTS BAIRRO;<br>
	CREATE TABLE BAIRRO (<br>
    		codigo INTEGER PRIMARY KEY,<br>
    		nome VARCHAR(255),<br>
    		taxa_entrega FLOAT<br>
	);<br>
	<br>
	DROP TABLE IF EXISTS CIDADE;<br>
	CREATE TABLE CIDADE (<br>
	    codigo INTEGER PRIMARY KEY,<br>
	    nome VARCHAR(255)<br>
	);<br>
	<br>
	DROP TABLE IF EXISTS ESTADO;<br>
	CREATE TABLE ESTADO (<br>
	    codigo INTEGER PRIMARY KEY,<br>
	    nome VARCHAR(255)<br>
	);<br>

	DROP TABLE IF EXISTS ENDERECO;<br>
	CREATE TABLE ENDERECO (<br>
	    cep VARCHAR(25),<br>
	    nome_logradouro VARCHAR(255),<br>
	    numero INTEGER,<br>
	    codigo INTEGER PRIMARY KEY,<br>
	    FK_TIPO_LOGRADOURO_codigo INTEGER,<br>
	    FK_BAIRRO_codigo INTEGER,<br>
	    FK_CIDADE_codigo INTEGER,<br>
	    FK_ESTADO_codigo INTEGER,<br>
	    <br>
		FOREIGN KEY (FK_TIPO_LOGRADOURO_codigo)<br>
	    REFERENCES TIPO_LOGRADOURO (codigo),<br>
		FOREIGN KEY (FK_BAIRRO_codigo)<br>
	    REFERENCES BAIRRO (codigo),<br>
		FOREIGN KEY (FK_CIDADE_codigo)<br>
	    REFERENCES CIDADE (codigo),<br>
		FOREIGN KEY (FK_ESTADO_codigo)<br>
	    REFERENCES ESTADO (codigo)<br>
	);<br>
	<br>
	DROP TABLE IF EXISTS PAGAMENTO;<br>
	CREATE TABLE PAGAMENTO (<br>
	<br>
	    codigo INTEGER PRIMARY KEY,<br>
	    forma_pagamento VARCHAR(255)<br>
	);<br>
	<br>
	DROP TABLE IF EXISTS PEDIDO;<br>
	CREATE TABLE PEDIDO (<br>
	    codigo INTEGER PRIMARY KEY,<br>
	    data_hora TIMESTAMP,<br>
	    valor_uni FLOAT,<br>
	    qtd_produto INTEGER,<br>
	    FK_CLIENTE_cpf VARCHAR(25),<br>
	    FK_ATENDENTE_codigo INTEGER,<br>
	    FK_ENDERECO_codigo INTEGER,<br>
	    FK_MOTOBOY_codigo INTEGER,<br>
	    FK_PAGAMENTO_codigo INTEGER,<br>
		FOREIGN KEY (FK_CLIENTE_cpf)<br>
	    REFERENCES CLIENTE (cpf),<br>
	    <br>
		FOREIGN KEY (FK_ATENDENTE_codigo)<br>
	    REFERENCES ATENDENTE (codigo),<br>
		FOREIGN KEY (FK_ENDERECO_codigo)<br>
	    REFERENCES ENDERECO (codigo),<br>
		FOREIGN KEY (FK_MOTOBOY_codigo)<br>
	    REFERENCES MOTOBOY (codigo),<br>
		FOREIGN KEY (FK_PAGAMENTO_codigo)<br>
	    REFERENCES PAGAMENTO (codigo)<br>
	);<br>
	<br>
	DROP TABLE IF EXISTS PRODUTO;<br>
	CREATE TABLE PRODUTO (<br>
	    codigo INTEGER PRIMARY KEY,<br>
	    tamanho VARCHAR(25),<br>
	    FK_CALDA_codigo INTEGER<br>
	);<br>
	<br>
	DROP TABLE IF EXISTS CALDA;<br>
	CREATE TABLE CALDA (<br>
	    codigo INTEGER PRIMARY KEY,<br>
	    nome VARCHAR(255)<br>
	);<br>
	<br>
	DROP TABLE IF EXISTS FRUTA;<br>
	CREATE TABLE FRUTA (<br>
	    codigo INTEGER PRIMARY KEY,<br>
	    nome VARCHAR(255)<br>
	);<br>

	DROP TABLE IF EXISTS COMPLEMENTO;<br>
	CREATE TABLE COMPLEMENTO (<br>
	    codigo INTEGER PRIMARY KEY,<br>
	    nome VARCHAR(255)<br>
	);<br>

	DROP TABLE IF EXISTS PRODUTO_FRUTA;<br>
	CREATE TABLE PRODUTO_FRUTA (<br>
	    fk_FRUTA_codigo INTEGER,<br>
	    fk_PRODUTO_codigo INTEGER<br>
	);<br>
	<br>
	DROP TABLE IF EXISTS PRODUTO_COMPLEMENTO;<br>
	CREATE TABLE PRODUTO_COMPLEMENTO (<br>
	    fk_PRODUTO_codigo INTEGER,<br>
	    fk_COMPLEMENTO_codigo INTEGER<br>
	);<br>
	<br>
	DROP TABLE IF EXISTS PRODUTO_CALDA;<br>
	CREATE TABLE PRODUTO_CALDA<br>
	    fk_CALDA_codigo INTEGER,<br>
	    fk_PRODUTO_codigo INTEGER<br>
	);<br>
	<br>
	DROP TABLE IF EXISTS PEDIDO_PRODUTO;<br>
	CREATE TABLE PEDIDO_PRODUTO (<br>
	    fk_PRODUTO_codigo INTEGER,<br>
	    fk_PEDIDO_codigo INTEGER,<br>
		FOREIGN KEY (fk_PRODUTO_codigo)<br>
	    REFERENCES PRODUTO (codigo),<br>
		FOREIGN KEY (fk_PEDIDO_codigo)
	    REFERENCES PEDIDO (codigo)<br>
	);<br>
	<br>
        
       
### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>
        a) inclusão das instruções de inserção dos dados nas tabelas criadas pelo script de modelo físico
        (Drop para exclusão de tabelas + create definição de para tabelas e estruturas de dados + insert para dados a serem inseridos)
        b) Criar um novo banco de dados para testar a restauracao 
        (em caso de falha na restauração o grupo não pontuará neste quesito)
        c) formato .SQL


### 9	TABELAS E PRINCIPAIS CONSULTAS<br>
    OBS: Usar o colab para apresentar os resultados que devem incluir as instruções SQL + resultados em forma de tabela.<br>
    
    LINK DO COLAB: https://colab.research.google.com/drive/1TnGEAMw-GhBKL_J_CNiLCnEioEFcl8vr?usp=sharing
#### 9.1	CONSULTAS DAS TABELAS COM TODOS OS DADOS INSERIDOS (Todas) <br>

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



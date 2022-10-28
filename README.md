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

A empresa "ACAIFES" visa colaborar com prestador de serviço na distribuição de açaí para o instituto federal do espiríto Santo,tendo em vista que o local não tem acesso há muitos comércios e que certamente será sucesso, o propretário deseja que desde o início de seu negócio tenha total controle de vendas e entradas para que assim tenha maior controle no estoque e em nenhuma hipótese falte matéria prima e etc,visando também ser um ambiente acadêmico é necessário horários estratégicos. Para que as aplicações sejam feitas adequadamente é necessário um sistema com o cadastro do cliente pois assim pode er feito o controle dos mesmos,já do produto será armazenado código,valor,tamanho e complementos ;outra forma de conseguir saber quais produtos e tamanhos são mais vendidos ou não.Nesta aplicação manteremos também informações do funcionário ao proprietário,vizamos essa informação importante pois uma vez que haja erros na entrega do produto será possível que saiba o responsável e assim corrigí-las de maneira mais direta e controle também da data de contratação e etc deste pois entendemos que é muito mais provável alcançar o sucesso se houver uma equipe unida e organizada.

--------Nossa motivação é a união da equipe pois acreditamos que é o que faz o trabalho alcançar o sucesso-----(frase motivacional necessária para que o empresário insira aos funcionários um controle de modo que os mesmos aceitem como algo bom e não como uma vigilancia constante e assim o cumpram com mais amor )----------
 
 

### 3.MINI-MUNDO<br>

> Em uma açaiteria chamada "Açaifes" o dono deseja criar um sistema para melhor controle de seu delivery. Nesse sistema cada cliente possuirá um cadastro, para isso será armazenado as informações do cliente de nome e cpf. Do cadastro será armazenado as informações de codigo, telefone e endereço. Um cliente possui deve possuir um único cadastro e o cadastro pertencer a somente um cliente. Além disso, será armazenado as informações sobre cada pedido relizado pelo cliente, sendo elas código, valor unitario de cada produto, quantidade de cada produto, complementos, frutas e calda. Um cliente poderá comprar vários ou nehnum produto e um produto poderá ser vendido para vários ou nenhum cliente. Um produduto possui código e tamanho, sendo que cada pedido possui um ou vários produtos e cada produto pertence a vários ou nenhum pedido. Para melhor supervisão, será armazenado nesse sistema as informações de cada  funcionário, ele possuirá nome, código, salário, data de contratação. Um funcioário realiza vários pedidos ou nenhum pedido e o pedido é realizado por apenas um funcionário.


### 4.PERGUNTAS A SEREM RESPONDIDAS E TABELA DE DADOS<br>
#### 4.1 QUAIS PERGUNTAS PODEM SER RESPONDIDAS COM O SISTEMA PROPOSTO?
    a) O sistema proposto poderá fornecer quais tipos de relatórios e informaçes? 
    b) Crie uma lista com os 5 principais relatórios que poderão ser obtidos por meio do sistema proposto!
    
> A Açaiteria "Açaifes" precisa inicialmente dos seguintes relatórios:
 *Relatório que mostre o valor total do pedido de cada cliente. (informação útil p/ o cliente e o açaí)<br>
 *Relatório que traga o código de todos os pedidos realizados por cada funcionário e o código do cliente responsável por esse pedido.(útil p/ o dono do açaí caso ocorra erros nos pedidos)<br>
 *Relatório que mostre para cada cliente as informações sobre seu pedido, sendo elas o tamanho, complemento, calda, fruta, quantidade e data_hora que realizou o pedido. (útil p/ o funcionário que realizará o pedido)<br>
 *Relatório com os dados de cada cliente sobre: endereço e telefone (útil p/ o motoboy)<br>
 *Relatório de obtenha a quantidade de pedidos por bairro, quantidade de pedidos realizados para cada tamanho de acaí e a quantidade de pedidos por cada forma de pagamento. (útil p/ controle do dono sobre o 

    A) Utilizar a Notação adequada (Preferencialmente utilizar o BR Modelo 3)
    B) O mínimo de entidades do modelo conceitual pare este trabalho será igual a 5 e o Máximo 7.
        * informe quais são as 3 principais entidades do sistema em densenvolvimento<br>(se houverem mais de 3 entidades, pense na importância da entidade para o sistema)       
    C) Principais fluxos de informação/entidades do sistema (mínimo 3). <br>Dica: normalmente estes fluxos estão associados as tabelas que conterão maior quantidade de dados 
    D) Qualidade e Clareza
        Garantir que a semântica dos atributos seja clara no esquema (nomes coerentes com os dados).
        Criar o esquema de forma a garantir a redução de informação redundante, possibilidade de valores null, 
        e tuplas falsas (Aplicar os conceitos de normalização abordados).   
        

    
    
        
    
#### 5.1 Validação do Modelo Conceitual
![image](https://user-images.githubusercontentGrupo01]: Camila,yasmim,Isabellay e Davi nunes 
    [Grupo02]: [Nomes Eduardo
Nycooly
Elisa

#### 5.2 Descrição dos dados 
    [objeto]: [descrição do objeto]
    
    EXEMPLO:
    CLIENTE: Tabela que armazena as informações relativas ao cliente<br>
    CPF: campo que armazena o número de Cadastro de Pessoa Física para cada cliente da empresa.<br>


### 6	MODELO LÓGICO
![image](https://user-images.githubusercontent.com/109684951/198706413-d59ead9d-5406-4c24-b6bc-ed5f56978403.png)

        a) inclusão do esquema lógico do banco de dados
        b) verificação de correspondencia com o modelo conceitual 
        (não serão aceitos modelos que não estejam em conformidade)

### 7	MODELO FÍSICO<br>

DROP TABLE IF EXISTS TELEFONE;
CREATE TABLE 
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
	FOREIGN KEY (FK_CLIENTE_cpf)
    REFERENCES CLIENTE (cpf),
	FOREIGN KEY (FK_ATENDENTE_codigo)
    REFERENCES ATENDENTE (codigo),
	FOREIGN KEY (FK_ENDERECO_codigo)
    REFERENCES ENDERECO (codigo),
	FOREIGN KEY (FK_MOTOBOY_codigo)
    REFERENCES MOTOBOY (codigo),
	FOREIGN KEY (FK_PAGAMENTO_codigo)
    REFERENCES PAGAMENTO (codigo)
);

DROP TABLE IF EXISTS PRODUTO;
CREATE TABLE PRODUTO (
    codigo INTEGER PRIMARY KEY,
    tamanho VARCHAR(25),
    FK_CALDA_codigo INTEGER
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

DROP TABLE IF EXISTS PRODUTO_FRUTA;
CREATE TABLE PRODUTO_FRUTA (
    fk_FRUTA_codigo INTEGER,
    fk_PRODUTO_codigo INTEGER
);

DROP TABLE IF EXISTS PRODUTO_COMPLEMENTO;
CREATE TABLE PRODUTO_COMPLEMENTO (
    fk_PRODUTO_codigo INTEGER,
    fk_COMPLEMENTO_codigo INTEGER
);

DROP TABLE IF EXISTS PRODUTO_CALDA;
CREATE TABLE PRODUTO_CALDA (
    fk_CALDA_codigo INTEGER,
    fk_PRODUTO_codigo INTEGER
);

DROP TABLE IF EXISTS PEDIDO_PRODUTO;
CREATE TABLE PEDIDO_PRODUTO (
    fk_PRODUTO_codigo INTEGER,
    fk_PEDIDO_codigo INTEGER,
	FOREIGN KEY (fk_PRODUTO_codigo)
    REFERENCES PRODUTO (codigo),
	FOREIGN KEY (fk_PEDIDO_codigo)
    REFERENCES PEDIDO (codigo)
);(
        
       
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



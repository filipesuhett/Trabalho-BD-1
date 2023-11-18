# TRABALHO 01:  Sistema de vendas de veículos

# Introdução e Motivação

O projeto em questão visa o desenvolvimento de um inovador sistema de vendas de veículos, pautado na abrangência de um público diversificado, compreendendo desde entusiastas automotivos experientes até aqueles que estão apenas começando a explorar o universo dos automóveis. Nosso compromisso primordial consiste em criar uma solução minuciosa e criteriosa, projetada para oferecer suporte abrangente a qualquer indivíduo que almeje adquirir um veículo novo.

# Sumário

1. [COMPONENTES](#1-componentes)
2. [MINI-MUNDO](#2-mini-mundo)
3. [PERGUNTAS A SEREM RESPONDIDAS](#3-perguntas-a-serem-respondidas)
4. [-](#-)
5. [DESCRIÇÃO DOS DADOS](#5-descrição-dos-dados)
6. [MODELO LÓGICO](#6-modelo-lógico)
7. [MODELO FÍSICO](#7-modelo-físico)
8. [INSERT APLICADO NAS TABELAS DO BANCO DE DADOS](#8-insert-aplicado-nas-tabelas-do-banco-de-dados)
9. [TABELAS E PRINCIPAIS CONSULTAS](#9-tabelas-e-principais-consultas)
   - [CONSULTAS DAS TABELAS COM TODOS OS DADOS INSERIDOS (Todas)](#91consultas-das-tabelas-com-todos-os-dados-inseridos-todas)
   - [CONSULTAS DAS TABELAS COM FILTROS WHERE (Mínimo 4)](#92consultas-das-tabelas-com-filtros-where-mínimo-4)
   - [CONSULTAS QUE USAM OPERADORES LÓGICOS, ARITMÉTICOS E TABELAS OU CAMPOS RENOMEADOS (Mínimo 11)](#93consultas-que-usam-operadores-lógicos-aritméticos-e-tabelas-ou-campos-renomeados-mínimo-11)
   - [CONSULTAS QUE USAM OPERADORES LIKE E DATAS (Mínimo 12)](#94consultas-que-usam-operadores-like-e-datas-mínimo-12)
   - [INSTRUÇÕES APLICANDO ATUALIZAÇÃO E EXCLUSÃO DE DADOS (Mínimo 6)](#95instruções-aplicando-atualização-e-exclusão-de-dados-mínimo-6)
   - [CONSULTAS COM INNER JOIN E ORDER BY (Mínimo 6)](#96consultas-com-inner-join-e-order-by-mínimo-6)
   - [CONSULTAS COM GROUP BY E FUNÇÕES DE AGRUPAMENTO (Mínimo 6)](#97consultas-com-group-by-e-funções-de-agrupamento-mínimo-6)
   - [CONSULTAS COM LEFT, RIGHT E FULL JOIN (Mínimo 4)](#98consultas-com-left-right-e-full-join-mínimo-4)
   - [CONSULTAS COM SELF JOIN E VIEW (Mínimo 6)](#99consultas-com-self-join-e-view-mínimo-6)
   - [SUBCONSULTAS (Mínimo 4)](#910subconsultas-mínimo-4)
10. [RELATÓRIOS E GRÁFICOS](#10-relatórios-e-gráficos)
11. [AJUSTES DA DOCUMENTAÇÃO, CRIAÇÃO DOS SLIDES E VÍDEO PARA APRESENTAÇÃO FINAL](#11-ajustes-da-documentação-criação-dos-slides-e-vídeo-para-apresentaçao-final-)
12. [FORMATAÇÃO NO GIT](#12-formatacao-no-git)

### 1. COMPONENTES<br>
Integrantes do grupo<br>
Bruno Plazzi: brunoplazzi@hotmail.com<br>
Caio Daniel Meireles de Souza: caiodaniel7437@gmail.com<br>
Filipe Suhett: filipe.gmx@gmail.com<br>
Giovanna Scalfoni: giovanna.scalfoni@gmail.com<br>


### 2. MINI-MUNDO<br>

> Uma pessoa interessada em adquirir um novo carro decide utilizar um Sistema de Auxílio à Compra de Carros para tornar sua decisão mais informada e conveniente. Primeiramente, ela se cadastra no sistema, fornecendo suas informações pessoais, como nome, endereço, data de nascimento e preferências de compra, especificando seu orçamento e o tipo de carro que está buscando.
Com o perfil criado, inicia a pesquisa filtrando os carros disponíveis com base em critérios como marca, modelo, tipo de carroceria, preço do veículo e se é usado ou novo, encontrando várias opções que se encaixam em suas preferências. Para uma decisão mais embasada, utiliza a função de comparação de carros do sistema, analisando detalhadamente diferentes modelos, comparando informações técnicas do carro (motor, desempenho, transmissão, tração, suspensão, freios, direção e dimensões do veículo) e preços. O usuário também pode deixar ou verificas as avaliações de outros motoristas disponíveis no sistema para ter certeza de que os locais de compra são de confiança e possuem um bom atendimento. Além disso, enquanto pesquisa, o usuário recebe notificações sobre ofertas especiais em carros semelhantes aos que está considerando, ajudando-a a se manter atualizada sobre oportunidades de economia.
Após selecionar um dos carros, decide agendar um test drive usando o sistema. Localiza concessionárias locais que oferecem o carro desejado e faz um agendamento conveniente, armazenando data e hora (para que mais de um agendamento não seja marcado no mesmo momento). Concessionárias possuem informações como o nome das mesmas, email de contado e o endereço da unidade. Além disso, clientes podem avaliar as concessionárias em uma escala de 0-5 (estrutura do local, atendimento e outros aspéctos que podem ser observados pelos clientes durante a ida ao local), gerando uma única nota total para a unidade.  
No dia do test drive, visita a concessionária e avalia pessoalmente o carro. Todo o processo que envolve testar o carro, a forma de pagamento e a compra efetiva é feito na concessionária, não tendo relação com o sistema.


### 3. PERGUNTAS A SEREM RESPONDIDAS<br>
#### 3.1 QUAIS PERGUNTAS PODEM SER RESPONDIDAS COM O SISTEMA PROPOSTO?

> A Empresa necessita dos seguintes relatórios:
* Relatório que mostre a quantidade de clientes, para assim saber quais épocas são mais movimentadas e se é possível determinar um padrão
* Relatório que mostre os 20 carros mais acessados na semana, com a quantidade de acessos de cada
* Relatorio que mostre as concessionárias mais populares/bem avaliadas entre os usuários do sistema, com suas localizações e respectiva avaliação final
* Relatório que mostre as informações relacionadas ao perfil dos usuários do sistema. O relatório deve ter informações como o orçamento médio e se o carro vuscado costuma ser novo ou usado
* Relatório que obtenha quantos clientes usuários fizeram o agendamento para um test drive com o auxílio do sistema. Deve mostrar a compatibilidade do carro escolhido com as preferências anteriormente especificadas no perfil do cliente, assim como comparar o orçamento com o preço do carro

    
### 5. MODELO CONCEITUAL<br>
    
    Principais entidades do sistema: Pessoa, Carro e Info_tecnicas. São as principais entidades envolvidas na pesquisa e compra dos carros pelos clientes.
    Principais fluxos: Pessoa compra carro, carro possui informações técnicas e carro pertence a concessionária.
	
![image](https://github.com/filipesuhett/Trabalho-BD-1-Veiculos/assets/72825142/7de783a5-59bd-404f-a494-0b04018c57f9)







    
    
#### 5.1 Validação do Modelo Conceitual
    Sistema de empregos: Erick Kenzo, Jhonata Polito Demuner
    Sistema rodoviário: Lara Aguilar, Rodolfo Oliveira, Erick Gama, João Marcos Pimentel

Os dois grupos acima analisaram o modelo conceitual feito baseado no mini-mundo também apresentado. 
Ambos concordam que o modelo está condizente, sendo um único detalhe o atributo avaliação, na entidade concessionaria, que pode funcionar tanto como atributo quanto como uma nova entidade, estando correto em ambos os casos.


#### 5.2 Descrição dos dados 

    CARRO: Tabela que armazena informações referentes aos carros cadastrados no sistema;
    CODIGO: campo que armazena o número identificador de cada carro no sistema;
    PRECO: campo que armazena o preço de cada carro;
    EH_NOVO: campo que armazena a informação se o carro especificado é novo ou não.

    MARCA: Tabela que armazena informações sobre a marca do carro cadastrado;
    ID: campo que armazena o número identificador da marca;
    NOME: campo que armazena o nome da marca.
    
    MODELO: Tabela que armazena informações sobre os modelos de carro;
    ID: campo que armazena o número identificador do modelo de carro;
    NOME: campo que armazena o nome do modelo do carro;
    SIGLA: campo que armazena a sigla do modelo do carro;
    NUMERO_MOTO: campo que armazena o numero do motor do carro;
    ANO: campo que armazena o ano do carro.

    TIPO_CARROCERIA: Tabela que armazena informações sobre o tipo de carroceria de carro;
    ID: campo que armazena o número identificador do tipo de carroceria;
    TIPO: campo que armazena o tipo de carroceria;
    DESCRICAO: campo que armazena a descrição do tipo de carroceria especificado.

    INFO_TECNICAS: Tabela que armazena as informações técnicas para cada carro do sistema;
    POTENCIA: campo que armazena a potencia, em cavalos, de cada carro;
    FREIOS_ABS: campo que armazena a informação se o freio do carro é ABS ou não;
    DIRECAO_HIDRAULICA: campo que armazena a informação se a direção do carro é hidraulica ou não;
    DIMENSOES: campo que armazena as dimensões do carro especificado.

    MOTOR: Tabela que armazena informações sobre motores de carro;
    ID: campo que armazena o número identificador do motor;
    TIPO: campo que armazena o tipo de motor;

    TRANSMISSAO: Tabela que armazena informações sobre Transmissões de carro;
    ID: campo que armazena o número identificador da Transmissão;
    TIPO: campo que armazena o tipo de transmissão.

    TRACAO: Tabela que armazena informações sobre os tipo de tração dos veiculos;
    ID: campo que armazena o número identificador da tração;
    TIPO: campo que armazena qual a tração.

    SUSPENSAO: Tabela que armazena informações sobre os tipos de suspensão de veiculos;
    ID: campo que armazena o número identificador do tipo de suspensão;
    TIPO: campo que armazena o tipo de suspensão.

    USUARIO: Tabela que armazena as informações de usuário;
    ID: campo que armazena o número identificador dos usuários do aplicativo;
    NOME: campo que armazena o nome do usuário;
    ENDEREÇO: campo que armazena o endereço do usuário;
    EMAIL: campo que armazena o email do usuário.

    CONCESSIONARIA: Tabela que armazena informações relativas aos usuários que são Concessionárias;
    CNPJ: campo que armazena o Cadastro Nacional de Pessoa Jurídica da concessionária.

    PESSOA: Tabela que armazena informações relativas aos usuários que são pessoas físicas;
    PREFERENCIA: campo que armazena a preferência de cada pessoa;
    ORCAMENTO: campo que armazena quanto a pessoa cadastrada tem para comprar o carro;
    TIPO_CARRO: campo que armazena a infromação de qual tipo de carro a pessoa está buscando;
    DTNASC: campo que armazena a data de nascimento do usuário.

    AVALIACAO: Tabela que armazena informações sobre as avalições realizadas;
    ID: campo que armazena o número identificador de cada avaliação;
    NOTA: campo que armazena a nota atribuida na avaliação;
    COMENTARIO: campo que armazena o comentário realizado na avaliação.

    AGENDAMENTO: Tabela que armazena informações sobre os agendamentos de visitas das pessoas às concessionárias;
    CODIGO: campo que armazena o codigo identificador de cada agendamento realizado;
    DATA: campo que  armazena a data que foi agendada para a visita;
    HORA: campo que armazena o horário para qual a agendada a visita.

    COMPRA: relação entre pessoa e carro;
    DATA_HORA: campo que armazena a data e a hora da compra do carro;
    PRECO: campo que armazena o preço pago na compra do carro.


># Marco de Entrega 01: Do item 1 até o item 5.2 (5 PTS) <br> 

### 6. MODELO LÓGICO<br>

![image](https://github.com/filipesuhett/Trabalho-BD-1-Veiculos/assets/72825142/5cb4eebd-2bc1-487b-a452-30581c82dfc3)




        a) inclusão do esquema lógico do banco de dados
        b) verificação de correspondencia com o modelo conceitual 
        (não serão aceitos modelos que não estejam em conformidade)

### 7. MODELO FÍSICO<br>
	CREATE TABLE MODELO (
	    id INTEGER PRIMARY KEY,
	    nome VARCHAR,
	    sigla VARCHAR,
	    numero_motor VARCHAR,
	    ano INTEGER
	);
	
	CREATE TABLE MARCA (
	    id INTEGER PRIMARY KEY,
	    nome VARCHAR
	);
	
	CREATE TABLE USUARIO (
	    id INTEGER PRIMARY KEY,
	    nome VARCHAR,
	    endereco VARCHAR,
	    email VARCHAR
	);
	
	CREATE TABLE CONCESSIONARIA ( 
    	    cnpj VARCHAR   
	    FK_USUARIO_id INTEGER PRIMARY KEY,
    	    FOREIGN KEY (FK_USUARIO_id) REFERENCES USUARIO(id)
	);
	
	CREATE TABLE PESSOA (
	    orcamento FLOAT,
	    preferencia VARCHAR,
	    tipo_carro VARCHAR,
	    FK_USUARIO_id INTEGER PRIMARY KEY,
	    FOREIGN KEY (FK_USUARIO_id) REFERENCES USUARIO(id)
	);
	
	CREATE TABLE AVALIACAO (
	    id INTEGER PRIMARY KEY,
	    nota FLOAT,
	    comentario VARCHAR,
	    FK_PESSOA_FK_USUARIO_id INTEGER,
	    FOREIGN KEY (FK_PESSOA_FK_USUARIO_id) REFERENCES PESSOA(FK_USUARIO_id)
	);
	
	CREATE TABLE MOTOR (
	    id INTEGER PRIMARY KEY,
	    tipo VARCHAR
	);
	
	CREATE TABLE TRANSMISSAO (
	    id INTEGER PRIMARY KEY,
	    tipo VARCHAR
	);
	
	CREATE TABLE TRACAO (
	    id INTEGER PRIMARY KEY,
	    tipo VARCHAR
	);
	
	CREATE TABLE SUSPENSAO (
	    id INTEGER PRIMARY KEY,
	    tipo VARCHAR
	);
	
	CREATE TABLE INFO_TECNICAS (
	    id INTEGER PRIMARY KEY,
	    potencia INTEGER,
	    freio_abs BOOLEAN,
	    direcao_hidraulica BOOLEAN,
	    dimensoes VARCHAR,
	    FK_MOTOR_id INTEGER,
	    FK_TRANSMISSAO_id INTEGER,
	    FK_TRACAO_id INTEGER,
	    FK_SUSPENSAO_id INTEGER,
	    FOREIGN KEY (FK_MOTOR_id) REFERENCES MOTOR(id),
	    FOREIGN KEY (FK_TRANSMISSAO_id) REFERENCES TRANSMISSAO(id),
	    FOREIGN KEY (FK_TRACAO_id) REFERENCES TRACAO(id),
	    FOREIGN KEY (FK_SUSPENSAO_id) REFERENCES SUSPENSAO(id)
	);
	
	CREATE TABLE TIPO_CARROCERIA (
	    id INTEGER PRIMARY KEY,
	    tipo VARCHAR,
	    descricao VARCHAR
	);
	
	CREATE TABLE CARRO (
	    id INTEGER PRIMARY KEY,
	    preco FLOAT,
	    eh_novo BOOLEAN,
	    FK_INFO_TECNICAS_id INTEGER,
	    FK_MARCA_id INTEGER,
	    FK_MODELO_id INTEGER,
	    FK_TIPO_CARROCERIA_id INTEGER,
	    FOREIGN KEY (FK_INFO_TECNICAS_id) REFERENCES INFO_TECNICAS(id),
	    FOREIGN KEY (FK_MARCA_id) REFERENCES MARCA(id),
	    FOREIGN KEY (FK_MODELO_id) REFERENCES MODELO(id),
	    FOREIGN KEY (FK_TIPO_CARROCERIA_id) REFERENCES TIPO_CARROCERIA(id)
	);
	
	CREATE TABLE Compra (
	    FK_PESSOA_FK_USUARIO_id INTEGER,
	    FK_CARRO_id INTEGER,
	    FOREIGN KEY (FK_PESSOA_FK_USUARIO_id) REFERENCES PESSOA(FK_USUARIO_id),
	    FOREIGN KEY (FK_CARRO_id) REFERENCES CARRO(id)
	);
	
	CREATE TABLE AGENDAMENTO (
	    codigo INTEGER PRIMARY KEY,
	    data DATE,
	    hora TIME,
	    FK_PESSOA_FK_USUARIO_id INTEGER,
	    FK_CONCESSIONARIA_FK_USUARIO_id INTEGER,
	    FOREIGN KEY (FK_PESSOA_FK_USUARIO_id) REFERENCES PESSOA(FK_USUARIO_id),
	    FOREIGN KEY (FK_CONCESSIONARIA_FK_USUARIO_id) REFERENCES CONCESSIONARIA(FK_USUARIO_id)
	);

      
### 8. INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>
	DROP TABLE IF EXISTS Compra CASCADE;
	DROP TABLE IF EXISTS AVALIACAO CASCADE;
	DROP TABLE IF EXISTS AGENDAMENTO CASCADE;
	DROP TABLE IF EXISTS CARRO CASCADE;
	DROP TABLE IF EXISTS INFO_TECNICAS CASCADE;
	DROP TABLE IF EXISTS PESSOA CASCADE;
	DROP TABLE IF EXISTS CONCESSIONARIA CASCADE;
	DROP TABLE IF EXISTS USUARIO CASCADE;
	DROP TABLE IF EXISTS TIPO_CARROCERIA CASCADE;
	DROP TABLE IF EXISTS MARCA CASCADE;
	DROP TABLE IF EXISTS MODELO CASCADE;
	DROP TABLE IF EXISTS SUSPENSAO CASCADE;
	DROP TABLE IF EXISTS TRACAO CASCADE;
	DROP TABLE IF EXISTS TRANSMISSAO CASCADE;
	DROP TABLE IF EXISTS MOTOR CASCADE;
	
	/* logico_sprints_v6: */
	
	CREATE TABLE MODELO (
	    id INTEGER PRIMARY KEY,
	    nome VARCHAR,
	    sigla VARCHAR,
	    numero_motor VARCHAR,
	    ano INTEGER
	);
	
	CREATE TABLE MARCA (
	    id INTEGER PRIMARY KEY,
	    nome VARCHAR
	);
	
	CREATE TABLE USUARIO (
	    id INTEGER PRIMARY KEY,
	    nome VARCHAR,
	    endereco VARCHAR,
	    email VARCHAR
	);
	
	CREATE TABLE CONCESSIONARIA (
 	    cnpj VARCHAR
	    FK_USUARIO_id INTEGER PRIMARY KEY,
	    FOREIGN KEY (FK_USUARIO_id) REFERENCES USUARIO(id)
	);
	
	CREATE TABLE PESSOA (
	    orcamento FLOAT,
	    preferencia VARCHAR,
	 	    dtNasc DATE,
	    tipo_carro VARCHAR,
	    FK_USUARIO_id INTEGER PRIMARY KEY,
	    FOREIGN KEY (FK_USUARIO_id) REFERENCES USUARIO(id)
	);
	
	CREATE TABLE AVALIACAO (
	    id INTEGER PRIMARY KEY,
	    nota FLOAT,
	    comentario VARCHAR,
	    FK_PESSOA_FK_USUARIO_id INTEGER,
	    FOREIGN KEY (FK_PESSOA_FK_USUARIO_id) REFERENCES PESSOA(FK_USUARIO_id)
	);
	
	CREATE TABLE MOTOR (
	    id INTEGER PRIMARY KEY,
	    tipo VARCHAR
	);
	
	CREATE TABLE TRANSMISSAO (
	    id INTEGER PRIMARY KEY,
	    tipo VARCHAR
	);
	
	CREATE TABLE TRACAO (
	    id INTEGER PRIMARY KEY,
	    tipo VARCHAR
	);
	
	CREATE TABLE SUSPENSAO (
	    id INTEGER PRIMARY KEY,
	    tipo VARCHAR
	);
	
	CREATE TABLE INFO_TECNICAS (
	    id INTEGER PRIMARY KEY,
	    potencia INTEGER,
	    freio_abs BOOLEAN,
	    direcao_hidraulica BOOLEAN,
	    dimensoes VARCHAR,
	    FK_MOTOR_id INTEGER,
	    FK_TRANSMISSAO_id INTEGER,
	    FK_TRACAO_id INTEGER,
	    FK_SUSPENSAO_id INTEGER,
	    FOREIGN KEY (FK_MOTOR_id) REFERENCES MOTOR(id),
	    FOREIGN KEY (FK_TRANSMISSAO_id) REFERENCES TRANSMISSAO(id),
	    FOREIGN KEY (FK_TRACAO_id) REFERENCES TRACAO(id),
	    FOREIGN KEY (FK_SUSPENSAO_id) REFERENCES SUSPENSAO(id)
	);
	
	CREATE TABLE TIPO_CARROCERIA (
	    id INTEGER PRIMARY KEY,
	    tipo VARCHAR,
	    descricao VARCHAR
	);
	
	CREATE TABLE CARRO (
	    id INTEGER PRIMARY KEY,
	    preco FLOAT,
	    eh_novo BOOLEAN,
	    FK_INFO_TECNICAS_id INTEGER,
	    FK_MARCA_id INTEGER,
	    FK_MODELO_id INTEGER,
	    FK_TIPO_CARROCERIA_id INTEGER,
	    FOREIGN KEY (FK_INFO_TECNICAS_id) REFERENCES INFO_TECNICAS(id),
	    FOREIGN KEY (FK_MARCA_id) REFERENCES MARCA(id),
	    FOREIGN KEY (FK_MODELO_id) REFERENCES MODELO(id),
	    FOREIGN KEY (FK_TIPO_CARROCERIA_id) REFERENCES TIPO_CARROCERIA(id)
	);
	
	CREATE TABLE Compra (
	    FK_PESSOA_FK_USUARIO_id INTEGER,
	    FK_CARRO_id INTEGER,
	    FOREIGN KEY (FK_PESSOA_FK_USUARIO_id) REFERENCES PESSOA(FK_USUARIO_id),
	    FOREIGN KEY (FK_CARRO_id) REFERENCES CARRO(id)
	);
	
	CREATE TABLE AGENDAMENTO (
	    codigo INTEGER PRIMARY KEY,
	    data DATE,
	    hora TIME,
	    FK_PESSOA_FK_USUARIO_id INTEGER,
	    FK_CONCESSIONARIA_FK_USUARIO_id INTEGER,
	    FOREIGN KEY (FK_PESSOA_FK_USUARIO_id) REFERENCES PESSOA(FK_USUARIO_id),
	    FOREIGN KEY (FK_CONCESSIONARIA_FK_USUARIO_id) REFERENCES CONCESSIONARIA(FK_USUARIO_id)
	);
	
	-- MODELO
	INSERT INTO MODELO (id, nome, sigla, numero_motor, ano) VALUES 
	(1, 'HB20', 'S', '1234', 2019),
	(2, 'Yaris', 'S', '12345', 2022),
	(3, 'Tracker', 'SL', '234', 2021),
	(4, 'Cruze', 'Sport', '098', 2022),
	(5, 'Kicks', 'SL', '5678', 2017),
	(6, 'Sentra', 'SV', '546', 2018),
	(7, 'Pulse', 'X', '94802', 2022),
	(8, 'Fastback', 'SP', '809', 2022),
	(9, 'Civic', 'XLR', '998', 2013),
	(10, 'HR-V', 'XS', '777', 2023);
	
	-- MARCA
	INSERT INTO MARCA (id, nome) VALUES 
	(1, 'Toyota'),
	(2, 'Chevrolet'),
	(3, 'Nissan'),
	(4, 'Fiat'),
	(5, 'Honda');
	
	-- USUARIO
	INSERT INTO USUARIO (id, nome, endereco, email) VALUES 
	(1, 'João Silva', 'Rua A, 123', 'joao.silva@example.com'),
	(2, 'Maria Santos', 'Av. B, 456', 'maria.santos@example.com'),
	(3, 'José Oliveira', 'Rua C, 789', 'jose.oliveira@example.com'),
	(4, 'Ana Souza', 'Av. D, 012', 'ana.souza@example.com'),
	(5, 'Pedro Pereira', 'Rua E, 345', 'pedro.pereira@example.com'),
	(6, 'Carro Bom', 'Av. F, 678', 'Carro Bom@example.com'),
	(7, 'Sedan da Hora', 'Rua G, 901', 'SedandaHora@example.com'),
	(8, 'SUVWINS', 'Av. H, 234', 'SUVWINS@example.com'),
	(9, 'ApenasCaminhonete', 'Rua I, 567', 'ApenasCaminhonete@example.com'),
	(10, 'VanForever', 'Av. J, 890', 'VanForever@example.com');
	
	-- CONCESSIONARIA
	INSERT INTO CONCESSIONARIA (cnpj, FK_USUARIO_id) VALUES 
	('12.345.678/0001-90', 6),
	('23.456.789/0001-01',7),
	('34.567.890/0001-12',8),
	('45.678.901/0001-23',9),
	('56.789.012/0001-34',10);
	
	-- PESSOA
	INSERT INTO PESSOA (orcamento, preferencia, tipo_carro, dtNasc, FK_USUARIO_id) VALUES 
	(30000.00, 'Novo', 'SUV', '2000-01-01', 1),
	(25000.00, 'Usado', 'Sedan', '2000-01-01', 2),
	(35000.00, 'Novo', 'Hatchback', '1999-11-20', 3),
	(20000.00, 'Usado', 'Crossover', '2005-05-10', 4),
	(28000.00, 'Novo', 'SUV', '2000-10-12', 5);
	
	-- AVALIACAO
	INSERT INTO AVALIACAO (id, nota, comentario, FK_PESSOA_FK_USUARIO_id) VALUES 
	(1, 4.5, 'Ótima experiência!', 1),
	(2, 3.2, 'Poderia ser melhor.', 2),
	(3, 4.0, 'Muito satisfeito.', 3),
	(4, 3.7, 'Algumas melhorias necessárias.', 4),
	(5, 4.8, 'Excelente atendimento.', 5);
	
	-- MOTOR
	INSERT INTO MOTOR (id, tipo) VALUES 
	(1, 'SLK V10'),
	(2, 'LPS V8'),
	(3, 'RFD V6'),
	(4, 'KLY V4');
	
	-- TRANSMISSAO
	INSERT INTO TRANSMISSAO (id, tipo) VALUES 
	(1, 'Manual'),
	(2, 'CVT'),
	(3, 'Sequencial'),
	(4, 'Semi-Automatico');
	
	-- TRACAO
	INSERT INTO TRACAO (id, tipo) VALUES 
	(1, 'Dianteira'),
	(2, 'Traseira'),
	(3, '4x4');
	
	-- SUSPENSAO
	INSERT INTO SUSPENSAO (id, tipo) VALUES 
	(1, 'Eixo Rigido'),
	(2, 'Feixe de Molas'),
	(3, 'Dupla A'),
	(4, 'Independente');
	
	-- INFO_TECNICAS
	INSERT INTO INFO_TECNICAS (id, potencia, freio_abs, direcao_hidraulica, dimensoes, FK_MOTOR_id, FK_TRANSMISSAO_id, FK_TRACAO_id, FK_SUSPENSAO_id) VALUES 
	(1, 150, true, true, '4x2x1,5', 4, 2, 1, 1),
	(2, 200, true, false, '5x3x2', 3, 2, 1, 4),
	(3, 180, true, true, '6x2x2', 4, 4, 2, 3),
	(4, 170, false, true, '4x2x3', 4, 1, 1, 4),
	(5, 190, true, false, '5x2x1', 2, 3, 2, 3),
	(6, 160, false, true, '4x2x1,5', 3, 3, 3, 3),
	(7, 210, true, false, '4x2x1,5', 1, 1, 1, 1),
	(8, 220, false, true, '3x2,5x1', 2, 2, 2, 2),
	(9, 195, true, true, '4x3x2', 4, 3, 2, 4),
	(10, 185, false, false, '4x2x1,5', 1, 3, 2, 4);
	
	-- TIPO_CARROCERIA
	INSERT INTO TIPO_CARROCERIA (id, tipo, descricao) VALUES 
	(1, 'Sedan médio', 'Conforto e espaço interno'),
	(2, 'SUV Medio', 'Espaço para a familia'),
	(3, 'Hatch', 'Agilidade na cidade'),
	(4, 'Picape', 'Uso para carga e para passageiros'),
	(5, 'utilitário', 'Baixo custo para transporte de cargas'),
	(6, 'SUV Compacto', 'Opção mais barata de SUV'),
	(7, 'SUV Grande', '7 lugares e tração integral'),
	(8, 'Minivan', 'Versatilidade'),
	(9, 'Sedan compacto', 'preço e porta malas mais amplos'),
	(10, 'Sedan grande', 'Segmento premium');
	
	-- CARRO
	INSERT INTO CARRO (id, preco, eh_novo, FK_INFO_TECNICAS_id, FK_MARCA_id, FK_MODELO_id, FK_TIPO_CARROCERIA_id) VALUES 
	(1, 35000.00, true, 1, 1, 1, 1),
	(2, 28000.00, false, 2, 1, 2, 1),
	(3, 38000.00, true, 3, 2, 3, 2),
	(4, 27000.00, false, 4, 2, 4, 1),
	(5, 32000.00, true, 5, 3, 5, 6),
	(6, 30000.00, true, 6, 3, 6, 1),
	(7, 40000.00, false, 7, 4, 7, 2),
	(8, 31000.00, true, 8, 4, 8, 2),
	(9, 33000.00, true, 9, 5, 9, 1),
	(10, 29500.00, true, 10, 5, 10, 6);
	
	-- Compra
	INSERT INTO Compra (FK_PESSOA_FK_USUARIO_id, FK_CARRO_id) VALUES 
	(1, 1),
	(2, 2),
	(3, 3),
	(4, 4),
	(5, 5);
	
	-- AGENDAMENTO
	INSERT INTO AGENDAMENTO (codigo, data, hora, FK_PESSOA_FK_USUARIO_id, FK_CONCESSIONARIA_FK_USUARIO_id) VALUES 
	(1, '2023-10-25', '10:00', 1, 6),
	(2, '2023-11-05', '14:30', 2, 7),
	(3, '2023-11-10', '11:00', 3, 8),
	(4, '2023-11-15', '15:00', 4, 9),
	(5, '2023-11-20', '13:30', 5, 10);
	
	
	-- Tabela MODELO
	SELECT * FROM MODELO;
	
	-- Tabela MARCA
	SELECT * FROM MARCA;
	
	-- Tabela USUARIO
	SELECT * FROM USUARIO;
	
	-- Tabela CONCESSIONARIA
	SELECT * FROM CONCESSIONARIA;
	
	-- Tabela PESSOA
	SELECT * FROM PESSOA;
	
	-- Tabela AVALIACAO
	SELECT * FROM AVALIACAO;
	
	-- Tabela MOTOR
	SELECT * FROM MOTOR;
	
	-- Tabela TRANSMISSAO
	SELECT * FROM TRANSMISSAO;
	
	-- Tabela TRACAO
	SELECT * FROM TRACAO;
	
	-- Tabela SUSPENSAO
	SELECT * FROM SUSPENSAO;
	
	-- Tabela INFO_TECNICAS
	SELECT * FROM INFO_TECNICAS;
	
	-- Tabela TIPO_CARROCERIA
	SELECT * FROM TIPO_CARROCERIA;
	
	-- Tabela CARRO
	SELECT * FROM CARRO;
	
	-- Tabela Compra
	SELECT * FROM Compra;
	
	-- Tabela AGENDAMENTO
	SELECT * FROM AGENDAMENTO;


### 9. TABELAS E PRINCIPAIS CONSULTAS<br>
Os seguintes tópicos foram feitos e organizados no Colab. Link a seguir: 
	https://colab.research.google.com/drive/1aYu0eD-_TnxyzKvVAlqT8S1UWihWf7R6?usp=sharing 
    
#### 9.1	CONSULTAS DAS TABELAS COM TODOS OS DADOS INSERIDOS (Todas) <br>

#### 9.2	CONSULTAS DAS TABELAS COM FILTROS WHERE (Mínimo 4)<br>

#### 9.3	CONSULTAS QUE USAM OPERADORES LÓGICOS, ARITMÉTICOS E TABELAS OU CAMPOS RENOMEADOS (Mínimo 11)
    a) Criar 5 consultas que envolvam os operadores lógicos AND, OR e Not
    b) Criar no mínimo 3 consultas com operadores aritméticos 
    c) Criar no mínimo 3 consultas com operação de renomear nomes de campos ou tabelas

#### 9.4	CONSULTAS QUE USAM OPERADORES LIKE E DATAS (Mínimo 12) <br>
    a) Criar outras 5 consultas que envolvam like ou ilike
    b) Criar uma consulta para cada tipo de função data apresentada.

># Marco de Entrega 02: Do item 6. até o item 9.1 (5 PTS) <br>

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

># Marco de Entrega 03: Do item 9.2 até o ítem 9.10 (10 PTS)<br>

### 10. RELATÓRIOS E GRÁFICOS

#### a) análises e resultados provenientes do banco de dados desenvolvido (usar modelo disponível)
#### b) link com exemplo de relatórios será disponiblizado pelo professor no AVA
#### OBS: Esta é uma atividade de grande relevância no contexto do trabalho. Mantenha o foco nos 5 principais relatórios/resultados visando obter o melhor resultado possível.

    

### 11. AJUSTES DA DOCUMENTAÇÃO, CRIAÇÃO DOS SLIDES E VÍDEO PARA APRESENTAÇAO FINAL <br>

#### a) Modelo (pecha kucha)<br>
#### b) Tempo de apresentação 6:40 

># Marco de Entrega 04: Itens 10 e 11 (20 PTS) <br>
<br>
<br>




### 12. FORMATACAO NO GIT:<br> 
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



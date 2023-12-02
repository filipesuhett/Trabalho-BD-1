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
* Relatório com as concessionárias mais bem avaliadas entre os usuários do sistema
* Relatório com as informações relacionadas aos carros disponíveis no sistema. Questões como modelo de motor, tração, transmissão e suspensão.
* Relatório de quantos agendamentos cada concessionária recebeu com o auxílio do sistema
* Relatório com a quantidade de carros vendidos de acordo se ele é usado ou novo e do ano de fabricação
* Relatório de quantos carros são vendidos por marca e qual o valor médio de cada marca


    
### 5. MODELO CONCEITUAL<br>
    
    Principais entidades do sistema: Pessoa, Carro e Info_tecnicas. São as principais entidades envolvidas na pesquisa e compra dos carros pelos clientes.
    Principais fluxos: Pessoa compra carro, carro possui informações técnicas e carro pertence a concessionária.
	
![image](https://github.com/filipesuhett/Trabalho-BD-1-Veiculos/assets/72825142/23383452-43b1-4e60-b6fe-f56ef06aba73)







    
    
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


># Marco de Entrega 01: Do item 1 até o item 5.2 (5 PTS) <br> 

### 6. MODELO LÓGICO<br>

![image](https://github.com/filipesuhett/Trabalho-BD-1-Veiculos/assets/72825142/6852336c-68bb-4281-9607-8eb6b235ae5f)





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
	    cnpj VARCHAR,
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
	(10, 'HR-V', 'XS', '777', 2023),
	(11, 'Corolla', 'GLI', '12345', 2022),
	(12, 'Onix', 'LT', '67890', 2023),
	(13, 'Renegade', 'Sport', '45678', 2021),
	(14, 'T-Cross', 'Highline', '23456', 2022),
	(15, 'Golf', 'Trendline', '78901', 2023),
	(16, 'Compass', 'Longitude', '34567', 2022),
	(17, 'Argo', 'HGT', '89012', 2021),
	(18, 'Seltos', 'EX', '56789', 2023),
	(19, 'Creta', 'Prestige', '01234', 2022),
	(20, 'Logan', 'Life', '90123', 2023),
	(21, 'Corolla', 'GLI', '123456', 2013),
	(22, 'Cruze', 'LTZ', '234567', 2013),
	(23, 'March', 'S', '345678', 2013),
	(24, 'Onix', 'LT', '456789', 2015),
	(25, 'Kicks', 'SL', '567890', 2015),
	(26, 'Sandero', 'RS', '678901', 2015),
	(27, 'Versa', 'SV', '789012', 2017),
	(28, 'Civic', 'EXR', '890123', 2017),
	(29, 'Rio', 'LX', '901234', 2017),
	(30, 'Fiesta', 'SE', '012345', 2018),
	(31, 'HR-V', 'EX', '123456', 2018),
	(32, 'Soul', 'SX', '234567', 2018),
	(33, 'Gol', 'Trendline', '345678', 2019),
	(34, 'Creta', 'Prestige', '456789', 2019),
	(35, 'EcoSport', 'Titanium', '567890', 2019);
	
	-- MARCA
	INSERT INTO MARCA (id, nome) VALUES 
	(1, 'Toyota'),
	(2, 'Chevrolet'),
	(3, 'Nissan'),
	(4, 'Fiat'),
	(5, 'Honda'),
	(6, 'Renault'),
	(7, 'Jeep'),
	(8, 'Kia'),
	(9, 'Volkswagen'),
	(10, 'Hyundai'),
	(11, 'Ford');
	
	
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
	(10, 'VanForever', 'Av. J, 890', 'VanForever@example.com'),
	(11, 'Carlos Oliveira', 'Rua K, 123', 'carlos.oliveira@example.com'),
	(12, 'Amanda Costa', 'Av. L, 456', 'amanda.costa@example.com'),
	(13, 'Lucas Rodrigues', 'Rua M, 789', 'lucas.rodrigues@example.com'),
	(14, 'Isabela Pereira', 'Av. N, 012', 'isabela.pereira@example.com'),
	(15, 'Fernando Santos', 'Rua O, 345', 'fernando.santos@example.com'),
	(16, 'Larissa Ferreira', 'Rua P, 567', 'larissa.ferreira@example.com'),
	(17, 'Rafael Oliveira', 'Av. Q, 890', 'rafael.oliveira@example.com'),
	(18, 'Mariana Souza', 'Rua R, 123', 'mariana.souza@example.com'),
	(19, 'Guilherme Santos', 'Av. S, 456', 'guilherme.santos@example.com'),
	(20, 'Camila Costa', 'Rua T, 789', 'camila.costa@example.com'),
	(21, 'Leonardo Silva', 'Av. U, 012', 'leonardo.silva@example.com'),
	(22, 'Juliana Pereira', 'Rua V, 345', 'juliana.pereira@example.com'),
	(23, 'Felipe Rodrigues', 'Av. W, 678', 'felipe.rodrigues@example.com'),
	(24, 'Bruna Martins', 'Rua X, 901', 'bruna.martins@example.com'),
	(25, 'Vinicius Fernandes', 'Av. Y, 234', 'vinicius.fernandes@example.com'),
	(26, 'Fernanda Almeida', 'Rua Z, 567', 'fernanda.almeida@example.com'),
	(27, 'Gustavo Lima', 'Av. AA, 890', 'gustavo.lima@example.com'),
	(28, 'Isabella Gonçalves', 'Rua BB, 123', 'isabella.goncalves@example.com'),
	(29, 'Pedro Rocha', 'Av. CC, 456', 'pedro.rocha@example.com'),
	(30, 'Luiza Carvalho', 'Rua DD, 789', 'luiza.carvalho@example.com'),
	(31, 'Lucas Vieira', 'Av. EE, 012', 'lucas.vieira@example.com'),
	(32, 'Amanda Camargo', 'Rua FF, 345', 'amanda.camargo@example.com'),
	(33, 'Matheus Cardoso', 'Av. GG, 678', 'matheus.cardoso@example.com'),
	(34, 'Laura Gomes', 'Rua HH, 901', 'laura.gomes@example.com'),
	(35, 'Ricardo Barbosa', 'Av. II, 234', 'ricardo.barbosa@example.com');
	
	-- CONCESSIONARIA
	INSERT INTO CONCESSIONARIA (cnpj, FK_USUARIO_id) VALUES 
	('12.345.678/0001-90',6),
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
	(28000.00, 'Novo', 'SUV', '2000-10-12', 5),
	(26000.00, 'Novo', 'Hatchback', '1995-05-15', 11),
	(30000.00, 'Usado', 'Sedan', '1990-09-25', 12),
	(28000.00, 'Novo', 'SUV', '1988-12-10', 13),
	(32000.00, 'Usado', 'Crossover', '1992-08-03', 14),
	(29000.00, 'Novo', 'Hatchback', '1998-04-20', 15),
	(27000.00, 'Novo', 'Sedan', '1994-06-20', 16),
	(32000.00, 'Usado', 'Hatchback', '1990-10-15', 17),
	(30000.00, 'Novo', 'SUV', '1988-03-25', 18),
	(29000.00, 'Usado', 'Crossover', '1992-09-03', 19),
	(31000.00, 'Novo', 'Hatchback', '1995-05-10', 20),
	(28000.00, 'Usado', 'SUV', '1998-11-20', 21),
	(30000.00, 'Novo', 'Sedan', '1993-07-12', 22),
	(33000.00, 'Usado', 'Hatchback', '1989-08-30', 23),
	(34000.00, 'Novo', 'SUV', '1996-04-05', 24),
	(32000.00, 'Usado', 'Crossover', '1990-12-15', 25),
	(31000.00, 'Novo', 'Hatchback', '1997-01-22', 26),
	(30000.00, 'Usado', 'SUV', '1994-02-18', 27),
	(29000.00, 'Novo', 'Sedan', '1988-06-07', 28),
	(33000.00, 'Usado', 'Hatchback', '1991-09-28', 29),
	(31000.00, 'Novo', 'SUV', '1995-08-13', 30),
	(30000.00, 'Usado', 'Crossover', '1993-07-04', 31),
	(32000.00, 'Novo', 'Hatchback', '1998-12-30', 32),
	(30000.00, 'Usado', 'SUV', '1989-11-12', 33),
	(29000.00, 'Novo', 'Sedan', '1996-10-25', 34),
	(31000.00, 'Usado', 'Hatchback', '1992-05-17', 35);
	
	-- AVALIACAO
	INSERT INTO AVALIACAO (id, nota, comentario, FK_PESSOA_FK_USUARIO_id) VALUES 
	(1, 4.5, 'Ótima experiência!', 1),
	(2, 3.2, 'Poderia ser melhor.', 2),
	(3, 4.0, 'Muito satisfeito.', 3),
	(4, 3.7, 'Algumas melhorias necessárias.', 4),
	(5, 4.8, 'Excelente atendimento.', 5),
	(6, 4.2, 'Ótimo atendimento!', 11),
	(7, 3.8, 'Poderia melhorar.', 12),
	(8, 4.5, 'Muito satisfeito com a compra.', 13),
	(9, 3.5, 'Algumas falhas no serviço.', 14),
	(10, 4.8, 'Excelente experiência.', 15),
	(11, 4.1, 'Bom atendimento!', 16),
	(12, 3.6, 'Poderia melhorar.', 17),
	(13, 4.3, 'Satisfeito com a compra.', 18),
	(14, 3.9, 'Pequenos problemas.', 19),
	(15, 4.7, 'Excelente experiência.', 20),
	(16, 4.0, 'Ótimo atendimento!', 21),
	(17, 3.8, 'Poderia melhorar.', 22),
	(18, 4.4, 'Muito satisfeito.', 23),
	(19, 3.5, 'Algumas falhas.', 24),
	(20, 4.9, 'Muito bom!', 25),
	(21, 4.2, 'Boa experiência.', 26),
	(22, 3.7, 'Poderia ser melhor.', 27),
	(23, 4.5, 'Muito satisfeito.', 28),
	(24, 3.4, 'Algumas melhorias necessárias.', 29),
	(25, 4.8, 'Excelente atendimento.', 30),
	(26, 3.9, 'Bom serviço.', 31),
	(27, 4.6, 'Muito satisfeito.', 32),
	(28, 3.3, 'Podia ser melhor.', 33),
	(29, 4.9, 'Excelente experiência.', 34),
	(30, 3.7, 'Algumas falhas.', 35),
	(31, 4.5, 'Bom serviço!', 1),
	(32, 3.8, 'Precisa de melhorias.', 19),
	(33, 4.0, 'Satisfeito com a compra.', 11),
	(34, 4.2, 'Atendimento rápido e eficiente.', 12),
	(35, 3.9, 'Poderia ter mais opções.', 13),
	(36, 4.6, 'Ótimo ambiente!', 14),
	(37, 3.5, 'Esperava mais.', 15),
	(38, 4.0, 'Boa experiência no geral.', 11),
	(39, 3.7, 'Poderia ser mais organizado.', 12),
	(40, 4.3, 'Recomendo!', 13),
	(41, 4.1, 'Profissionais competentes.', 14),
	(42, 3.8, 'Poderia ser mais rápido.', 15),
	(43, 4.4, 'Produto de qualidade.', 16),
	(44, 3.6, 'Não atendeu às expectativas.', 17),
	(45, 4.2, 'Ótimo atendimento!', 18),
	(46, 3.9, 'Poderia ter mais opções.', 19),
	(47, 4.0, 'Satisfeito com a compra.', 20),
	(48, 4.5, 'Bom serviço!', 21),
	(49, 3.8, 'Precisa de melhorias.', 22),
	(50, 4.0, 'Satisfeito com a compra.', 23),
	(51, 4.2, 'Atendimento rápido e eficiente.', 24),
	(52, 3.9, 'Poderia ter mais opções.', 25),
	(53, 4.6, 'Ótimo ambiente!', 26),
	(54, 3.5, 'Esperava mais.', 27),
	(55, 4.0, 'Boa experiência no geral.', 28),
	(56, 3.7, 'Poderia ser mais organizado.', 29),
	(57, 4.3, 'Recomendo!', 30),
	(58, 4.1, 'Profissionais competentes.', 31),
	(59, 3.8, 'Poderia ser mais rápido.', 32),
	(60, 4.4, 'Produto de qualidade.', 33);
	
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
	(10, 185, false, false, '4x2x1,5', 1, 3, 2, 4),
	(11, 140, true, false, '4x2x1,5', 2, 1, 1, 2),
	(12, 130, false, true, '5x3x2', 1, 2, 2, 3),
	(13, 150, true, true, '4x2x3', 3, 3, 3, 4),
	(14, 160, true, true, '5x2x1', 4, 4, 1, 2),
	(15, 170, false, false, '4x2x1,5', 2, 1, 2, 3),
	(16, 180, true, true, '3x2,5x1', 3, 2, 3, 4),
	(17, 190, true, false, '4x3x2', 4, 3, 1, 1),
	(18, 200, true, true, '6x2x2', 1, 4, 2, 4),
	(19, 210, true, true, '4x2x1,5', 2, 2, 2, 1),
	(20, 220, false, true, '4x2x1,5', 3, 3, 3, 2),
	(21, 130, true, false, '4x2x1,5', 2, 1, 1, 2),
	(22, 140, true, true, '5x3x2', 1, 2, 2, 3),
	(23, 120, false, true, '4x2x3', 3, 3, 3, 4),
	(24, 150, true, true, '5x2x1', 4, 4, 1, 2),
	(25, 160, false, false, '4x2x1,5', 2, 1, 2, 3),
	(26, 170, true, true, '3x2,5x1', 3, 2, 3, 4),
	(27, 180, true, false, '4x3x2', 4, 3, 1, 1),
	(28, 190, true, true, '6x2x2', 1, 4, 2, 4),
	(29, 200, true, true, '4x2x1,5', 2, 2, 2, 1),
	(30, 210, false, true, '4x2x1,5', 3, 3, 3, 2),
	(31, 140, true, false, '4x2x1,5', 2, 1, 1, 2),
	(32, 150, true, true, '5x3x2', 1, 2, 2, 3),
	(33, 130, false, true, '4x2x3', 3, 3, 3, 4),
	(34, 160, true, true, '5x2x1', 4, 4, 1, 2),
	(35, 170, false, false, '4x2x1,5', 2, 1, 2, 3);
	
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
	(10, 29500.00, true, 10, 5, 10, 6),
	(11, 45000.00, true, 11, 1, 11, 10),
	(12, 32000.00, false, 12, 2, 12, 6),
	(13, 41000.00, true, 13, 7, 13, 2),
	(14, 29000.00, false, 14, 9, 14, 1),
	(15, 38000.00, true, 15, 9, 15, 3),
	(16, 36000.00, true, 16, 7, 16, 2),
	(17, 42000.00, false, 17, 4, 17, 6),
	(18, 33000.00, true, 18, 8, 18, 4),
	(19, 43000.00, true, 19, 10, 19, 3),
	(20, 34000.00, true, 20, 6, 20, 1),
	(21, 25000.00, false, 21, 1, 21, 9),
	(22, 28000.00, true, 22, 2, 22, 1),
	(23, 22000.00, false, 23, 3, 23, 3),
	(24, 27000.00, true, 24, 2, 24, 6),
	(25, 31000.00, true, 25, 3, 25, 2),
	(26, 26000.00, false, 26, 6, 26, 4),
	(27, 30000.00, true, 27, 7, 27, 1),
	(28, 29000.00, true, 28, 5, 28, 3),
	(29, 32000.00, false, 29, 6, 29, 2),
	(30, 33000.00, true, 30, 11, 30, 3),
	(31, 27000.00, false, 31, 10, 31, 6),
	(32, 28000.00, true, 32, 5, 32, 2),
	(33, 30000.00, true, 33, 9, 33, 4),
	(34, 32000.00, false, 34, 10, 34, 1),
	(35, 31000.00, true, 35, 11, 35, 3);
	
	-- Compra
	INSERT INTO Compra (FK_PESSOA_FK_USUARIO_id, FK_CARRO_id) VALUES
	(1, 14), (2, 11), (3, 15), (4, 18), (5, 2), (11, 24), (12, 35), (13, 26), (14, 30), (15, 25), (16, 10), (17, 14), (18, 26), (19, 13), (20, 4), (21, 25), (22, 26), (23, 13), (24, 7), (25, 17), (26, 2), (27, 26), (28, 32), (29, 22), (30, 21), (31, 15), (32, 19), (33, 29), (34, 15), (35, 20), (1, 19), (2, 32), (3, 35), (4, 13), (5, 5), (11, 12), (12, 16), (13, 18), (14, 28), (15, 33), (16, 33), (17, 13), (18, 34), (19, 22), (20, 33), (21, 33), (22, 15), (23, 29), (24, 33), (25, 5), (26, 21), (27, 5), (28, 25), (29, 15), (30, 32), (31, 16), (32, 21), (33, 13), (34, 27), (35, 28), (1, 31), (2, 28), (3, 11), (4, 23), (5, 26), (11, 20), (12, 23), (13, 29), (14, 33), (15, 11), (16, 11), (17, 3), (18, 15), (19, 22), (20, 14), (21, 3), (22, 2), (23, 2), (24, 15), (25, 3), (26, 21), (27, 17), (28, 12), (29, 12), (30, 14), (31, 8), (32, 35), (33, 7), (34, 23), (35, 8), (1, 2), (2, 5), (3, 28), (4, 24), (5, 35), (11, 14), (12, 1), (13, 19), (14, 30), (15, 23), (16, 24), (17, 30), (18, 9), (19, 31), (20, 26), (21, 7), (22, 17), (23, 6), (24, 9), (25, 25), (26, 25), (27, 28), (28, 5), (29, 29), (30, 13), (31, 28), (32, 9), (33, 1), (34, 5), (35, 32), (1, 2), (2, 8), (3, 24), (4, 22), (5, 27), (11, 24), (12, 9), (13, 29), (14, 19), (15, 24), (16, 30), (17, 2), (18, 4), (19, 2), (20, 19), (21, 3), (22, 25), (23, 16), (24, 27), (25, 2), (26, 14), (27, 22), (28, 35), (29, 7), (30, 6), (31, 22), (32, 17), (33, 13), (34, 34), (35, 30), (1, 3), (2, 32), (3, 23), (4, 30), (5, 5), (11, 7), (12, 15), (13, 5), (14, 22), (15, 33), (16, 19), (17, 28), (18, 19), (19, 3), (20, 8), (21, 2), (22, 16), (23, 35), (24, 27), (25, 7), (26, 19), (27, 27), (28, 34), (29, 31), (30, 28), (31, 14), (32, 2), (33, 4), (34, 14), (35, 27), (1, 25), (2, 19), (3, 33), (4, 17), (5, 33), (11, 33), (12, 6), (13, 11), (14, 31), (15, 35), (16, 8), (17, 15), (18, 17), (19, 16), (20, 9), (21, 30), (22, 35), (23, 18), (24, 3), (25, 10), (26, 9), (27, 31), (28, 22), (29, 9), (30, 35), (31, 4), (32, 16), (33, 4), (34, 34), (35, 8), (1, 12), (2, 18), (3, 17), (4, 24), (5, 16), (11, 18), (12, 7), (13, 10), (14, 28), (15, 4), (16, 26), (17, 10), (18, 26), (19, 18), (20, 33), (21, 19), (22, 2), (23, 19), (24, 16), (25, 27), (26, 16), (27, 26), (28, 34), (29, 30), (30, 4), (31, 17), (32, 23), (33, 19), (34, 21), (35, 31), (1, 5), (2, 16), (3, 23), (4, 10), (5, 3), (11, 16), (12, 20), (13, 33), (14, 7), (15, 9), (16, 33), (17, 15), (18, 31), (19, 11), (20, 29), (21, 34), (22, 14), (23, 1), (24, 12), (25, 13), (26, 20), (27, 32), (28, 35), (29, 32), (30, 23), (31, 32), (32, 6), (33, 27), (34, 19), (35, 12), (1, 5), (2, 19), (3, 16), (4, 17), (5, 24), (11, 2), (12, 8), (13, 33), (14, 17), (15, 10), (16, 17), (17, 7), (18, 34), (19, 27), (20, 30), (21, 25), (22, 2), (23, 18), (24, 12), (25, 16), (26, 28), (27, 7), (28, 27), (29, 18), (30, 32), (31, 2), (32, 6), (33, 26), (34, 34), (35, 21), (1, 13), (2, 31), (3, 34), (4, 18), (5, 26), (11, 21), (12, 32), (13, 3), (14, 22), (15, 6), (16, 11), (17, 18), (18, 24), (19, 30), (20, 26), (21, 13), (22, 26), (23, 10), (24, 2), (25, 31), (26, 1), (27, 22), (28, 35), (29, 6), (30, 6), (31, 24), (32, 21), (33, 28), (34, 22), (35, 35), (1, 17), (2, 20), (3, 10), (4, 22), (5, 4), (11, 5), (12, 32), (13, 18), (14, 22), (15, 35), (16, 20), (17, 18), (18, 3), (19, 1), (20, 6), (21, 32), (22, 25), (23, 5), (24, 12), (25, 18), (26, 11), (27, 4), (28, 27), (29, 25), (30, 16), (31, 22), (32, 35), (33, 8), (34, 19), (35, 5), (1, 31), (2, 25), (3, 32), (4, 23), (5, 1), (11, 17), (12, 35), (13, 13), (14, 2), (15, 35), (16, 26), (17, 20), (18, 3), (19, 12), (20, 22), (21, 24), (22, 26), (23, 22), (24, 25), (25, 4), (26, 11), (27, 8), (28, 5), (29, 22), (30, 30), (31, 9), (32, 3), (33, 12), (34, 20), (35, 28), (1, 9), (2, 10), (3, 31), (4, 2), (5, 34), (11, 35), (12, 4), (13, 13), (14, 35), (15, 24), (16, 3), (17, 31), (18, 15), (19, 10), (20, 35), (21, 14), (22, 2), (23, 31), (24, 3), (25, 9), (26, 27), (27, 29), (28, 21), (29, 7), (30, 17), (31, 26), (32, 33), (33, 35), (34, 20), (35, 16), (1, 32), (2, 4), (3, 19), (4, 10), (5, 34), (11, 6), (12, 35), (13, 32), (14, 13), (15, 26), (16, 3), (17, 22), (18, 21), (19, 22), (20, 33), (21, 23), (22, 9), (23, 9), (24, 11), (25, 24), (26, 33), (27, 15), (28, 20), (29, 13), (30, 25), (31, 13), (32, 14), (33, 11), (34, 28), (35, 8), (1, 30), (2, 32), (3, 10), (4, 27), (5, 20), (11, 20), (12, 18), (13, 3), (14, 27), (15, 21), (16, 20), (17, 29), (18, 8), (19, 34), (20, 20), (21, 13), (22, 17), (23, 17), (24, 30), (25, 6), (26, 3), (27, 27), (28, 32), (29, 16), (30, 2), (31, 22), (32, 3), (33, 19), (34, 8), (35, 24), (1, 1), (2, 30), (3, 1), (4, 8), (5, 20), (11, 35), (12, 24), (13, 8), (14, 5), (15, 14), (16, 15), (17, 25), (18, 11), (19, 8), (20, 32), (21, 18), (22, 2), (23, 34), (24, 1), (25, 27), (26, 35), (27, 29), (28, 34), (29, 19), (30, 5), (31, 13), (32, 13), (33, 28), (34, 15), (35, 13), (1, 10), (2, 11), (3, 11), (4, 27), (5, 6), (11, 10), (12, 24), (13, 23), (14, 22), (15, 30), (16, 15), (17, 1), (18, 7), (19, 34), (20, 30), (21, 21), (22, 2), (23, 22), (24, 24), (25, 35), (26, 26), (27, 7), (28, 24), (29, 27), (30, 31), (31, 3), (32, 15), (33, 11), (34, 5), (35, 18), (1, 27), (2, 34), (3, 21), (4, 17), (5, 35), (11, 28), (12, 25), (13, 32), (14, 8), (15, 29), (16, 25), (17, 28), (18, 15), (19, 33), (20, 21), (21, 24), (22, 24), (23, 30), (24, 29), (25, 19), (26, 33), (27, 6), (28, 21), (29, 17), (30, 15), (31, 10), (32, 14), (33, 12), (34, 25), (35, 30), (1, 4), (2, 3), (3, 8), (4, 6), (5, 33), (11, 16), (12, 13), (13, 14), (14, 31), (15, 32), (16, 4), (17, 22), (18, 12), (19, 14), (20, 19), (21, 30), (22, 31), (23, 19), (24, 30), (25, 7), (26, 16), (27, 32), (28, 31), (29, 11), (30, 6), (31, 3), (32, 11), (33, 26), (34, 34), (35, 3), (1, 35), (2, 7), (3, 27), (4, 25), (5, 30), (11, 2), (12, 32), (13, 11), (14, 3), (15, 32), (16, 16), (17, 35), (18, 9), (19, 28), (20, 17), (21, 27), (22, 27), (23, 1), (24, 31), (25, 27), (26, 20), (27, 17), (28, 24), (29, 5), (30, 24), (31, 10), (32, 11), (33, 21), (34, 14), (35, 2), (1, 32), (2, 6), (3, 10), (4, 24), (5, 13), (11, 14), (12, 19), (13, 4), (14, 11), (15, 30), (16, 21), (17, 18), (18, 13), (19, 21), (20, 32), (21, 23), (22, 22), (23, 16), (24, 11), (25, 28), (26, 8), (27, 13), (28, 5), (29, 17), (30, 12), (31, 21), (32, 13), (33, 19), (34, 14), (35, 26), (1, 4), (2, 23), (3, 6), (4, 29), (5, 22), (11, 31), (12, 30), (13, 11), (14, 30), (15, 32), (16, 32), (17, 1), (18, 13), (19, 30), (20, 35), (21, 5), (22, 6), (23, 9), (24, 22), (25, 4), (26, 35), (27, 4), (28, 19), (29, 26), (30, 33), (31, 9), (32, 9), (33, 29), (34, 25), (35, 30), (1, 16), (2, 2), (3, 13), (4, 18), (5, 7), (11, 24), (12, 14), (13, 29), (14, 5), (15, 2), (16, 13), (17, 32), (18, 24), (19, 19), (20, 34), (21, 34), (22, 5), (23, 24), (24, 16), (25, 18), (26, 16), (27, 31), (28, 5), (29, 21), (30, 32), (31, 6), (32, 17), (33, 1), (34, 30), (35, 15), (1, 24), (2, 26), (3, 20), (4, 1), (5, 21), (11, 12), (12, 19), (13, 3), (14, 27), (15, 6), (16, 18), (17, 12), (18, 24), (19, 5), (20, 2), (21, 13), (22, 33), (23, 18), (24, 5), (25, 28), (26, 15), (27, 27), (28, 33), (29, 22), (30, 21), (31, 11), (32, 23), (33, 14), (34, 27), (35, 34), (1, 26), (2, 8), (3, 14), (4, 4), (5, 7), (11, 35), (12, 19), (13, 2), (14, 21), (15, 2), (16, 14), (17, 31), (18, 1), (19, 29), (20, 20), (21, 32), (22, 28), (23, 28), (24, 21), (25, 10), (26, 29), (27, 27), (28, 20), (29, 6), (30, 14), (31, 22), (32, 3), (33, 4), (34, 18), (35, 19), (1, 29), (2, 2), (3, 7), (4, 5), (5, 33), (11, 17), (12, 8), (13, 19), (14, 9), (15, 2), (16, 27), (17, 32), (18, 6), (19, 31), (20, 10), (21, 5), (22, 24), (23, 30), (24, 30), (25, 21), (26, 16), (27, 33), (28, 21), (29, 22), (30, 19), (31, 17), (32, 11), (33, 22), (34, 7), (35, 11), (1, 13), (2, 34), (3, 23), (4, 27), (5, 18), (11, 2), (12, 15), (13, 19), (14, 25), (15, 16), (16, 5), (17, 33), (18, 24), (19, 20), (20, 18), (21, 23), (22, 14), (23, 10), (24, 8), (25, 32), (26, 5), (27, 29), (28, 18), (29, 27), (30, 21), (31, 15), (32, 21), (33, 15), (34, 29), (35, 22), (1, 9), (2, 5), (3, 35), (4, 26), (5, 33), (11, 31), (12, 25), (13, 31), (14, 16), (15, 33), (16, 20), (17, 34), (18, 15), (19, 8), (20, 25), (21, 3), (22, 27), (23, 30), (24, 21), (25, 20), (26, 16), (27, 25), (28, 22), (29, 25), (30, 5), (31, 28), (32, 19), (33, 22), (34, 19), (35, 6), (1, 22), (2, 6), (3, 25), (4, 12), (5, 18), (11, 13), (12, 20), (13, 19), (14, 35), (15, 23), (16, 10), (17, 6), (18, 28), (19, 3), (20, 31), (21, 17), (22, 20), (23, 21), (24, 10), (25, 5), (26, 20), (27, 17), (28, 28), (29, 11), (30, 25), (31, 21), (32, 17), (33, 25), (34, 16), (35, 14), (1, 25), (2, 18), (3, 12), (4, 5), (5, 7), (11, 9), (12, 3), (13, 27), (14, 20), (15, 24), (16, 22), (17, 6), (18, 20), (19, 21), (20, 21), (21, 24), (22, 27), (23, 2), (24, 23), (25, 24), (26, 28), (27, 29), (28, 29), (29, 2), (30, 4), (31, 10), (32, 9), (33, 12), (34, 26), (35, 27), (1, 29), (2, 32), (3, 4), (4, 2), (5, 17), (11, 31), (12, 23), (13, 26), (14, 3), (15, 10), (16, 17), (17, 32), (18, 14), (19, 27), (20, 32), (21, 24), (22, 11), (23, 30), (24, 24), (25, 15), (26, 12), (27, 31), (28, 33), (29, 35), (30, 9), (31, 13), (32, 30), (33, 34), (34, 35), (35, 27), (1, 10), (2, 27), (3, 20), (4, 26), (5, 7), (11, 3), (12, 8), (13, 32), (14, 22), (15, 12), (16, 1), (17, 15), (18, 10), (19, 3), (20, 24), (21, 22), (22, 18), (23, 10), (24, 6), (25, 20), (26, 24), (27, 21), (28, 29), (29, 20), (30, 4), (31, 6), (32, 33), (33, 8), (34, 20), (35, 16), (1, 19), (2, 25), (3, 8), (4, 3), (5, 25), (11, 13), (12, 22), (13, 34), (14, 8), (15, 35);
	
	-- AGENDAMENTO
	INSERT INTO AGENDAMENTO (codigo, data, hora, FK_PESSOA_FK_USUARIO_id, FK_CONCESSIONARIA_FK_USUARIO_id) VALUES 
	(1, '2023-10-25', '10:00', 1, 6),
	(2, '2023-11-05', '14:30', 2, 7),
	(3, '2023-11-10', '11:00', 3, 8),
	(4, '2023-11-15', '15:00', 4, 9),
	(5, '2023-11-20', '13:30', 5, 10),
	(6, '2023-11-25', '09:30', 11, 6),
	(7, '2023-12-05', '11:30', 12, 7),
	(8, '2023-12-10', '10:00', 13, 8),
	(9, '2023-12-15', '14:00', 14, 9),
	(10, '2023-12-20', '13:00', 15, 10),
	(11, '2023-11-25', '09:30', 16, 6),
	(12, '2023-12-05', '11:30', 17, 7),
	(13, '2023-12-10', '10:00', 18, 8),
	(14, '2023-12-15', '14:00', 19, 9),
	(15, '2023-12-20', '13:00', 20, 10),
	(16, '2023-11-25', '09:30', 21, 6),
	(17, '2023-12-05', '11:30', 22, 7),
	(18, '2023-12-10', '10:00', 23, 8),
	(19, '2023-12-15', '14:00', 24, 9),
	(20, '2023-12-20', '13:00', 25, 10),
	(21, '2023-11-25', '09:30', 26, 6),
	(22, '2023-12-05', '11:30', 27, 7),
	(23, '2023-12-10', '10:00', 28, 8),
	(24, '2023-12-15', '14:00', 29, 9),
	(25, '2023-12-20', '13:00', 30, 10),
	(26, '2023-11-25', '09:30', 31, 6),
	(27, '2023-12-05', '11:30', 32, 7),
	(28, '2023-12-10', '10:00', 33, 8),
	(29, '2023-12-15', '14:00', 34, 9),
	(30, '2023-12-20', '13:00', 35, 10),
	(31, '2023-12-05', '09:00', 1, 6),
	(32, '2023-12-06', '13:30', 19, 9),
	(33, '2023-12-07', '15:00', 11, 7),
	(34, '2023-12-08', '10:45', 12, 6),
	(35, '2023-12-09', '14:20', 13, 10),
	(36, '2023-12-10', '11:10', 14, 7),
	(37, '2023-12-11', '16:00', 15, 8),
	(38, '2023-12-12', '08:30', 11, 6),
	(39, '2023-12-13', '12:15', 12, 6),
	(40, '2023-12-14', '14:45', 13, 6),
	(41, '2023-12-15', '09:30', 14, 10),
	(42, '2023-12-16', '11:55', 15, 9),
	(43, '2023-12-17', '13:25', 16, 8),
	(44, '2023-12-18', '15:40', 17, 7),
	(45, '2023-12-19', '08:00', 18, 7),
	(46, '2023-12-20', '10:20', 19, 10),
	(47, '2023-12-21', '12:50', 20, 6),
	(48, '2023-12-22', '14:15', 21, 9),
	(49, '2023-12-23', '16:30', 22, 9),
	(50, '2023-12-24', '09:15', 23, 7),
	(51, '2023-12-25', '11:25', 24, 7),
	(52, '2023-12-26', '13:55', 25, 10),
	(53, '2023-12-27', '15:10', 26, 6),
	(54, '2023-12-28', '08:45', 27, 9),
	(55, '2023-12-29', '10:55', 28, 10),
	(56, '2023-12-30', '12:35', 29, 10),
	(57, '2023-12-31', '14:05', 30, 9),
	(58, '2024-01-01', '16:15', 31, 9),
	(59, '2024-01-02', '09:50', 32, 9),
	(60, '2024-01-03', '11:45', 33, 8);
	
	
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
Os seguintes subtópicos corespondentes ao tópico "9" foram feitos e organizados no Colab. Link a seguir: 
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
A seguir, o link do colab onde foram feitos os relatórios: 
https://colab.research.google.com/drive/10ZrxDePS2s975dSGYxJH1Ly9g2-DISu_?usp=sharing 

### 11. AJUSTES DA DOCUMENTAÇÃO, CRIAÇÃO DOS SLIDES E VÍDEO PARA APRESENTAÇAO FINAL <br>

#### a) Modelo (pecha kucha)<br>
	Slides da apresentação: https://docs.google.com/presentation/d/1Dz_eb6xFFWOOFnBgvoSQkJtSGn6O7KGtyoW4JNXBwBs/edit?usp=sharing

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



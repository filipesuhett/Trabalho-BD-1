# TRABALHO 01:  Sistema de vendas de veículos

# Introdução e Motivação

O projeto em questão visa o desenvolvimento de um inovador sistema de vendas de veículos, pautado na abrangência de um público diversificado, compreendendo desde entusiastas automotivos experientes até aqueles que estão apenas começando a explorar o universo dos automóveis. Nosso compromisso primordial consiste em criar uma solução minuciosa e criteriosa, projetada para oferecer suporte abrangente a qualquer indivíduo que almeje adquirir um veículo novo.

# Sumário

1. [COMPONENTES](#1-componentes)
2. [MINI-MUNDO](#2-mini-mundo)
3. [PERGUNTAS A SEREM RESPONDIDAS](#3-perguntas-a-serem-respondidas)
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
11. [AJUSTES DA DOCUMENTAÇÃO, CRIAÇÃO DOS SLIDES E VÍDEO PARA APRESENTAÇÃO FINAL](#11-ajustes-da-documentação-criação-dos-slides-e-vídeo-para-apresentação-final)
12. [FORMATAÇÃO NO GIT](#12-formatação-no-git)

### 1. COMPONENTES<br>
Integrantes do grupo<br>
Giovanna Scalfoni: giovanna.scalfoni@gmail.com<br>
Filipe Suhett: filipe.gmx@gmail.com<br>
Bruno Plazzi: brunoplazzi@hotmail.com<br>
Caio Daniel Meireles de Souza: caiodaniel7437@gmail.com<br>


### 2. MINI-MUNDO<br>

> Uma pessoa interessada em adquirir um novo carro decide utilizar um Sistema de Auxílio à Compra de Carros para tornar sua decisão mais informada e conveniente. Primeiramente, ela se cadastra no sistema, fornecendo suas informações pessoais, como nome, endereço e preferências de compra, especificando seu orçamento e o tipo de carro que está buscando.
Com o perfil criado, inicia a pesquisa filtrando os carros disponíveis com base em critérios como marca, modelo, tipo de carroceria, preço do veículo e se é usado ou novo, encontrando várias opções que se encaixam em suas preferências. Para uma decisão mais embasada, utiliza a função de comparação de carros do sistema, analisando detalhadamente diferentes modelos, comparando informações técnicas do carro (motor, desempenho, transmissão, tração, suspensão, freios, direção e dimensões do veículo) e preços. O usuário também pode deixar ou verificas as avaliações de outros motoristas disponíveis no sistema para ter certeza de que os locais de compra são de confiança e possuem um bom atendimento. Além disso, enquanto pesquisa, o usuário recebe notificações sobre ofertas especiais em carros semelhantes aos que está considerando, ajudando-a a se manter atualizada sobre oportunidades de economia.
Após selecionar um dos carros, decide agendar um test drive usando o sistema. Localiza concessionárias locais que oferecem o carro desejado e faz um agendamento conveniente, armazenando data e hora (para que mais de um agendamento não seja marcado no mesmo momento). Concessionárias possuem informações como o nome das mesmas, telefone de contado e o endereço da unidade. Além disso, clientes podem avaliar as concessionárias em uma escala de 0-5 (estrutura do local, atendimento e outros aspéctos que podem ser observados pelos clientes durante a ida ao local), gerando uma única nota total para a unidade.  
No dia do test drive, visita a concessionária e avalia pessoalmente o carro. Todo o processo que envolve testar o carro, a forma de pagamento e a compra efetiva é feito na concessionária, não tendo relação com o sistema.


### 3. PERGUNTAS A SEREM RESPONDIDAS<br>
#### 3.1 QUAIS PERGUNTAS PODEM SER RESPONDIDAS COM O SISTEMA PROPOSTO?

> A Empresa necessita dos seguintes relatórios:
* Relatório que mostre os municipios e estados que mais acessam o sistema, tal qual a quantidade de acessos
* Relatório que mostre os 20 carros mais acessados na semana, com a quantidade de acessos de cada
* Relatorio que mostre as concessionárias mais populares/bem avaliadas entre os usuários do sistema, com suas localizações e respectiva avaliação final
* Relatório que mostre as informações relacionadas ao perfil dos usuários do sistema. O relatório deve ter informações como: sexo, idade, modelos de carro preferidos, marcas preferidas e orçamento médio
* Relatório que obtenha quantos clientes usuários fizeram a compra efetiva do carro com o auxílio do sistema. Deve mostrar a compatibilidade do carro comprado com as preferências anteriormente especificadas no perfil do cliente, assim como comparar o orçamento com o preço pago

    
### 5. MODELO CONCEITUAL<br>
    
    Principais entidades do sistema: Pessoa, Carro e Info_tecnicas. São as principais entidades envolvidas na pesquisa e compra dos carros pelos clientes.
    Principais fluxos: Pessoa compra carro, carro possui informações técnicas e carro pertence a concessionária.
	
![image](https://github.com/filipesuhett/Trabalho-BD-1/assets/72825142/f85f089d-48db-45ba-abd3-9e3fd81f2c7e)


    
    
#### 5.1 Validação do Modelo Conceitual
    Sistema de empregos: Erick Kenzo, Jhonata Polito Demuner
    Sistema rodoviário: Lara Aguilar, Rodolfo Oliveira, Erick Gama, João Marcos Pimentel


#### 5.2 Descrição dos dados 
    [objeto]: [descrição do objeto]
    
    EXEMPLO:
    CLIENTE: Tabela que armazena as informações relativas ao cliente<br>
    CPF: campo que armazena o número de Cadastro de Pessoa Física para cada cliente da empresa.<br>

># Marco de Entrega 01: Do item 1 até o item 5.2 (5 PTS) <br> 

### 6. MODELO LÓGICO<br>
        a) inclusão do esquema lógico do banco de dados
        b) verificação de correspondencia com o modelo conceitual 
        (não serão aceitos modelos que não estejam em conformidade)

### 7. MODELO FÍSICO<br>
        a) inclusão das instruções de criacão das estruturas em SQL/DDL 
        (criação de tabelas, alterações, etc..) 

      
### 8. INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>
        a) Script das instruções relativas a inclusão de dados 
	Requisito mínimo: (Script dev conter: Drop para exclusão de tabelas + create definição de para tabelas e estruturas de dados + insert para dados a serem inseridos)
        OBS
	1) Criar um novo banco de dados para testar a restauracao (em caso de falha na restauração o grupo não pontuará neste quesito)
        2) script deve ser incluso no template em um arquivo no formato .SQL


### 9. TABELAS E PRINCIPAIS CONSULTAS<br>
    OBS: Usa template da disciplina disponibilizado no Colab.<br>
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



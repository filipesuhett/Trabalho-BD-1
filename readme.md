# TRABALHO 01:  Sistema de vendas de veículos
Trabalho desenvolvido durante a disciplina de BD1

# Sumário

### 1. COMPONENTES<br>
Integrantes do grupo<br>
Giovanna Scalfoni: giovanna.scalfoni@gmail.com<br>
Filipe Suhett: filipe.gmx@gmail.com<br>
Bruno Plazzi: brunoplazzi@hotmail.com<br>
Caio Daniel Meireles de Souza: caiodaniel7437@gmail.com<br>


### 2.MINI-MUNDO<br>

> Uma pessoa interessada em adquirir um novo carro decide utilizar um Sistema de Auxílio à Compra de Carros para tornar sua decisão mais informada e conveniente. Primeiramente, ela se cadastra no sistema, fornecendo suas informações pessoais, como nome, endereço, data de nascimento e preferências de compra. Especifica seu orçamento e o tipo de carro que está buscando.
Com o perfil criado, inicia a pesquisa filtrando os carros disponíveis com base em critérios como marca, modelo, tipo de carroceria e preço do veículo usado ou novo. Encontra várias opções que se encaixam em suas preferências. Para uma decisão mais embasada, utiliza a função de comparação de carros do sistema, analisando detalhadamente diferentes modelos, comparando especificações técnicas (motor, desempenho, transmissão, tração, suspensão, freios, direção e dimensões do veículo), preços e recursos (como ar condicionado, gps, sistema de som, etc). O usuário também pode deixar ou verificas as avaliações de outros motoristas disponíveis no sistema para ter certeza de que os locais de compra são de confiança e possuem um bom atendimento. Além disso, enquanto pesquisa, o usuário recebe notificações sobre ofertas especiais em carros semelhantes aos que está considerando, ajudando-a a se manter atualizada sobre oportunidades de economia.
Após selecionar um dos carros, decide agendar um test drive usando o sistema. Localiza concessionárias locais que oferecem o carro desejado e faz um agendamento conveniente.
No dia do test drive, visita a concessionária e avalia pessoalmente o carro. Todo o processo que envolve estar o carro, a forma de pagamento e a compra efetiva é feito na concessionária, não tendo relação com o sistema.


### 3.PERGUNTAS A SEREM RESPONDIDAS<br>
#### 3.1 QUAIS PERGUNTAS PODEM SER RESPONDIDAS COM O SISTEMA PROPOSTO?
    a) O sistema proposto poderá fornecer quais tipos de relatórios e informaçes? 
    b) Crie uma lista com os 5 principais relatórios que poderão ser obtidos por meio do sistema proposto!
    
> A Empresa necessita dos seguintes relatórios:
* Relatório que mostre os municipios e estados que mais acessam o sistema, tal qual a quantidade de acessos
* Relatório que mostre os 20 carros mais acessados na semana, com a quantidade de acessos de cada
* Relatorio que mostre as concessionárias mais populares entre os usuários do sistema, com suas localizações e respectiva avaliação final
* Relatório que mostre as informações relacionadas ao perfil dos usuários do sistema. O relatório deve ter informações como: sexo, idade, modelos de carro preferidos, marcas preferidas e orçamento médio
>> ##### Observações: <br> a) perceba que este relatório pode conter linhas com alguns dados repetidos (mas não todos). <br>  b) para os empregados que não possuirem alguma destas informações o valor no registro deve aparecer sem informação/nulo. 
* Relatório que obtenha a frequencia absoluta e frequencia relativa da quantidade de cpfs únicos no relatório anterior. Apresente os resultados ordenados de forma decrescente pela frequencia relativa.

    
### 5.MODELO CONCEITUAL<br>
    
    Principais entidades do sistema: Pessoa, Carro e Info_tecnicas. São as principais entidades envolvidas na pesquisa e compra dos carros pelos clientes.
    Principais fluxos: Pessoa compra carro, carro possui informações técnicas e carro pertence a concessionária.
	
![image](https://github.com/filipesuhett/Trabalho-BD-1/assets/72825142/a817ecf9-6198-4bfe-8cfc-3004037d0ff9)

    
    
#### 5.1 Validação do Modelo Conceitual
    Sistema de empregos: Erick Kenzo, Jhonata Polito Demuner
    Sistema rodoviário: Lara Aguilar, Rodolfo Oliveira, Erick Gama, João Marcos Pimentel


#### 5.2 Descrição dos dados 
    [objeto]: [descrição do objeto]
    
    EXEMPLO:
    CLIENTE: Tabela que armazena as informações relativas ao cliente<br>
    CPF: campo que armazena o número de Cadastro de Pessoa Física para cada cliente da empresa.<br>

># Marco de Entrega 01: Do item 1 até o item 5.2 (5 PTS) <br> 

### 6	MODELO LÓGICO<br>
        a) inclusão do esquema lógico do banco de dados
        b) verificação de correspondencia com o modelo conceitual 
        (não serão aceitos modelos que não estejam em conformidade)

### 7	MODELO FÍSICO<br>
        a) inclusão das instruções de criacão das estruturas em SQL/DDL 
        (criação de tabelas, alterações, etc..) 

      
### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>
        a) Script das instruções relativas a inclusão de dados 
	Requisito mínimo: (Script dev conter: Drop para exclusão de tabelas + create definição de para tabelas e estruturas de dados + insert para dados a serem inseridos)
        OBS
	1) Criar um novo banco de dados para testar a restauracao (em caso de falha na restauração o grupo não pontuará neste quesito)
        2) script deve ser incluso no template em um arquivo no formato .SQL


### 9	TABELAS E PRINCIPAIS CONSULTAS<br>
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

### 10 RELATÓRIOS E GRÁFICOS

#### a) análises e resultados provenientes do banco de dados desenvolvido (usar modelo disponível)
#### b) link com exemplo de relatórios será disponiblizado pelo professor no AVA
#### OBS: Esta é uma atividade de grande relevância no contexto do trabalho. Mantenha o foco nos 5 principais relatórios/resultados visando obter o melhor resultado possível.

    

### 11	AJUSTES DA DOCUMENTAÇÃO, CRIAÇÃO DOS SLIDES E VÍDEO PARA APRESENTAÇAO FINAL <br>

#### a) Modelo (pecha kucha)<br>
#### b) Tempo de apresentação 6:40 

># Marco de Entrega 04: Itens 10 e 11 (20 PTS) <br>
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



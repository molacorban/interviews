Fase técnica (NodeJS) backend | Mola Corban
==========================
## Sobre a Mola

Somos uma solução eficiente que impulsiona os negócios do correspondente bancário

## Este desafio

### Criação de API para importação de dados via planilha 

O objetivo desse desafio é desenvolver um código que seja capaz de importar o arquivo de exemplo em *./arquivos/produtos.csv* para uma base de dados Postgresql.
Fique atento aos seguintes endpoints obrigatórios  

#### End-point de autenticação

* O primeiro passo do fluxo é a criação de um endpoint que validade o usuário e senha passados no corpo da requisição com valores armazenados numa tabela do banco de dados; 
* Caso usuário e senha existam na tabela, um token é obtido. Este serve como identificador da autenticação do usuário e possui um tempo de vida (TTL)
* Caso usuário e senha não existam na tabela de verificação, uma exceção de erro deve ser gerada.

#### End-point de submissão de arquivo

* Segundo passo é a submissão do arquivo do exemplo *./arquivos/produtos.csv* a partir de um endpoint específico para isso | *tratamentos de exceções de erro para tempo execução, formato de arquivo, validação de colunas e campos não são obrigatórios, mas vc ganha pontos se fizer!* :) 
* O acesso à este endpoint é protegido aos que possuem o token obtido na autenticação! 
* O resultado esperado é que o contéudo do arquivo esteja distribuído em tabelas do banco de dados (Uma ou várias, fica a seu critério!) e que este tenha um identificador único gerado automaticamente

!! Tenha em mente que não é possível prever o tamanho do arquivo (o céu é o limite!), então considere estratégias inteligentes para realização desse processo. !!  

#### End-point de consulta aos dados resultantes do processo

* Terceiro passo (e final!) é um novo end-point que retorne os dados da planilha de exemplo que foram inseridos no banco a partir do identificador único passado como paramêtro. 

* O acesso à este endpoint é protegido aos que possuem o token obtido na autenticação!

* Caso não seja possível encontrar o registro a partir da chave única informada como parametro, uma exceção deve ser gerada.   

#### Requisitos

* Ter uma cobertura de teste relativamente boa, a maior que você conseguir!
* Usar algum framework de NodeJS com ORM é um plus, mas não é obrigatório!  
* Utilize um ambiente orquestrado com Docker para NodeJS, NestJS, Postgresql, Redis, Brokers e o que mais julgar necessário. (nos deixe saber como reproduzir - levantar - o ambiente que vc pensou!)
* Se você conseguir implantar alguma solução Serverless será lindo!


## Orientações

* Procure fazer uma API sucinta. 
* O arquivo de exemplo (csv) está no repositório.
* Pensa em escalabilidade, pode ser uma quantidade muito grande de dados.
* Coloque isso em um repositório GIT.
* Colocar as orientações de setup no README do seu repositório.

# Boa sorte 
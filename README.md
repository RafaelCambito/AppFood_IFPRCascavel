### Atividade Prática do Curso de TADS - IFPR Cascavel - Programação WEB II - 2023</br>

### Atividade proposta:</br>
Criar o passo a passo com cada comando para instalar as dependencias e pacotes necessários, configurar e iniciar o docker e como inserir dados no via Insomia ou Postman.</br>

### Considera-se que esse projeto já esta em andamento, então entende-se que o usuário já terá instalado em sua máquina os programas:</br>

Node JS</br>
Yarn</br>
Insomnia</br>

### Como funciona:</br>

Os arquivos do repositório devem estar em uma única pasta</br>
Abrir o pasta do projeto via VSCODE (VSCODE > FILE > OPEN FOLDER)</br>
Abrir terminal via VSCODE e executar os seguintes comandos</br>
	1 - npm install
	2 - npm i -g yarn
	3 - yarn dev
Abrir um segundo terminal via VSCODE para startar o docker:</br>
	1 - docker ps -a
	2 - docker run -p 27017:27017 mongo

OBS: Irá notificar no primeiro terminal a mensagem "Server is runing on http://localhost:3000". Se essa mensagem não aparecer, basta executar novamente no primeiro terminal o comando "yarn dev".

### Cadastros de categorias via Insomnia - Utilização das rotas definidas no arquivo routers.ts
Com o servidor iniciado, Abrir o Insomnia para realizar os cadastros:</br>
	
##### 1 - New Folder - Utilizar nome de pasta como: CATEGORIES

##### 2 - Criação de request com o método POST e utilizando JSON.
		
	2.1 - Na pasta "CATEGORIES", clicar em NEW HTTP REQUEST e renomear esse request para "createCategory"
	2.2 - Definir esse category com o método POST 
	2.3 - Endereço para POST: http://localhost:3000/categories/
	2.4 - Definir o tipo do POST como JSON
	2.5 - Estrutura do Arquivo JSON:
	{
		"icon":"🍕",
		"name":"Pizza"
	}
	OBS: O ícone acima utilizado foi copiado do site (https://emojipedia.org). Ao acessar o site basta pesquisar pelo nome do ícone desejado, copiar e colar no espaço destinado ao ícone no JSON do Insominia.
	No exemplo acima foi copiado o ícone de Pizza.
	2.6 - Clicar em SEND no Insomnia para realizar o cadastro. Deve retornar Status "201 - Created".

##### 3 - Criação de request com método GET para listar as categorias criadas:
	
	3.1 - Na pasta "CATEGORIES", clicar em NEW HTTP REQUEST e renomear esse request para "listCategories"
	3.2 - Definir essa category com o método GET
	3.3 - Endereço para GET: http://localhost:3000/categories/
	3.4 - Manter o tipo como Body
	3.5 - Ao clicar em SEND, deve retornar as categorias cadastradas.

### Cadastros de Products via Insomnia - Utilização das rotas definidas no arquivo routers.ts
Com o servidor iniciado, Abrir o Insomnia para realizar os cadastros:</br>
	
##### 1 - New Folder - Utilizar nome de pasta como: PRODUCTS

##### 2 - Criação de request com o método POST e utilizando MILTIPART.
	
	2.1 - Na pasta "PRODUCTS", clicar em NEW HTTP REQUEST e renomear esse request para "createProducts"
	2.2 - Definir esse category com o método POST 
	2.3 - Endereço para POST: http://localhost:3000/products/
	2.4 - Definir o tipo do POST como MULTIPART
	2.5 - Estrutura do Arquivo MULTIPART:
	2.5.1 - name, description, image (file), price, category
	2.6 - Preencher a estrutura do arquivo e clicar em SEND para cadastrar.

##### 3 - Criação de request com método GET para listar os products cadastrados.

	3.1 - Na pasta "PRODUCTS", clicar em NEW HTTP REQUEST e renomear esse request para "listProducts"
	3.2 - Definir essa category com o método GET 
	3.3 - Endereço para GET: http://localhost:3000/products/
	3.4 - Manter o tipo como Body
	3.5 - Ao clicar em SEND, deve retornar os products cadastrados.

##### OBS = Junto ao repositório, deixei imagens demonstrando os cadastros e pesquisas realizadas utilizando o Insomnia.

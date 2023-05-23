# Atividade Prática do Curso de TADS - IFPR Cascavel - Programação WEB II</br>

Atividade proposta:</br>
Criar o passo a passo com cada comando para instalar as dependencias e pacotes necessários, configurar e iniciar o docker e como inserir dados no via Insomia ou Postman.</br>

# Considera-se que esse projeto já esta em andamento, então entende-se que o usuário já terá instalado em sua máquina os programas:</br>
Node JS</br>
Yarn</br>
Insomnia</br>

# Como funciona:</br>
- Os arquivos do repositório devem estar em uma única pasta</br>
- Abrir o pasta do projeto via VSCODE (VSCODE > FILE > OPEN FOLDER)
- Abrir terminal via VSCODE e executar os seguintes comandos
1 - npm install
2 - npm i -g yarn
3 - yarn dev

- Abrir um segundo terminal via VSCODE para startar o docker:
1 - docker ps -a
2 - docker run -p 27017:27017 mongo
OBS: Irá notificar no primeiro terminal a mensagem "Server is runing on http://localhost:3000". Se essa mensagem não aparecer, basta executar novamente no primeiro terminal o comando "yarn dev".

# Cadastros de categorias via Insomnia
- Com o servidor iniciado, Abrir o Insomnia para realizar os cadastros:</br>
1 - New Folder - Utilizar nome de pasta como: CATEGORIES

2 - Agora será criado um request com o método POST e utilizando JSON.
2.1 - Na pasta "CATEGORIES", clicar em NEW HTTP REQUEST e renomear esse request para "CREATE CATEGORY"
2.2 - Definir esse category com o método POST 
2.3 - Endereço para POST: http://localhost:3000/Categories/
2.4 - Definir o tipo do POST como JSON




- Junto ao diretório existem imagens das requisições com Cadastro, Busca e Atualização dos dados pelo Insomnia</br>

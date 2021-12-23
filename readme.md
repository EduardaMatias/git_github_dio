## Desafio DIO 

Durante o Bootcamp da [Digital innovation one](https://web.dio.me/home) em parceria com a [Inter](https://www.bancointer.com.br/superapp/?utm_source=google&utm_medium=cpc&utm_campaign=Pesquisa+Brand&gclid=CjwKCAiAtouOBhA6EiwA2nLKH-_eJJ2s6QokogX5syb1sjsFr2nC5HRbGTaESV0ri4QnQhLD39daHBoCFIwQAvD_BwE) foi proposto um desafio, onde o objetivo era criar um repositório no GitHub e subir arquivos para o mesmo. Isso levando em conta as aulas de "Introdução ao GIT e GitHub" ministradas pelo professor Otavio. Confira abaixa as anotações feitas em aula!

## Introdução ao GIT

 - GIT é um sistema de versionamento de código destribuído. Foi criado por Linus Torvalds, em 2005.

 - O GIT não tem interface gráfica (ou seja, é CLI), a forma de interagir com o GIT é por linhas de comando.

 - Comandos para usuários do windows:
cd(navegar entre as pastas) <br>
dir (listar; se situar dentro do sistema computacional) <br> 
mkdir(criar pasta) <br>
del / rmdir(remover arquivos \ remover respositório) <br>

 - Comandos para usuários do linux
cd(navegar entre as pastas) <br>
ls (listar; se situar dentro do sistema computacional) <br>
mkdir(criar pasta) <br>
rm -rf (remover arquivos \ remover respositório) <br>

 - Limpar a tela 
CLS (Windows) e Clear (Linux)

## Tópicos fundamentais para entender o funcionamento do Git

- SHA1

Algoritmo de criptação. O algoritimo pega o arquivo (seja foto, video, etc) e o embaralha de forma especifica. A encriptação gera conjunto de caracteres identificador de 40 digitos.

- Objetos fundamentais

1. BLOBS

Onde os arquivos ficam guardados. 

Estrutura do blob: Tipo do objeto + tamanho do objeto + \0 + conteúdo do arquivo.

1. TREES

Armazena blobs. 

Estrutura: Tipo do objeto + tamanho do objeto + \0 + blob + sha1 + nome do arquivo.

Diferentemento da blob, a árvore guarda o nome do arquivo e podem apontar tanto para blobs ou para outras árvores.

4. COMMITS

É possivel escrever uma mensagem nesse objeto que estará explicando os arquivos da pasta.

Estrutura: Tipo do objeto + tamanho do objeto + árvore + parente (ou seja, último commit realizado) + autor + mensagem + timestamp (arquivo de tempo)

 ## Porque o Git é um sistema ditribuído e seguro?

 - Chave SSH

Estabelece uma conexão segura e encriptada entre duas máquinas. 

Conexão estabelecida com duas chaves, sendo uma pública e outra privada.

Gerar chave: 

No git bash 

passo 1: ssh-keygen -t ed25519 -C email@gmail.com <br>
passo 2: selecionar pasta que deseja salvar e a senha <br>
passo 3: localizar na pasta -> cd /c/Users/... <br>
passo 4: cat id_ed25519.pub <br>

No github: Settings > SSH and GPC keys > New SSH key > colar a chave que o git bash retornou após o último passo.

GitBash novamente

passo 1:
input:  eval $(ssh-agent -s) <br> 
output: Agent pid 999 <br>

passo 2: 
input: ssh-add id_ed25519 <br> 
output: Enter passphrase for id_ed25519: <br>
input: senha definida anteriormente <br>
output: id_ed25519 (email2003@gmail.com) <br>

 - Clonar projeto

No github: copiar SSH do projeto

No gitbash: git clone git@github.com:Gurtinho/foodfy.git <br>
ou seja, git clone + SSH do projeto <br>

 - Iniciar GIT

git init (inicializa um repositório) <br>
git add (passa o arquivo de untracked para tracked - staged) <br> <br>
git commit <br>

Ummodified - arquivo que não sofreu modificação <br>
Modified - arquivo que foi modificado <br>
Staged - esperando para ser manipulado <br>

 - Resolvendo conflitos

git add . <br> 
git commit -a <br>
git pull origin main <br>
git push origin main <br>

## Links úteis

[Instalação do GIT](https://git-scm.com/downloads) <br>
[Acesso ao GitHub](https://github.com/) <br>
[Bootcamp DIO+Inter](https://web.dio.me/track/inter-frontend-developer?tab=path)


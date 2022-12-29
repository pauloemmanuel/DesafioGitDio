# Git e Github


   ## **`Introdução`**

O git é uma ferramenta poderosa de versinamento de código distribuído, ou seja, o código tem várias versões em diferentes locais, tornando tudo muito seguro, já que se a máquina de um integrante da equipe der problema, basta clonar o repositório novamente, e se o Git passar por instabilidades, nós teremos o código em máquina local de toda equipe.

O git evita coisas do tipo:
<br>📁 Projeto
<br>📚 Projetov1.zip
<br>📚 ProjetoFinal.zip
<br>📚 ProjetoFinalFinal.zip
<br>📚 ProjetoFinalMesmo.zip

O git usa o SHA1 (Secure Hash Algoritm) para identificar os arquivos e commits de forma segura e rápida, sendo possível ver ao acessar algum repositório e digitar git log, aparecerá:<br>
commit 622e96e8...<br>
O SHA1 é seguro pois é quase impossível muda-lo de forma que fique coerente, assim todo commit leva consigo o author, as alterações e a hora que foi alterado, não podendo ser mudado.

## **`Objetos do GitHub `**
O git se baseia em alguns objetos, são eles:<br>


### Blob 
Todo arquivo para o git é um "blob", ou seja, o git pega os arquivos colocam dentro do "blob" com meta-dados para que o SHA1 dele seja diferente dos outros.

### Tree
São de forma resumida, as pastas do repositório, a raíz do seu repositório é uma tree que aponta para todos os outros arquivos do repositório, é a Tree que monta a estrutura de arquivos do diretório, além disso a tree guarda o nome dos arquivos.

De forma resumida -> (Trees == Pasta && Blob == Arquivos)

Exemplo:<br>
 📁 Tree<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;📁 Tree2 <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;🖼️ Blob2.png <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;🖼️ Blob1.png

Sendo que a "Tree" sabia o nome da Tree2 e de Blob1.png, e a Tree2 sabia o nome de Blob2.png.

### Commit

É o objeto que dá sentido ao git, ele "junta tudo".
Ele leva consigo:
- Nome do autor
- Sua árvore "raíz"
- Último commit realizado
- Mensagem
- TimeStamp

## **`Estados dos arquivos`**

O git possui um ciclo de vida bem definido, todos os arquivos tem "estados", são eles:
### Untracked 
- Arquivo que o git não "conhece", não foi adicionado no repositório
### Unmodified
- Arquivo que não foi modificado, o git entende que é igual o da última versão.
### Modified
- Arquivo modificado , porém ainda não foi usado o git add.
### Staged
- Foi utilizado o git add para adicionar o arquivo para staged, basicamente está pronto para ser commidado

## **`Comandos Git`**

  **git init**
  ```git
  git init - Inicializa o repositório localmente
  ``` 

  **git add**
  ```git
  git add - Adiciona arquivos em Staged
  ``` 
  **git config**
  ```git
  git config - Serve para modificar as configurações locais do git
 
  git config --global user.name -> Configura o nome do usuário

  git config --global user.email -> Configura o email do usuário

  git config --global --unset user.email -> Remove a configuraç
  ``` 
  **git commit**
  ```git
  git commit - Pega os arquivos em Staged e faz um commit

  git commit -m "Mensagem" - Commita com uma mensagem

  git commit -m "Mensagem" - Commita com uma mensagem
  ``` 

  **git branch**
  ```git
  git branch - Lista todas as branches do repositório

  git branch -d nome_do_branch - Deleta a branch caso tenha sido mergeado.

  git branch -D nome_do_branch - Deleta a branch mesmo se ela não tiver sido mergeada
  ```
  **git checkout**
  ```git
  git checkout nome_da_branch - Serve para trocar entre branches

  git checkout -b nome_da_branch - Cria uma nova branch caso ela não exista
  ```

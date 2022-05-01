# Git Fundamentos

## Objetos Fundamentais

Os objetos internos do Git são:

- BLOB: contém os metadados (hash) e o conteúdo de um arquivo

- TREE: contém os metadados da árvore (hash), o nome do arquivo e apontam para blobs ou para outras árvores

- COMMIT: aponta para uma árvore, para um parente, para um autor, para mensagem e tem o timestamp. Também possui um hash com os metadados do commit

## Comandos

- git init: inicializar o repositório git

- ls -a: mostra arquivos ocultos (mostrar a pasta .git, por exemplo)

- git config --global user.email "email@email.com": configura e-mail de usuário

- git config --global user.name "name-here": configura nome de usuário

- git add *: adicionar as alterações

- git commit -m "string-here": dão significado às alterações, carregam metadados

- git status: status dos arquivos

- git remote add origin ULR: adicionar diretório local ao GitHub (ao servidor remoto)

- git remote -v: lista os repositórios remotos adicionados (para o qual está apontado)

- git push origin master: "empurra" os repositório local para o repositório remoto

- git clone: clona um repositório

- ssh-keygen -t ed25519 -C email@email.com: gerar (par) chave(s) SSH

## Ciclo de Vida dos Arquivos

- Tracked são arquivos rastreados pelo Git. Se subdividem em:
  
  - Unmodified: arquivo ainda não modificado
  
  - Modified: arquivo modificado
  
  - Staged: arquivos que estão prontos para serem commitados para o repositório
    
    Quando o commit é feito, o arquivo sai de Staged e vai para Unmodified. É um ciclo.

- Untracked são arquivos ainda não rastreados pelo Git.

## Áreas de Trabalho

- Servidor
  
  - Remote Repository

- Ambiente de desenvolvimento
  
  - Working Directory
  
  - Staging Area
  
  - Local Repository

## Conflito de Merge

- Ocorre quando dois desenvolvedores alteram o mesmo trecho de código

- Para resolver esse conflito basta uma intervenção manual :hand: 

- Deve-se alterar o código e fazer um novo commit.

Comando para trazer o conteúdo/mudanças do repositório remoto: 

- git pull origin master: "puxa" o conteúdo do repositório remoto para o repositório de trabalho local

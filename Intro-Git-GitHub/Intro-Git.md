# Introdução ao Git

#### Site oficial:[Git](https://git-scm.com/downloads)

#### Definição:

-   Sistema de controle de versões distribuído
-   Software livre (open source)
-   Possibilita o histórico completo de revisões de edições de qualquer
    arquivo
-   Inicialmente projetado e desenvolvido por Linus Torvalds, criador do
    sistema Linux.   
    
#### Criptografia SHA1

* Sincronização segura e criptografada entre o git e o github

* SHA1 (Secure Hash Algorithm)* Conjunto de funções hash criptografadas projetadas pela NSA (Agência de Segurança Nacional dos EUA)

* Forma curta de representar um arquivo formado por um conjunto de caracteres identificador de 40 dígitos.
* Comando _openssl sha1_ (nome do arquivo e extensão. Ex. arquivo.txt)

#### Chaves SSH/Token
1. ssh-keygen -t ed25519 -C (seu email)
2. Gera códigos públicos e privados possibilitando a sincronização segura entre o servidor local e remoto.
3. Na pasta .ssh, utilizar no git o comando cat id_ed25519.pub para mostrar a chave pública
4. Copiar no campo SSH Keys no Github
5. Usar o comando eval $(ssh-agent -s)
6. Usar o comando ssh-add id_ed25519
7. Entrar com uma senha
    
#### Objetos:

-   Blobs: Representa o conteúdo que guarda o sha1 do arquivo no diretório
-   Trees: Um conjunto de blobs com nomes dos arquivos nos diretórios
-   Commits: conjunto de árvores e metadados (autor,descrição e timestamp )

#### Ferramentas:

-   Branch: ramificação a partir de um commit, podendo ser revisões ou
    alterações diversas que podem ser mescladas posteriormente no
    servidor remoto.
-   Stash: Cria um espaço à parte, um rascunho do branch principal para
    modificações não salvas, sem carregar o contexto para outra branch,
    podendo ou não ser integrada ao branch.

#### Comandos básicos:

| Comandos básicos                    | Descrição                                                                                                                  |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| git init: iniciar git na pasta bash | Criar um novo repositório                                                                                                  |
| git add:                            | Adiciona arquivo ao index                                                                                                  |
| git add *                           | Adiciona todos os arquivos index                                                                                           |
| git commit -m “commit inicial”      | Avançar para o atual branch                                                                                                |
|                                     | Identificar o nome do usuário                                                                                              |
|                                     | Identificar o email do usuário (o mesmo do login do github)                                                                |
|                                     | Resetar o nome informado                                                                                                   |
|                                     | Resetar o email informado                                                                                                  |
|                                     | Lista todas as configurações do Git                                                                                        |
|                                     | Cria um alias de um comando do git para maior agilidade no comando (incluir após o ponto o alias e seu respectivo comando) |
|                                     | Apagar um alias criado (não esquecer de especificar o alias após o ponto)                                                  |
|                                     | Configurar o git para escrever o código direto no VS Code                                                                  |
|                                     | Desfazer o core editor                                                                                                     |
|                                     | Clonar um repositório em um novo diretório                                                                                 |
|                                     | Atualização remota de um repositório (no caso, no github)                                                                  |
|                                     | Buscar e integrar com outro repositório existente                                                                          |
|                                     | Lista o histórico de commits presentes no repósitório                                                                      |
|                                     | Lista o histórico de commits numa linha                                                                                    |
|                                     | Mover-se entre as branches                                                                                                 |
|                                     | Mover e criar nova branch                                                                                                  |
|                                     | Alterar o nome da branch                                                                                                   |
|                                     | Deletar branch                                                                                                             |
|                                     | Listar branches                                                                                                            |
| git merge "nome_branch"             | Mesclar branches                                                                                                           |
| git stash                           | Espaço temporário numa branch                                                                                              |
| git stash list                      | Listar todas as stashes                                                                                                    |
| git stash pop                       | Mesclar uma stash a um branch                                                                                              |
| git reset --soft HEAD~1             | Reseta um commit para uma posição inversa de stage                                                                         |
| git reset --mixed HEAD~1            | Reseta um commit para uma posição inversa de untracked                                                                     |
| git reset --hard HEAD~1             | Apaga o commit e seu arquivo associado                                                                                     |
| Ctrl + L                            | Limpar entradas no terminal do git                                                                                         |
| ls                                  | listar arquivos e diretórios                                                                                               |
| ls -a                               | listar arquivos e diretórios ocultos                                                                                       |
| q                                   | Sair e retornar à linha de código do git                                                                                   |
| :wq                                 | Sair, salvar e retornar à linha de código do git                                                                           |
| Atalho: tab                         | Autocompleta comandos                                                                                                      |
| Atalho: seta (up/down)              | Lista últimos comandos executados                                                                                          |
#### Transferência - Repositório Github:
1. git add *
2. git commit -m “commit inicial”
3. git log --oneline
4. git remote add origin link_repositório_do_github.git 
5. git branch M- main
6. git push -u origin main

#### Transferência - Mudança de Repositório Github:
1. git add *
2. git commit -m “commit inicial”
3. git log --oneline
4. git remote rm origin
5. git remote add origin novo_repositório_a_ser_apontado.git 
6. git branch M- main
7. git push -u origin main

#### Integrar alterações - Repositório Github:
1. git add *
2. git commit -m “commit inicial”
3. git log --oneline
4. git remote add origin link_repositório_do_github.git 
5. git branch M- main
6. git pull -u origin main



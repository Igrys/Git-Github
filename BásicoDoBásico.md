# Git 

- Estados Possíveis.

  1.Modificado (modifield).

  2.Preparado (staged/index).

  3.Consolidado (committed).

  ## Geral

- Listar Configurações - **git config --list**

- Setar Usuário - **git config --global user.name "example.name"**

- Setar Email - **git config --global user.email "example.email"***

- Setar Editor - **git confing --global core.editor vim**

- Setar Ferramenta de Merge - **git config --global merge.tool vimdiff**

- Setar Arquivos a Serem ignorados - **git config --global core.excludesfile ~/.gitignore**

  

  ## Repositório Local

  - Criar Novo Repositório - **git init**

  - Verificar Status - **git status**

    

  - ### Adicionar arquivo/diretório (STAGED)

    - Adicionar arquivo específico - **git add meu_arquivo.txt**

    - Adicionar diretório específico - **git add meu_diretório**

    - Adicionar Todos os Arquivos - **git add .**

      

  - ### Comitar arquivo/diretório

  - Comitar um arquivo - **git commit meu_arquivo.txt**

  - Comitar vários arquivos - **git commit meu_arquivo.tct meu_outro_arquivo.txt**

  - Comitar informando mensagem - **git commit meuarquivo.txt -m "mensagem"**

    

  - ### Remover arquivo/diretório

  - Remover arquivo - **git rm meu_arquivo.txt**

  - Remover diretório - **git rm -r diretório**

  

  - ### Visualizar histórico *Básico*

  - Exibir histórico - **git log**

  - Exibir histórico com diff das sua últimas alterações - **git log -p -2**

  - Exibir resumo do histórico - **git log --stat**

  

  - ### Repositório Remoto

  - Exibir repositórios remotos - **git remote**  /  **git remote -v**

  - Vincular LOCAL-REMOTO - **git remote add origin "https://github.com/user/repo. git."**

  - Exibir informações dos repositórios remotos - **git remote show origin**

  - Enviar arquivos/diretórios para o repositórios remoto - **git push**

  - Atualizar repositório local de acordo com o remoto - **git pull**

  - Clonar - **git clone "..."**

  

  ## Termos Básicos

  - ## Repositório

    O repositório é a pasta do projeto. Todo repositório tem uma pasta oculta .git. Isso é o que mostra para o git e para você que existe um repositório naquela pasta.

    #### Criar um novo repositório

    - Vá até a pasta do projeto.
    - Use o comando: git init

    ## Commit

    Um commit é um grupo de alterações no código. Toda vez que você quiser "salvar" as alterações feitas por você no repositório, você commita essas mudanças. Um commit contém as alterações que foram feitas nele e uma mensagem descritiva, além de informações meta (data, autor, etc).

    O ideal é que os commit sejam feitos de forma lógica e organizada, por exemplo: Você criou uma alteração no layout e vai comitar ela depois, ao invés de fazer commits separados ("Adição de div no HTML", "Alteração do CSS", "link do CSS"), faça um só commit ("Alteração no layout: <pequena descrição sobre a alteração>").

    Ou seja, faça commit de alterações já completas ou que possam ser completadas por alguém. Nunca separe alterações em pequenos commits de poucas mudanças.

    #### Criar um commit

    - Na pasta do repositório
    - Use o comando: git add *[arquivos a serem adicionados ao commit]*
    - Use o comando: git commit -m *[mensagem]*

    > O comando "git add ." adiciona todos os arquivos alterados num repositório.

    ## Branch

    Branches são separações de código. O branch padrão do projeto é o master. Branches normalmente são utilizados para separar alterações grandes ou novas funcionalidades do projeto, por exemplo: Existe um projeto de blog, os desenvolvedores já fizeram quase toda a parte do blog, mas existem alterações para fazer no sistema de usuários do blog e algumas a fazer no sistema de posts do blog. Para isso, cria se uma branch "usuarios" e uma "posts" (ou algo do tipo) e fazem-se as alterações nessas branches, um time trabalha em cada uma dessas branches, enquanto isso, outro time continua trabalhando em pequenas mudanças ou bugfixes na branch master.

    #### Criar uma branch

    - Use o comando: git branch *[nome da branch]*

    #### Trocar de branch

    - Use o comando: git checkout *[branch de destino]*

    ## Merge

    Um merge é a união de duas branches, normalmente, merges são feitos na branch master. No exemplo do blog, quando a alteração do blog for terminada, alguém vai unir essas alterações na branch master para que elas possam finalmente fazer parte do projeto de fato.

    Os merges costumam dar bastante problema, pois os códigos podem (e provavelmente vão entrar em conflito). Se houverem alterações no mesmo arquivo ou o git não conseguir definir se alguma linha deve ou não entrar no projeto por motivo de conflito, essas alterações deverão ser corrigidas manualmente.

    #### Realizar um merge

    - Vá para a branch de destino (exemplo: git checkout master).
    - Use o comando: git merge *[branch a unir]*

    ## Clone

    Um clone de um repositório funciona como uma branch de um repositório online em um repositório local. Ou seja, quando se deseja trabalhar em um repositório hospedado no github, clona-se esse repositório para o seu computador, trabalha-se nele, e então é pedida a permissão para atualizar as alterações online.

    #### Realizar um clone

    - Use o comando: git clone *[link do repositório]*
    - Uma pasta será criada com o nome do repositório no lugar onde foi realizado o comando.

    ## Pull

    É uma atualização do repositório local. É feito um merge do repositório online com o local para que os conflitos sejam resolvidos e seja possível enviar o código (sem conflitos) para o repositório online por meio de um push.

    - Dentro do repositório.
    - Use o comando: git pull *[nome do repositório remoto]*

    > No caso do github, o nome do repositório remoto costuma ser origin. Quando ocorre um clone, é sempre origin.

    ## Push

    Envia (ou tenta enviar) o código para o repositório online.

    - Dentro do repositório.
    - Use o comando: git push *[node do repositório remoto]*.

    ## Fork

    O fork é como um clone, porém dentro do github. Isso quer dizer que o repositório não vai ser baixado para seu computador, mas será criado um igual na sua conta.

    ## Pull Request

    Um pull request é um pedido que se faz ao dono do repositório para que esse atualize o código dele com o seu código. Ou seja, você pede para que o dono do projeto ao qual você quer contribuir adicione suas modificações ao projeto oficial

  


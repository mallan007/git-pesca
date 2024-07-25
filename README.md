
# DIO | Resumos de Git e GitHub
 
 ## 🔗 Links úteis:

 | Descrição | Link |
 | ----- | ----- |
 | Editor de mds | https://readme.so/pt/editor |
 | Documentação Git | https://git-scm.com/doc|
 | Documentação GitHub | https://docs.github.com/pt |

 ## Objetivos da Aula:

 ## 1. Criar um repositório local e adicioná-lo ao nosso GitHub - remoto; [✅]

 * Criar uma pasta e copiar o caminho do local do arquivo (Estado Work Directory ou comando:

        mkdir nome-da-pasta

 * Criar um repositório no GitHub com o mesmo nome. Há a opção de usar o .git ignore evita que alguns arquivos sejam adicionados no repositório: 

        echo nome-da-pasta/ > .gitignore 

 * Abir a pasta criada, pelo VScode;
 
 *  Ir  até o local da pasta -> botão direito -> "Git Bash here". Ou abrir a aba "Terminal":

        git init 
 (Cria um .git no repositório local);

 * Criar um arquivo no VScode com sua respectiva extensão (Ex: README.md) e salvá-lo: com "Ctrl + S" ou usar o comando: 

        touch nome-da-pasta/nome-do-arquivo.extensão
    
 * Preparar os arquivos na máquina local com suas modificações:
 
        git add . 

 * Adicionar os arquivos para estado Staging, verificando as alterações feitas no Work Directory:

       git status 

 * Aplicar as alterações feitas, adicionando-se um comentário:   
 
        git commit -m "Frase a ser digitada" 
 
 * Criar uma Branch nomeada "main":   
 
        git branch -M main 
 
 * Adicionar o Repositório Remoto através do link criado na página do GitHub como origem:
 
        git remote add origin ['link']https://github.com/user/repo-name.git 
 
 * Atualizar o conteúdo criado no Work Directory para a máquina remota através da branch remota origem - main:

        git push -u origin main 
    
 ## 2. Clonar um repositório remoto para o nosso computador local; [✅]

 *      git clone ['link'](https://github.com/user/repo-name.git);
 * cd repo-name
 (Seleciona a pasta com o repositório)
 * ls 
 (Lista o conteúdo da pasta)
 *      git clone ['link'](https://github.com/user/repo-name.git) --branch feature-1 --single-branch 
 (escolhe e clona apenas a branch "feature-1");

 ## 3. Fazer alterações >> Adicionar arquivos | Comitar + Inserção/Correção de comentário | Desfazer Commits | Enviar arquivos | Excluir arquivos | Restaurar arquivos; [✅]

 ### 3.1. Adicionar arquivos:

 * Verificar o status:

        git status
 (Verifica se há arquivos que não foram salvos no repositório: Non-Staging)

 * Criar um arquivo dentro da pasta aberta no VSCode ou:

         touch nome-da-pasta/nome-do-arquivo.extensão 
 (Comando in-line);
 
 * Adicionar os arquivos para estado Staging:

        git add . 
 
 ### 3.2. Comitar + Inserção/Correção de comentário:

 * Aplicar as alterações feitas:

        git commit
 (O editor será aberto; Pressionar 'i'(inserir); Digitar o comentário a ser feito + 'ENTER'; Pressionar 'ESC' + ':'(comando) + 'w'(escrever) + 'q'(sair) + 'ENTER') 
 
 * Aplicar as alterações feitas, adicionando-se um comentário:       

        git commit -m "Comentário bla-bla-bla"
 
 * Aplicar as alterações feitas, substituindo o comentário do commit anterior: 

        git commit --amend -m "Novo comentário" 
 
 * Abrir o histórico de commits:

       git log

    `commit 540bb50ce115e1638005a877a8affc48bbb903f0`

    `Author: name.user <name.email>`

    `Date:   Ddd Mmm XX XX:XX:XX YYYY -0300` 


 ### 3.3. Desfazer Commits:

 * Após fazer o git log, copiar o Hashcode (formato hexadecimal) do arquivo desejado, selecionando-o e pressionando o botão direito do mouse -> **'Copy'**:

`540bb50ce115e1638005a877a8affc48bbb903f0`
 * O comando para desfazer o commit é:

        git reset 

 * Onde se varia o nível em que a alteração será feita.

  ### 3.3.1 Hard:

        git reset --hard 540bb50ce115e1638005a877a8affc48bbb903f0
 * Desfaz e ignora todas as alterações em nível de **Work Directory**, apagando os arquivos do reporsitório automaticamente;

  ### 3.3.2 Soft:
 * A alteração será feita no nível **Staging** (localmente), nos arquivos posteriores ao arquivo do hash informado:

        git reset --soft 540bb50ce115e1638005a877a8affc48bbb903f0
 

  ### 3.3.3 Mixed (Padrão):
 * Adiciona os arquivos à árvore de trabalho, tornando-os **Untracked Files** (Pré-Staging, necessitando um `git add` posterior);

 * O comando para desfazer o commit é:

        git reset 540bb50ce115e1638005a877a8affc48bbb903f0
 * Ou:

        git reset --mixed 540bb50ce115e1638005a877a8affc48bbb903f0


 -  🛑🛑🛑 **Obs:** 🛑🛑🛑

  - `Desfazer commits é importante ao trabalhar em equipe de modo a evitar conflitos; ` 
  - ` É possível checar todos os Logs já feitos na máquina local através de: `

            git reflog
  - `As alterações de commits devem ser feitas antes de enviá-las para o repositório remoto.`

 ### 3.4. Enviar arquivos:
 * Enviar as alterações da sua máquina local para uma máquina remota:     

            git push

 ### 3.5. Excluir arquivos:
 *  Remover recursivamente e à força todos o conteúdo do diretório especificado, descartando todas as alterações feitas localmente:

           rm -rf nome-do-diretório
 
 * Verificar o status:

        git status
 
 ### 3.6. Restaurar arquivos:
 *  Restaurar os arquivos excluídos anteriormente:

          git restore nome-do-arquivo.extensão

  * Verificar o status:

            git status
 
 ## 4. Criar uma nova Branch; [✅]

 *      git branch nome-da-nova-branch
 *      git checkout nome-da-nova-branch
 *      ls 
 *      git status
 *      git switch nome-da-branch
(trocar de branch)
*       git checkout -b feature/nome-novo
 (troca de branch já nomeando-a)
 ## 5. Realizar um Pull Request e Merge; [✅]

 *      git checkout main
 *      git merge nome-da-nova-branch
 *      git branch

 ## 6. Criar nosso primeiro Fork; []



## 7. Rebase 
https://git-scm.com/book/pt-br/v2/Branches-no-Git-Rebase
   
    



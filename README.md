
# DIO | Resumos de Git e GitHub
 
 ## 🔗 Links úteis:

 | Descrição | Link |
 | ----- | ----- |
 | Editor de mds | https://readme.so/pt/editor |
 | Documentação Git | https://git-scm.com/doc|
 | Documentação GitHub | https://docs.github.com/pt |

 ## Objetivos da Aula:

 ### 1. Criar um repositório local e adicioná-lo ao nosso GitHub - remoto; [✅]

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
    
 ### 2. Clonar um repositório remoto para o nosso computador local; [✅]

 *      git clone ['link'](https://github.com/user/repo-name.git);
 * cd repo-name
 (Seleciona a pasta com o repositório)
 * ls 
 (Lista o conteúdo da pasta)
 *      git clone ['link'](https://github.com/user/repo-name.git) --branch feature-1 --single-branch 
 (escolhe e clona apenas a branch "feature-1");

 ### 3. Fazer alterações >> Adicionar arquivos| Comitar + Inserção/Correção de comentário | Desfazer Commits | Enviar arquivos | Excluir arquivos | Restaurar arquivos; [✅]

 *      git status
 (Verifica se há arquivos que não foram salvos no repositório: Non-Staging)
 * Criar um arquivo dentro da pasta aberta no VSCode ou touch nome-da-pasta/nome-do-arquivo.extensão (Comando in-line);
 *      git add . 
 *      git commit
 (O editor será aberto; Pressionar 'i'(inserir); Digitar o comentário a ser feito + 'ENTER'; Pressionar 'ESC' + ':'(comando) + 'w'(escrever) + 'q'(sair) + 'ENTER') 
 *      git commit -m "Comentário bla-bla-bla"
 (Commita já adicionando um comentário)
 *      git commit --amend -m "Novo comentário" 
 (Substitui o comentário do commit anterior)
 *      git log
 (Abre o histórico de commits)
 *      git push
 *      rm -rf nome-do-diretório
 (Remove recursivamente e à força todos o conteúdo do diretório especificado, descartando todas as alterações feitas localmente)
 *      git status
 *      git restore nome-do-arquivo.extensão
 (Restaura os arquivos excluídos anteriormente)
 *      git status
 

 ### 4. Criar uma nova Branch; [✅]

 *      git branch nome-da-nova-branch
 *      git checkout nome-da-nova-branch
 * ls 
 *      git status

 ### 5. Realizar um Pull Request e Merge; [✅]

 *      git checkout main
 *      git merge nome-da-nova-branch
 *      git branch

 ### 6. Criar nosso primeiro Fork; []



    
   
    




# DIO | Resumos de Git e GitHub
 
 ## 🔗 Links úteis:

 | Descrição | Link |
 | ----- | ----- |
 | Editor de mds | https://readme.so/pt/editor |
 | Documentação Git | https://git-scm.com/doc|
 | Documentação GitHub | https://docs.github.com/pt |

 ## Objetivos da Aula:

 ### 1. Criar um repositório local e adicioná-lo ao nosso GitHub - remoto; [✅]

 * Criar uma pasta (comando: mkdir nome-da-pasta) e copiar o caminho do local do arquivo (Estado Work Directory); 
 * Criar um repositório no GitHub com o mesmo nome (.git ignore evita que alguns arquivos sejam adicionados no repositório, usando o comando: echo nome-da-pasta/ > .gitignore );
 * Abir a pasta criada, pelo VScode;
 * Abrir a aba "Terminal" ou ir no local da pasta -> botão direito -> "Git Bash here";
 *      git init 
(cria um .git no repositório local);
 * Criar um arquivo no VScode com sua respectiva extensão (Ex: README.md) e salvá-lo: com "Ctrl + S" ou usar o comando: 
        touch nome-da-pasta/nome-do-arquivo.extensão
 *      git add . 
 (Adiciona o arquivo para estado Staging);
 *      git status 
 (Verifica as alterações feitas no Work Directory);
 *      git commit -m "Frase a ser digitada" 
 (Aplica as alterações feitas, adicionando-se um comentário);
 *      git branch -M main 
 (Cria-se um Branch nomeado "main");
 *      git remote add origin ['link']https://github.com/user/repo-name.git 
 (Adiciona o  Repositório Remoto através do link criado na página do GitHub como origem);
 *      git push -u origin main 
 (Atualiza o conteúdo criado no Work Directory para a máquina remota através da branch remota origem - main)


 ### 2. Clonar um repositório remoto para o nosso computador local; [✅]

 *      git clone ['link'](https://github.com/user/repo-name.git);
 * cd repo-name
 (Seleciona a pasta com o repositório)
 * ls 
 (Lista o conteúdo da pasta)
 *      git clone ['link'](https://github.com/user/repo-name.git) --branch feature-1 --single-branch 
 (escolhe e clona apenas a branch "feature-1");

 ### 3. Fazer alterações >> Adicionar | Comitar + Correção de comentário | Enviar arquivos | Excluir arquivos | Restaurar arquivos; [✅]

 *      git status
 (Verifica se há arquivos que não foram salvos no repositório: Non-Staging)
 * Criar um arquivo dentro da pasta aberta no VSCode ou touch nome-da-pasta/nome-do-arquivo.extensão (Comando in-line);
 *      git add .  
 *      git commit -m "Comentário bla-bla-bla"
 (Commita adicionando um comentário)
 *      git commit --amend -m "Novo comentário" 
 (Substitui o comentário do commit anterior)
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



    
   
    



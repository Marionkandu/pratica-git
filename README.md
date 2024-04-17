# pratica-git
Repositorio para pratica do git
pratica-git
Repositório para a prática de comandos do Git

git config --global core.editor "code --wait"
O comando acima define o Visual Studio Code como o editor padrão das mensagens de commit

git commit --allow-empty
O parâmetro --allow-emptypermite a criação de um commit vazio, para fins de testes e prática do Git.

git commit -a 
O parâmetro -aadiciona todos os arquivos modificados e não ignorados ao commit atual.

git checkout -b novoBranch
git switch -c novoBranch
O parâmetro -balternativo para novoBranchcriar o branch. o mesmo acontece com o comando git switchcom o parâmetro -c.

git branch -D nomeBranch
git push --delete origin nomeBranch
Para apagar um branch é preciso primeiro apagá-lo localmente (1º comando) e depois propagar a exclusão para o repositório remoto (2º comando).

git log --graph --oneline
O comando logexibe o histórico de commits em detalhes. Com as bandeiras --graphe --onelineexibe o histórico em um formato mais compreensível, através de um grafo (grafo?)

Rebase interativo
Para alterar o autor de um commit, você pode usar o rebase interativo e o comando commit --amend.

Antes, porém , verifique se o editor de mensagens do commit está configurado para o editor do próprio VS Code.

git rebase -i <referenciaCommit>
A referência do commit deve ser sempre para o commit anterior ao commit que deve ser alterado.

No editor de commits, altere a instrução do commit desejada pickpara edit. Em seguida grave e feche o editor.

O rebase fará uma pausa para que você altere as informações do autor.

git commit --amend --reset-author  --no-edit
Caso você queira especificar o autor, utilize um flag --author="Nome do Autor <email@autor>", nesse formato exato.

Caso seu commit seja vazio, silencioso ainda a flag --allow-empty.

Após o reparo do commit, continue o processo do rebase com o comando abaixo.

git rebase --continue
Finalmente, confira o novo histórico localmente e envie ao repositório remoto com segurança .

git push --force

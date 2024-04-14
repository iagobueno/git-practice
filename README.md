# git-practice

## Inicializando repositório no Github

```bash
echo "git-practice" >> README.md	# Cria arquivo READ.md
git init -b main			# Inicializa o repositório com a branch principal "main"
git add -A README.md			# Adiciona o README.md para área de staging
git commit -m "first commit"		# Cria commit inicial
git remote add origin REMOTE-URL	# Adiciona origem do repositório
git push -u origin main			# Envia os arquivos locais da área de staging para o repositório na branch main
```

## Adicionando arquivos a área de staging

```bash
URL="https://people.sc.fsu.edu/~jburkardt/data/png/cat.png"
curl $URL > cat.png						# baixa imagem para o repo
echo "#!/bin/python3" > app.py					# cria programa simples para o repo
echo "print('Hello, World!')" >> app.py 				
git add -A							# adiciona os arquivos para área de staging
git status							# Lista os arquivos que estão e não estão na área de staging	
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	modified:   README.md
	new file:   app.py
	new file:   cat.png
```

## Commitando alterações e enviando para repositório remoto

```bash
git commit -m "adicionando arquivos iniciais"	# Commita um snapshot de todas as alterações no diretório atual
[main 77923cc] adicionando arquivos iniciais
 3 files changed, 26 insertions(+)
 create mode 100644 app.py
 create mode 100644 cat.png

git push -u origin main				# Envia da origin para a main
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 12 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (5/5), 26.17 KiB | 26.17 MiB/s, done.
Total 5 (delta 0), reused 0 (delta 0), pack-reused 0
To github.com-iagobueno:iagobueno/git-practice.git
   3467452..77923cc  main -> main
Branch 'main' set up to track remote branch 'main' from 'origin'.
```

## Ciclo de atualização de código

No momento em que edito este arquivo, o Git já detecta que houve modificações nele em relação
à versão anterior:

```bash
git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
```

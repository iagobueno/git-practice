# git-practice

## Inicializando repositório no Github

```bash
echo "git-practice" >> README.md	# Cria arquivo READ.md
git init -b main			# Inicializa o repositório com a branch principal "main"
git add -A README.md			# Adiciona o README.md para área de staging
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
```



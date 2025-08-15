# Projeto Versionamento com Git e GitHub

Este projeto foi criado para cumprir a atividade de versionamento de código, demonstrando o uso das ferramentas Git e GitHub para controle de versões, manipulação de branches, merge e resolução de conflitos.

## Conteúdo do projeto

- index.txt: arquivo com o conteúdo final conciliado após merge das branches main e feature1.

## Comandos utilizados

```bash
git init
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@exemplo.com"
git status
git add index.txt
git commit -m "Arquivo inicial criado"
git push -u origin main
git checkout -b feature1
git add index.txt
git commit -m "Alteração para GIT na feature1"
git push origin feature1
git checkout main
git add index.txt
git commit -m "Alteração para VERSIONAMENTO na main"
git push origin main
git merge feature1
# Resolver conflito manualmente no index.txt
git add index.txt
git commit -m "Conflito resolvido entre main e feature1"
git push origin main
<HTML>
<HEAD><TITLE>ATIVIDADE DE VERSIONAMENTO</TITLE></HEAD>
<BODY>
   <H1> GIT e VERSIONAMENTO </H1>
</BODY>
</HTML>

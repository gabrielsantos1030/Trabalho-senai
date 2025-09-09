# 1️⃣ Configuração inicial do Git
git config --global user.name "Gabriel Santos dos Reis"
git config --global user.email "gabriel@example.com"

# 2️⃣ Criar repositório local e arquivo inicial
mkdir "atividade-versionamento"
cd "atividade-versionamento"
git init

echo "<HTML>
<HEAD><TITLE>ATIVIDADE DE VERSÃO</TITLE></HEAD>
<BODY>
   <H1> TÍTULO1 </H1>
</BODY>
</HTML>" > index.txt

git status
git add index.txt
git commit -m "Primeira versão do index.txt"

# 3️⃣ Criar repositório remoto e conectar
git remote add origin https://github.com/seuusuario/atividade-versionamento.git
git remote -v
git branch -M main
git push -u origin main

# 4️⃣ Criar branch feature1 e fazer alterações
git checkout -b feature1

echo "<HTML>
<HEAD><TITLE>ATIVIDADE DE VERSÃO</TITLE></HEAD>
<BODY>
   <H1> GIT </H1>
</BODY>
</HTML>" > index.txt

git add index.txt
git commit -m "Alteração para GIT na branch feature1"
git push -u origin feature1

# 5️⃣ Alterações na branch main
git checkout main

echo "<HTML>
<HEAD><TITLE>ATIVIDADE DE VERSÃO</TITLE></HEAD>
<BODY>
   <H1> VERSIONAMENTO </H1>
</BODY>
</HTML>" > index.txt

git add index.txt
git commit -m "Alteração para VERSIONAMENTO na branch main"
git push

# 6️⃣ Atualizar repositório local
git pull origin main

# 7️⃣ Merge da branch feature1 na main e resolução de conflitos
git merge feature1
# -> Conflito será detectado

echo "<HTML>
<HEAD><TITLE>ATIVIDADE DE VERSÃO</TITLE></HEAD>
<BODY>
   <H1> VERSIONAMENTO E GIT </H1>
</BODY>
</HTML>" > index.txt

git add index.txt
git commit -m "Resolução de conflito entre main e feature1"
git push

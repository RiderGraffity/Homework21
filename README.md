2. Створіть папку з набором підпапок і файлів.
mkdir my_git_project
cd my_git_project

mkdir folder1 folder2
echo "File 1 content" > folder1/file1.txt
echo "File 2 content" > folder2/file2.txt

3. Створіть репозиторій у головній папці.
git init

4. Додайте весь вміст папки в індекс репозиторія.
git commit -m "Initial commit: added folder1 and folder2 with files"

5. Створіть commit на підставі даних, доданих в індекс.
git commit -m "Initial commit: added folder1 and folder2 with files"

6. Створіть нову гілку з назвою newbranch.
 git branch newbranch

 7. Створіть нову підпапку з файлами в newbranch, зробіть коміт.
 git checkout newbranch
mkdir folder3
echo "New file in newbranch" > folder3/newfile.txt
git add .
git commit -m "Added folder3 with newfile.txt in newbranch"

8. Перейдіть у гілку master, додайте нову підпапку з файлами, зробіть коміт.
 git checkout master
mkdir folder4
echo "Data in master branch" > folder4/masterfile.txt
git add .
git commit -m "Added folder4 with masterfile.txt in master branch"

9. Перейдіть у гілку newbranch, злийте зміни з master.
  git checkout newbranch
git merge master

10. Перейдіть у master, внесіть конфліктні зміни у файли, зробіть коміт.
git checkout master
echo "Changed content in master" > folder3/newfile.txt
echo "Conflict content in master" > folder4/masterfile.txt
git add .
git commit -m "Made conflicting changes in master"

11. Перейдіть у newbranch, злийте зміни з master, розв’яжіть конфлікти.

git checkout newbranch
git merge master


git add folder3/newfile.txt
git add folder4/masterfile.txt
git commit -m "Resolved merge conflicts between master and newbranch"

12. Залити все на гітхаб 
git push -u origin master
git push -u origin newbranch


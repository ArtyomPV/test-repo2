# test-repo1
hello Git
# ImprovedGit_Seminar03
test repo 2


1. Создаем удаленный репозиторий с файлом README.md
2. Клонируем его в локальный репозиторий
```
git clone git@github.com:ArtyomPV/test-repo1.git
```
3. Создаем пустой удаленный репозиторий.
4. В локальном репозитории удаляем связи с первым удаленным репозиторием.
```
git remote -v
git remote remove origin
```
5. Отправляем локальный репозиторий на второй удаленный репозиторий
```
git remote add origin git@github.com:ArtyomPV/test-repo2.git
git push -u origin main
```
6. Появятся новые связи со вторым репозиторием.

7. Добавим первый удаленный репозиторий к локальному репозиторию 
```
git remote add source git@github.com:ArtyomPV/test-repo1.git
git remote -v
```
8. Добавим изменения в файл и отправим на удаленные репозитории

на основной (origin):
* git push -u origin main

на второй (source)
* git push - source main

9. В удаленных репозиториях внесем изменения в файл и добавим новый файл

10. Добавим изменеия удаленных репозиториев на длокальный
```
git fetch --all 
git merge origin/main
git merge source/main
```
------------------------------------------------------------------------------------

`git status` - просмотр статуса <br>
`git diff` - просмотр разницы состояния фала\ов, так же между коммитами (нужно указать хэш прошлого затем нынешнего состояния, можно указывать первые 4 символа хеша), если указать имя файла, то покажет разницу состояний этого файла, если без имени то состояние всех файлов в репозитории. Так же можно сравнивать состояния из разных веток. Возможно посмотреть разницу двух файлов вне гит репозитория, для этого нужно вписать имя первого файла, затем имя второго файла <br>
`git log` - выводит лог изменений, коммитов <br>
`git blame` - просмотр изменений в файле, с указанием автора и времени изменений файла построчно <br>
`.gitignore` - `!` исключает файл из списка исключений <br>

#### Отмена не сохранённых изменений

`git restore "имя файла"` - откат файла в состояние последнего коммита <br>
`git restore --staged`
`git reset --hard` - удаление всех не закоммиченных изменений <br>
`git clean -f` - удаление всех файлов вне индексации <br>
`git rm --cached "имя файла"` - удаление файла из отслеживания (так же этот файл удалится в удалённом репозитории) <br>

#### Работа с сохранёнными изменениями

`git checkout "commit" "file"` - возвращаем состояние файла к определённому коммиту <br>
`git revert "commit"` - отменяет конкретный коммит <br>
`git revert --no-commit "хэш коммита"` - отмена изменений конкретного коммита <br>
`git reset --soft "commit"` - сброс с отправкой всех сброшенных изменений в индекс <br>
`git reset --mixed "commit"` - можно без ключа (это дефолтное действие команды). С отправкой в рабочий каталог <br>
`git reset --hard "commit"` - сброс до состояния конкретного коммита с удалением всех последующих <br>

`git commit --amend -m "new comment"` - изменение текущего коммита с изменением комментария к нему <br>
`git commit --amend -m --no-edit` - без редактирования комментария <br>

#### Слияния веток

`git checkout -b new-branch` - создаём новую ветку, вносим изменения <br>
`git checkout main` - переключаемся на ветку main <br>
`git merge new-branch` - выполняем слияние веток (из new-branch в main) <br>
`git reset --merge "commit"` - отмена слияния <br>
`git merge --abort` - отмена слияния с конфликтом <br>

#### Откладывание изменений

`git stash` - прячет все не закомиченные изменения <br>
`git stash pop` - добавляет спрятанные изменения в текущее состояние <br>
`git stash list` - список спрятанных изменений <br>
`git stash drop` - удаляет спрятанное изменение <br>
`

#### Работа с сохранёнными изменениями

`git checkout "commit" "file"` - возвращаем состояние файла к определённому коммиту <br>
`git revert "commit"` - отменяет конкретный коммит <br>
`git revert --no-commit "хэш коммита"` - отмена изменений конкретного коммита <br>
`git reset --soft "commit"` - сброс с отправкой всех сброшенных изменений в индекс <br>
`git reset --mixed` - можно без ключа (это дефолтное действие команды). С отправкой в рабочий каталог <br>
`git reset --hard "commit"` - сброс до состояния конкретного коммита с удалением всех последующих <br>

`git commit --amend -m "new comment"` - изменение текущего коммита с изменением комментария к нему <br>
`git commit --amend -m --no-edit` - без редактирования комментария <br>

#### Слияния веток

`git checkout -b new-branch` - создаём новую ветку, вносим изменения <br>
`git checkout main` - переключаемся на ветку main <br>
`git merge new-branch` - выполняем слияние веток (из new-branch в main) <br>
`git reset --merge "commit"` - отмена слияния <br>
`git merge --abort` - отмена слияния с конфликтом <br>

#### Откладывание изменений

`git stash` - прячет все не закомиченные изменения <br>
`git stash pop` - добавляет спрятанные изменения в текущее состояние (добавляет с конца) <br>
`git stash list` - список спрятанных изменений <br>
`git stash drop` - удаляет спрятанное изменение <br>

#### Возможные варианты перемещений\слияний

`git merge "branch name"` - слив из указанной ветки в ту ветку в которой находимся сейчас <br>
`git rebase "branch name"` - перебазирует указанную ветку в текущую <br>
`git cherry-pick "commit"` - вливание конкретного коммита из другой ветки в текущую <br>

# Seminar

`git clone https://github.com/sortedmap/git-advanced-s2`
`git remote remove origin`
`git remote add origin https://github.com/SlavaVasilakiy/Seminar-2.git`
`git branch -M main`
`git push -u origin main`
`git log`
`git diff fe4e2 daaa3`

`git blame index.html`
`git checkout -b first_revert`
`git revert d014a17c`
`message - cause seminar issue`
`git log`
`git checkout main`
`git checkout first_revert`
`git add .`
`git commit -m "Revert commit d014a17c"`
`git push --set-upstream origin first_revert`
Compare pull request

`git checkout main`
`git blame main.js`
`git log`
`git diff 560a30066a37aff0f5d5badcf11304744dde74b5 main.js`
`git checkout -b revert_js`
`git revert 560a30066a37`
`git log`
`git revert 813c8e4b4fadf3b9415c50bfd38440d35d41bfc9`
`git push --set-upstream origin revert_js`

`cd logs`
`git rm --cached *.log`
`echo *.log > .gitignore`

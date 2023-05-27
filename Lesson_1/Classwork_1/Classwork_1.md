`git clone`
`cd "directory"`
`git add .`
`git commit -m init`
`git push -u origin main` - -u(апстрим, для возможности отката) для пустого репо
`git remote -v`
`git pull`
`git log --oneline`
`git remote show origin`
`git remote remove origin` - удаляет связь
`git remote add origin "source"` - добавляет связь
`git remote add source`
`git remote -v`
`git add . \Readme.md`
`git push origin main`
`git push source main`
`git fetch --all` - скачивание обновлений со всех источников, без применения
`git log origin/main ^main`
`git log source/main ^main`
`git merge origin/main`
`git merge source/main`
https://habr.com/ru/articles/161009/

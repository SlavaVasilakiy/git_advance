## Урок 1. Работа с удалёнными репозиториями

1) Выберите какой-нибудь проект на изучаемом вами языке программирования, с которым вы будете тренироваться работать в Git, и инициализируйте в папке этого проекта локальный репозиторий.
2) Создайте непустой удалённый репозиторий (например, с файлом README.md) с именем, соответствующим имени этого проекта.
3) Подключите свой проект к этому удалённому репозиторию и отправьте в него код этого проекта. Самостоятельно разрешите конфликты и проблемы, если они возникнут при выполнении данного задания.

### Solution:

1) `cd lesson1-project/`, `git init`
2) https://github.com/SlavaVasilakiy/lesson1-project
3) `git remote add origin https://github.com/SlavaVasilakiy/lesson1-project.git`
   
    ```bash
    git remote -v
    origin  https://github.com/SlavaVasilakiy/lesson1-project.git (fetch)
    origin  https://github.com/SlavaVasilakiy/lesson1-project.git (push)
    ```

    `git branch main`, `git switch main`, `git add .` 
    `git commit -m "Добавил файлы, первый коммит"`

    ```bash
        git push origin main
    To https://github.com/SlavaVasilakiy/lesson1-project.git
     ! [rejected]        main -> main (fetch first)
    error: failed to push some refs to 'https://github.com/SlavaVasilakiy/lesson1-project.git'
    hint: Updates were rejected because the remote contains work that you do
    hint: not have locally. This is usually caused by another repository pushing
    hint: to the same ref. You may want to first integrate the remote changes
    hint: (e.g., 'git pull ...') before pushing again.
    hint: See the 'Note about fast-forwards' in 'git push --help' for details.
    ```

    `git fetch --all`, `git pull origin main --allow-unrelated-histories`, `git push origin main`
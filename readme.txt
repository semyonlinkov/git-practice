git init - инициализация локального репозитория

git config --global user.email "you@example.com" - указываем нашу почту в конфиге
git config --global user.name "Your Name" - указываем в конфиге имя

git branch -M main - переименовывает master ветку на main

git add . - меняет статус файлов на Staged
git commit -m "first commit" - создает коммит с сообщением (флаг -m) "first commit"

git remote add origin https://github.com/semyonlinkov/git-practice.git 
    - казаные ссылки на удаленный репозиторий под названием origin
git push -u origin main - пушим файлы на удаленный репозиторий origin в ветку main

//! Комманды для инициализированного проекта
git add .
git commit -m "new commit"
git push

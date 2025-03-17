//! Начальные настройки
git init - инициализация локального репозитория

git config --global user.email "you@example.com" - указываем нашу почту в конфиге
git config --global user.name "Your Name" - указываем в конфиге имя

git branch -M main - переименовывает master ветку на main

//! Первый push
git add . - меняет статус файлов на Staged
git commit -m "first commit" - создает коммит с сообщением (флаг -m) "first commit"

git remote add origin https://github.com/semyonlinkov/git-practice.git 
    - указание ссылки на удаленный репозиторий под названием origin
git push -u origin main - пушим файлы на удаленный репозиторий origin в ветку main

//! Комманды пуша для уже инициализированного проекта
git add .
git commit -m "new commit"
git push

//! Клонирование репозитория
git clone https://github.com/semyonlinkov/git-practice

//! 
git status - показывает статус файлов в репозитории

//! создание алиасов в файле .gitconfig
[alias]
    s = status --short
    l = log --oneline --graph --decorate --all
    g = log --graph --abbrev-commit --decorate --all --format=format:'%C(bold blue)%h%C(reset) - %C(bold cyan)%aD%C(dim white) - %an%C(reset) %C(bold green)(%ar)%C(reset)%C(bold yellow)%d%C(reset)%n %C(white)%s%C(reset)'
    br = branch
    co = checkout

//! откат изменений 
git checkout -- index.html - до последнего коммита

git add index.html - добавить файл в промежуточный этап (staged) до коммита
git restore --staged index.html - убрать файл из промежуточного (unstage) этапа удалив изменения
git reset index.html - убрать файл из промежуточного (unstage) этапа без удаления изменений
git reset --hard HEAD^1 - откатыват на 1 коммит назад и удаляет его
git reset --soft HEAD^1 - откатыват на 1 коммит назад и удаляет его, но не удаляет изменения в файлах

//! Работа с ветками
git branch - позволяет посмотреть текущую ветку
git branch - v - тоже но с доп инфой по кол-ву коммитов

git branch develop - создает ветку develop
git checkout develop - переход на ветку develop
git checkout -b develop - создает и переходит на ветку

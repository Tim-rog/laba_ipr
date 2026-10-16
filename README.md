Не знаю
Я буду в маи через 25 минут +-
Скажите че гусь рассказывал
Про докер хрень какую-то
На лабах поймем

Kish Mishe
Photo
Это че за хуйня
Makar Shelyag
Это че за хуйня
Все темы которые мы прошли по матану и дискре
Ну тут без самых последних по матану по моему
md
task.md
13 KB
Makar Shelyag
task.md
Само напишется
Администрация вполне доходчиво намекнула, что завтра скипать не вариант
А так хотелось болт положить если честно
Makar Shelyag
Администрация вполне доходчиво намекнула, что завтра скипать не вариант
очень доходчиво
Вы съебали?
Макар
Тебя без паспорта пустили?
С паспортом
Makar Shelyag
С паспортом
Не забыл всё таки
Так я написал
Же ж
Не увидел
Никто не расходится
После лекции старосты собирают списки присутствующих на лекции и сдают мне
Да они Заебли
ахахаххах
интересно же почему
Не не
Это про другое
Про то как к Крылову ходили
Как я понял
а бля да
проебался

Лабораторная работа №1: Расширенные возможности ветвления в Git
Задание 1
git commit 
git tag v1.0
git commit 
git tag v1.1
git branch feat-auth
git checkout feat-auth
git commit 
git tag MR-123
git commit
git checkout main
git commit 
git tag hotfix
git merge --no-ff feat-auth 
git tag MR-merged
git commit 
git tag v1.2
git commit — Создает коммит в ветке main
git tag v1.0 — Создает тег v1.0 на текущем коммите
То же самое и повторяется с тегом v1.1
(По аналогии будет и дальше)

git branch feat-auth — Создает новую ветку feat-auth
git checkout feat-auth — Переключается на ветку feat-auth. Все последующие изменения сохраняются в ней
Далее создаются коммиты и тэги по аналогии
git checkout main — Возвращает рабочую область на основную ветку main
Далее создаются коммиты и тэги по аналогии
git merge --no-ff feat-auth — Выполняет слияние ветки feat-auth в текущую ветку (`main`). Флаг --no-ff (no fast-forward) принудительно создает специальный коммит слияния, сохраняя историю ветвления
Далее создаются коммиты и тэги по аналогии
Граф репозитория 1:

gitGraph
    commit tag:"v1.0"
    commit tag:"v1.1"
    branch feat-auth
    checkout feat-auth
    commit tag:"MR-123"
    commit
    checkout main
    commit tag:"hotfix"
    merge feat-auth tag:"MR-merged"
    commit tag:"v1.2"
Задание 2
git commit 
git tag v1.0
git commit 
git tag v1.1
git branch develop
git checkout develop
git commit
git commit
git checkout main 
git commit 
git tag v1.1.1
git checkout develop
git commit
git checkout main
git branch hotfix-critical
git checkout hotfix-critical
git commit 
git tag MR-456
git commit
git checkout main 
git commit 
git tag v1.1.2
git merge --no-ff hotfix-critical 
git tag MR-merged
git commit — Создает коммит в ветке main
git tag v1.0 — Создает тег v1.0 на текущем коммите
То же самое и повторяется с тегом v1.1
git branch develop — Создает ветку develop на текущем коммите
git checkout develop — Переключает рабочую область на ветку develop
Создаются коммиты в ветке develop
git checkout main — Возвращает активное окружение на главную ветку main
Создается коммит и тэг в main
git checkout develop — Возвращает к ветке разработки develop
Создается коммит
git checkout main — Переключает рабочую ветку обратно на main.
git branch hotfix-critical — Создает отдельную ветку hotfix-critical под критическую проблему
git checkout hotfix-critical — Переключается на созданную ветку хотфикса
По аналогии создаются коммиты и тэги
Переключаемся в ветку main, создаем коммит и тэг для него
git merge --no-ff hotfix-critical — Сливает ветку hotfix-critical в main с флагом --no-ff. Это принудительно создает коммит слияния (merge commit), сохраняя историю ветвления
Даем тег мерджу
Граф репозитория 2:

gitGraph
    commit tag:"v1.0"
    commit tag:"v1.1"
    branch develop
    checkout develop
    commit
    commit
    checkout main 
    commit tag:"v1.1.1"
    checkout develop
    commit
    checkout main
    branch hotfix-critical
    checkout hotfix-critical
    commit tag:"MR-456"
    commit
    checkout main 
    commit tag:"v1.1.2"
    merge hotfix-critical tag:"MR-merged"
Задание 3
git commit 
git tag v1.0
git branch feature-usermgmt
git checkout feature-usermgmt
git commit
git commit
git branch release-v2
git checkout release-v2
git commit 
git tag MR-789
git checkout main
git commit 
git tag v1.0.1
git checkout feature-usermgmt
git commit
git checkout release-v2
git commit
git checkout main 
git merge --no-ff release-v2 
git tag MR-merged
git commit 
git tag v2.0
git commit — Создает коммит в ветке main
git tag v1.0 — Создает тег v1.0 на текущем коммите
git branch feature-usermgmt — Создает ветку feature-usermgmt
git checkout feature-usermgmt — Переключает рабочую область на новую ветку
Создаем коммиты по аналогии
git branch release-v2 — Создает отдельную релизную ветку release-v2 на базе состояния ветки feature-usermgmt
git checkout release-v2 — Переходит на созданную ветку
Создаем коммиты и тэги по аналогии
git checkout main — Переключается обратно в главную ветку main
Создаем коммиты и тэги по аналогии
git checkout feature-usermgmt — Переключается на ветку feature-usermgmt
Создаем коммит
git checkout release-v2 — Переходит на ветку release-v2
сСоздаем коммит
git checkout main — Переключает рабочую среду на главную ветку main
git merge release-v2 — Сливает ветку release-v2 в main с флагом --no-ff. Это принудительно создает коммит слияния (merge commit), сохраняя историю ветвления
Создаем тэги и коммиты по аналогии
Граф репозитория 3:

gitGraph
    commit tag: "v1.0"
    branch feature-usermgmt
    checkout feature-usermgmt
    commit
    commit
    branch release-v2
    checkout release-v2
    commit tag: "MR-789"
    checkout main
    commit tag: "v1.0.1"
    checkout feature-usermgmt
    commit
    checkout release-v2
    commit
    checkout main 
    merge release-v2 tag:"MR-merged"
    commit tag:"v2.0"
Задание 4
git commit 
git tag init
git commit 
git tag setup
git branch feature-payment
git checkout feature-payment
git commit 
git tag MR-101
git branch feature-stripe 
git checkout feature-stripe
git commit 
git checkout feature-payment
git commit 
git checkout main 
git commit 
git tag integration-fix
git checkout feature-stripe
git commit
git checkout feature-payment
git merge --no-ff feature-stripe 
git tag subfeature-merged
git commit
git checkout main 
git merge --no-ff feature-payment 
git tag MR-merged
Создаем тэги и коммиты по аналогии в ветке main
git branch feature-payment — Создает ветку feature-payment
git checkout feature-payment — Переключается на ветку feature-payment
Создаются коммиты и тэги по аналогии
git checkout feature-stripe — Переключается на ветку feature-stripe
оздаем коммит
git checkout feature-payment — Возвращается в родительскую фича-ветку
Создаем коммит
git checkout main — Переключается в ветку main
Создаем коммиты и тэги по аналогии
git checkout feature-stripe — Переключается обратно в ветку feature-stripe
Создаем коммит
git checkout feature-payment — Переключается на ветку feature-payment
git merge --no-ff feature-stripe — Выполняет слияние ветки feature-stripe с явным коммитом слияния
Создаем коммиты и тэги по аналогии
git checkout main — Переключается в главную ветку main
git merge --no-ff feature-payment — Выполняет слияние ветки feature-payment в main с сохранением истории ветвления
Стаивтся тэг мерджа
Граф репозитория 4:

gitGraph
    commit tag:"init"
    commit tag:"setup"
    branch feature-payment
    checkout feature-payment
    commit tag:"MR-101"
    branch feature-stripe 
    checkout feature-stripe
    commit 
    checkout feature-payment
    commit 
    checkout main 
    commit tag:"integration-fix"
    checkout feature-stripe
    commit
    checkout feature-payment
    merge feature-stripe tag:"subfeature-merged"
    commit
    checkout main 
    merge feature-payment tag:"MR-merged"
Задание 5
git commit 
git tag base
git commit 
git tag core
git branch feature-ui
git checkout feature-ui
git commit 
git tag MR-202
git branch feature-api
git checkout feature-api
git commit
git checkout feature-ui
git commit 
git checkout main
git commit 
git tag shared-update
git checkout feature-api
git commit 
git checkout feature-ui
git commit
git checkout main
git merge --no-ff feature-ui 
git tag MR-merged
git commit
git merge --no-ff feature-api 
git tag MR-merged
Создаются коммиты и тэги по аналогии в ветке main
git branch feature-ui — Создает ветку feature-ui
git checkout feature-ui — Переключается на ветку feature-ui
Создаются тэги и коммиты по аналогии
git branch feature-api — Создает ветку feature-api на основе текущего состояния feature-ui
git checkout feature-api — Переключается на ветку feature-api
Создаем коммит
git checkout feature-ui — Возвращается в ветку feature-ui
Создает коммит
git checkout main — Переключается в ветку main
Создает тэги и коммиты по аналогии
git checkout feature-api — Переключается на ветку feature-api
Создает коммит
git checkout feature-ui — Переключается на ветку feature-ui
Создает коммит
git checkout main — Переключается в ветку main.
git merge --no-ff feature-ui — Выполняет слияние ветки UI с явным коммитом слияния
Создаются коммиты и тэги
git merge --no-ff feature-api — Выполняет слияние ветки API в обновленную ветку main
Создается тэг мерджа
Граф репозитория 5:

gitGraph
    commit tag:"base"
    commit tag:"core"
    branch feature-ui
    checkout feature-ui
    commit tag:"MR-202"
    branch feature-api
    checkout feature-api
    commit
    checkout feature-ui
    commit 
    checkout main
    commit tag:"shared-update"
    checkout feature-api
    commit 
    checkout feature-ui
    commit
    checkout main
    merge feature-ui tag:"MR-merged"
    commit
    merge feature-api tag:"MR-merged"
Выводы и трудности
Тк ранее имел опыт работы с Git, то особых трудностей в выполнении лабораторной работы не возникло

Однако можно выделить несколько интересных/необычных моментов:

1.
Впервые столкнулся с форматом mermaid. Стиль написания графа гит отличается от стиля написания команд в bash
2.
Впервые услышал про ff (fast forward)  и его отличия от обычного мерджа
3.
На самой лабораторке узнал про то, что бывает, если сразу не написать message в комите (привет, вим)
4.
Узнал про HEAD
В результате выполнения лаборатнорной работы вспомнил и попрактиковался в работе с гитом, узнал несколько новых моментов (писал выше)
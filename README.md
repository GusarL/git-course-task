# Удаление ненужных коммитов
Придумать как можно удалить все коммиты из истории кроме трех последних


# Expected result:
- Публичный репозиторий
- Склоненный с репозитория https://github.com/MaksymSemenykhin/git-course-task/tree/task%231
- В истории комитов только три коммита(последние в оригинальной репе)
- В README файле описано как именно был произведен откат(Схема, описание или скрипт)
- Правки README файла могут быть 4м коммитом

# Описание действий для удаления коммита (тот самы 4 коммит)
- git clone https://github.com/MaksymSemenykhin/git-course-task.git
- git remote set-url origin https://github.com/GusarL/git-course-task.git
- git checkout task#1
- git log --pretty=oneline --abbrev-commit
- git rebase -i --root
- dd на строчках с ненужными коммитами
- :wq
- nano README.md для решения конфликта
- ^x для сохраннения изменений
- git add README.md
- git rebase --continue
- esc

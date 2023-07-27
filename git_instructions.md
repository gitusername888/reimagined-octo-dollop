# # ---Основные команды Git---

*Введение в контроль версий. Работа с Git. Составление инструкции по работе с Git.*

✦ git init – инициализация локального репозитория

✦ git status – получить информацию от git о его текущем состоянии

✦ git add – добавить файл или файлы к следующему коммиту

✦ git commit -m “message” – создание коммита.

✦ git log – вывод на экран истории всех коммитов с их хеш-кодами.
--graph Добавить визуализацию веток.

✦ git checkout – переход от одного коммита к другому

✦ git checkout master – вернуться к актуальному состоянию и продолжить работу

✦ git diff – увидеть разницу между текущим файлом и закоммиченным файлом

✦ git --global user.name "__" – один раз нужно представиться и ввести почту.

✦ file -- avtosave  полезно включить автосохранение.

✦ git branch выводит информацию от ветках изменеий. если ввести название, то создается новая ветка.

✦ git rm --cached Screenshot_2.png  Удаляет фалйл из комита.

    -n                    do not show a diffstat at the end of the merge
    --stat                show a diffstat at the end of the merge
    --summary             (synonym to --stat)
    --log[=<n>]           add (at most <n>) entries from shortlog to merge commit message
    --squash              create a single commit instead of doing a merge
    --commit              perform a commit if the merge succeeds (default)
    -e, --edit            edit message before committing
    --cleanup <mode>      how to strip spaces and #comments from message
    --ff                  allow fast-forward (default)
    --ff-only             abort if fast-forward is not possible
    --rerere-autoupdate   update the index with reused conflict resolution if possible
    --verify-signatures   verify that the named commit has a valid GPG signature
    -s, --strategy <strategy>
                          merge strategy to use
    -X, --strategy-option <option=value>
                          option for selected merge strategy
    -m, --message <message>
                          merge commit message (for a non-fast-forward merge)
    -F, --file <path>     read message from file
    --into-name <name>    use <name> instead of the real target
    -v, --verbose         be more verbose
    -q, --quiet           be more quiet
    --abort               abort the current in-progress merge
    --quit                --abort but leave index and working tree alone
    --continue            continue the current in-progress merge
    --allow-unrelated-histories
                          allow merging unrelated histories
    --progress            force progress reporting
    -S, --gpg-sign[=<key-id>]
                          GPG sign commit
    --autostash           automatically stash/stash pop before and after
    --overwrite-ignore    update ignored files (default)
    --signoff             add a Signed-off-by trailer
    --no-verify           bypass pre-merge-commit and commit-msg hooks

   
✦ cherry-pick

git cherry-pick [--edit] [-n] [-m <parent-number>] [-s] [-x] [--ff]
 [-S[<keyid>]] <commit>…​
git cherry-pick (--continue | --skip | --abort | --quit)

Учитывая один или несколько существующих коммитов, примените изменения, вносимые каждым из них, записывая новый коммит для каждого. Для этого ваше рабочее дерево должно быть чистым (никаких изменений из головного коммита).

Когда не очевидно, как применить изменение, происходит следующее:

Текущая ветвь и HEAD указатель остаются на последней успешно выполненной фиксации.

CHERRY_PICK_HEADСсылка устанавливается так, чтобы указывать на фиксацию, которая внесла изменение, которое трудно применить.

Пути, в которых изменения были применены чисто, обновляются как в индексном файле, так и в вашем рабочем дереве.

Для конфликтующих путей индексный файл записывает до трех версий, как описано в разделе "ИСТИННОЕ СЛИЯНИЕ" git-merge[1]. Файлы рабочего дерева будут включать описание конфликта, заключенное в квадратные скобки обычными маркерами конфликта <<<<<<< и >>>>>>>.

Никаких других изменений не внесено.

Смотрите git-merge[1] некоторые подсказки по разрешению таких конфликтов приведены в разделе.

https://git-scm.com/docs/git-cherry-pick

✦ reset

✦ revert

✦ rebase


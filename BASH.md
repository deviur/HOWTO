# BASH
## HOWTO: СОЗДАТЬ ЗАГРУЗОЧНУЮ ФЛЭШКУ С UBUNTU
1. `sudo dd if=ubuntu-mate.iso of=/dev/sdb` - пример dd команды записи iso-образа на флешку
2. `sync` - обязательно выполнять эту команду после завершения работы команды dd
3. `sudo kill -USR1 $(pgrep ^dd)` - выводит промежуточные результаты выполнения команды dd (сколько уже скопировано и с какой средней скоростью
4. `watch -n5 'sudo kill -USR1 $(pgrep ^dd)'` - выводит промежуточные результаты регулярно, через каждые -n5 секунд
## HOWTO: НАЙТИ ПОХОЖИЕ ИЗОБРАЖЕНИЯ
```shell
findimagedupes -R -t=90 -i 'VIEW(){ for f in "$@";do echo \"$f\"; done; echo "---"; }'  -- * > dupes.txt
```
[see more detail](http://www.jhnc.org/findimagedupes/manpage.html#EXAMPLES)

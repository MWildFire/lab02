## Laboratory work II

Данная лабораторная работа посвещена изучению утилит для разработки проектов

## Tasks

- [X] 1. Ознакомиться со ссылками учебного материала
- [X] 2. Выполнить инструкцию учебного материала
- [X] 3. Составить отчет и отправить ссылку личным сообщением в **Slack**
 
## Tutorial

```bash
$ export GITHUB_USERNAME=<имя_пользователя> //создание переменных
$ export GIST_TOKEN=<сохраненный_токен>
$ alias edit=<nano|vi|vim|subl> //выбор текстового редактора
```

```ShellSession
$ mkdir -p ${GITHUB_USERNAME}/workspace //создание директории
$ cd ${GITHUB_USERNAME}/workspace //переход в директорию
$ pwd //вывод рабочего каталога
$ cd ..
$ pwd
```

```ShellSession
$ mkdir -p workspace/tasks/ //создание директорий
$ mkdir -p workspace/projects/
$ mkdir -p workspace/reports/
$ cd workspace
```

```ShellSession
# Debian
$ wget https://nodejs.org/dist/v6.11.5/node-v6.11.5-linux-x64.tar.xz
$ tar -xf node-v6.11.5-linux-x64.tar.xz
$ rm -rf node-v6.11.5-linux-x64.tar.xz
$ mv node-v6.11.5-linux-x64 node
```

```ShellSession
$ ls node/bin 
$ echo ${PATH}
$ export PATH=${PATH}:`pwd`/node/bin
$ echo ${PATH}
$ mkdir scripts
$ cat > scripts/activate<<EOF
export PATH=\${PATH}:`pwd`/node/bin
EOF
$ source scripts/activate
```

```ShellSession
$ npm install -g gistup //установка gistup
$ ls node/bin
```

```ShellSession
$ cat > ~/.gistup.json <<EOF //сохранение токена в файл
{
  "token": "${GIST_TOKEN}"
}
EOF
```

## Report

```ShellSession
$ export LAB_NUMBER=02
$ git clone https://github.com/tp-labs/lab${LAB_NUMBER} tasks/lab${LAB_NUMBER}
$ mkdir reports/lab${LAB_NUMBER}
$ cp tasks/lab${LAB_NUMBER}/README.md reports/lab${LAB_NUMBER}/REPORT.md
$ cd reports/lab${LAB_NUMBER}
$ edit REPORT.md
$ gistup -m "lab${LAB_NUMBER}"
```

## Links

### Unix commands

- [ar](https://en.wikipedia.org/wiki/Ar_(Unix)) //архиватор
- [cat](https://en.wikipedia.org/wiki/Cat_(Unix)) //считывает файлов и записывает их в стандартный вывод
- [cd](https://en.wikipedia.org/wiki/Cd_(command)) //переход в предыдющую директорию
- [cp](https://en.wikipedia.org/wiki/Cp_(Unix)) //копирование файла
- [cut](https://en.wikipedia.org/wiki/Cut_(Unix)) //выбор нужной части в каждой строке
- [echo](https://en.wikipedia.org/wiki/Echo_(command)) //вывести строку в терминал
- [env](https://en.wikipedia.org/wiki/Env_(shell)) //работа с переменными (удаление, добавление, переназначение)
- [ex](https://en.wikipedia.org/wiki/Ex_(editor)) //редактор строк
- [file](https://en.wikipedia.org/wiki/File_(command)) //распознование типов данных
- [find](https://en.wikipedia.org/wiki/Find) //найти файлы и директории
- [ls](https://en.wikipedia.org/wiki/Ls) //отобразить содержимое текущей директории
- [man](https://en.wikipedia.org/wiki/Man_page) //форматирование и вывод справочных страниц
- [mkdir](https://en.wikipedia.org/wiki/Mkdir) //создать директорию
- [mv](https://en.wikipedia.org/wiki/Mv) //перемещение файла(ов) из одного места в другое
- [nm](https://en.wikipedia.org/wiki/Nm_(Unix)) //просмотр и отображение содержимого в бинарных файлах
- [ps](https://en.wikipedia.org/wiki/Ps_(Unix)) //вывод текущие активные процессы
- [pwd](https://en.wikipedia.org/wiki/Pwd) //(рабочий каталог печати) запись имени рабочего каталога в ст вывод
- [rm](https://en.wikipedia.org/wiki/Rm_(Unix)) //удаление файлов, директорий и тд
- [sed](https://en.wikipedia.org/wiki/Sed) //редактирование текста
- [touch](https://en.wikipedia.org/wiki/Touch_(Unix)) //обновление дат, связанных с файлом, или каталогом

### Package Managers

- [apt](http://help.ubuntu.ru/wiki/apt) | [dnf](https://en.wikipedia.org/wiki/DNF_(software)) | [yum](https://fedoraproject.org/wiki/Yum/ru)
- [brew](https://brew.sh) | [linuxbrew](http://linuxbrew.sh)
- [npm](https://docs.npmjs.com)

### Software

- [curl](https://www.gitbook.com/book/bagder/everything-curl/details)
- [wget](https://www.gnu.org/software/wget/manual/wget.pdf)
- [clang](https://clang.llvm.org)
- [g++](https://gcc.gnu.org/onlinedocs/gcc-4.0.2/gcc/G_002b_002b-and-GCC.html)
- [make](https://en.wikipedia.org/wiki/Make_(software))
- [open](https://developer.apple.com/legacy/library/documentation/Darwin/Reference/ManPages/man1/open.1.html)
- [openssl](https://www.openssl.org)
- [nano](https://www.nano-editor.org)
- [tree](https://linux.die.net/man/1/tree)
- [vim](http://www.vim.org)

```
Copyright (c) 2017 Братья Вершинины
```

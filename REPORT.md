dts@dts-HP-Pavilion-Notebook:~$ export GITHUB_USERNAME=SpectreNutz
dts@dts-HP-Pavilion-Notebook:~$ export GITHUB_EMAIL=dmitriy15091978@gmail.com
dts@dts-HP-Pavilion-Notebook:~$ export GITHUB_TOKEN=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
dts@dts-HP-Pavilion-Notebook:~$ alias edit=nano
dts@dts-HP-Pavilion-Notebook:~$ cd ${GITHUB_USERNAME}/workspace
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace$ source scripts/activate
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace$ mkdir ~/.config
mkdir: невозможно создать каталог «/home/dts/.config»: Файл существует
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace$ cat > ~/.config/hub <<EOF
> github.com:
> - user: ${GITHUB_USERNAME}
> oauth_token: ${GITHUB_TOKEN}
> protocol: https
> EOF
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace$ git config --global hub.protocol https
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace$ mkdir projects/lab02 && cd projects/lab02
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace/projects/lab02$ git init
подсказка: Using 'master' as the name for the initial branch. This default branch name
подсказка: is subject to change. To configure the initial branch name to use in all
подсказка: of your new repositories, which will suppress this warning, call:
подсказка: 
подсказка: 	git config --global init.defaultBranch <name>
подсказка: 
подсказка: Names commonly chosen instead of 'master' are 'main', 'trunk' and
подсказка: 'development'. The just-created branch can be renamed via this command:
подсказка: 
подсказка: 	git branch -m <name>
Инициализирован пустой репозиторий Git в /home/dts/SpectreNutz/workspace/projects/lab02/.git/
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace/projects/lab02$ git config --global user.name ${GITHUB_USERNAME}
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace/projects/lab02$ git config --global user.email ${GITHUB_EMAIL}
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace/projects/lab02$ git config -e --global
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace/projects/lab02$ git remote add origin https://github.com/${GITHUB_USERNAME}/lab02.git
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace/projects/lab02$ git pull origin master
fatal: couldn't find remote ref master
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace/projects/lab02$ ls
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace/projects/lab02$ git pull origin master
fatal: couldn't find remote ref master
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace/projects/lab02$ git ls-remote --heads origin
93674445bd3e30d1c36111876afbcd549e09f1db	refs/heads/main
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace/projects/lab02$ git pull origin main
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Распаковка объектов: 100% (3/3), 1.44 КиБ | 245.00 КиБ/с, готово.
Из https://github.com/SpectreNutz/lab02
 * branch            main       -> FETCH_HEAD
 * [новая ветка]     main       -> origin/main
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace/projects/lab02$ touch README.md
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace/projects/lab02$ git status
Текущая ветка: master
Неотслеживаемые файлы:
  (используйте «git add <файл>...», чтобы добавить в то, что будет включено в коммит)
	README.md

индекс пуст, но есть неотслеживаемые файлы
(используйте «git add», чтобы проиндексировать их)
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace/projects/lab02$ git add README.md
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace/projects/lab02$ git commit -m"added README.md"
[master 44dae32] added README.md
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 README.md
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace/projects/lab02$ git push origin master
Username for 'https://github.com': 
Password for 'https://github.com': 
remote: No anonymous write access.
fatal: Authentication failed for 'https://github.com/SpectreNutz/lab02.git/'
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace/projects/lab02$ git push origin main
error: src refspec main ничему не соответствует
error: не удалось отправить некоторые ссылки в «https://github.com/SpectreNutz/lab02.git»
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace/projects/lab02$ git push origin master
Username for 'https://github.com': SpectreNutz
Password for 'https://SpectreNutz@github.com': 
Перечисление объектов: 4, готово.
Подсчет объектов: 100% (4/4), готово.
При сжатии изменений используется до 4 потоков
Сжатие объектов: 100% (2/2), готово.
Запись объектов: 100% (3/3), 285 байтов | 95.00 КиБ/с, готово.
Всего 3 (изменений 0), повторно использовано 0 (изменений 0), повторно использовано пакетов 0
remote: 
remote: Create a pull request for 'master' on GitHub by visiting:
remote:      https://github.com/SpectreNutz/lab02/pull/new/master
remote: 
To https://github.com/SpectreNutz/lab02.git
 * [new branch]      master -> master
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace/projects/lab02$ git pull origin master
Из https://github.com/SpectreNutz/lab02
 * branch            master     -> FETCH_HEAD
Уже актуально.
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace/projects/lab02$ git log
commit 44dae326b188d61105b7abe11c7006bc4eaeda9b (HEAD -> master, origin/master)
Author: SpectreNutz <dmitriy15091978@gmail.com>
Date:   Wed May 28 22:21:41 2025 +0300

    added README.md

commit 93674445bd3e30d1c36111876afbcd549e09f1db (origin/main)
Author: SpectreNutz <dmitriy15091978@gmail.com>
Date:   Wed May 28 22:16:17 2025 +0300

    Initial commit
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace/projects/lab02$ mkdir sources
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace/projects/lab02$ mkdir include
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace/projects/lab02$ mkdir examples
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace/projects/lab02$ cat > sources/print.cpp <<EOF
> #include <print.hpp>
> 
> void print(const std::string& text, std::ostream& out)
> {
>   out << text;
> }
> EOF
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace/projects/lab02$ cat > sources/print.cpp <<EOF
#include <print.hpp>

void print(const std::string& text, std::ostream& out)
{
  out << text;
}
EOF
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace/projects/lab02$ cat > sources/print.cpp <<EOF
#include <print.hpp>

void print(const std::string& text, std::ostream& out)
{
  out << text;
}
EOF
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace/projects/lab02$ cat > sources/print.cpp <<EOF
#include <print.hpp>

void print(const std::string& text, std::ostream& out)
{
  out << text;
}
> 
> EOF
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace/projects/lab02$ cat > sources/print.cpp <<EOF
> #include <print.hpp>
> 
> void print(const std::string& text, std::ostream& out)
> {
>   out << text;
> }
> 
> void print(const std::string& text, std::ofstream& out)
> {
>   out << text;
> }
> EOF
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace/projects/lab02$ cat > include/print.hpp <<EOF
> #include <fstream>
> #include <iostream>
> #include <string>
> 
> void print(const std::string& text, std::ofstream& out);
> void print(const std::string& text, std::ostream& out = std::cout);
> EOF
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace/projects/lab02$ cat > examples/example1.cpp <<EOF
> #include <print.hpp>
> 
> int main(int argc, char** argv)
> {
>   print("hello");
> }
> EOF
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace/projects/lab02$ cat > examples/example2.cpp <<EOF
> #include <print.hpp>
> 
> #include <fstream>
> 
> int main(int argc, char** argv)
{
  std::ofstream file("log.txt");
  print(std::string("hello"), file);
}
> EOF
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace/projects/lab02$ edit README.md
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace/projects/lab02$ git status
Текущая ветка: master
Неотслеживаемые файлы:
  (используйте «git add <файл>...», чтобы добавить в то, что будет включено в коммит)
	examples/
	include/
	sources/

индекс пуст, но есть неотслеживаемые файлы
(используйте «git add», чтобы проиндексировать их)
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace/projects/lab02$ git add .
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace/projects/lab02$ git commit -m"added sources"
[master 2059ca4] added sources
 4 files changed, 33 insertions(+)
 create mode 100644 examples/example1.cpp
 create mode 100644 examples/example2.cpp
 create mode 100644 include/print.hpp
 create mode 100644 sources/print.cpp
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace/projects/lab02$ git push origin master
Username for 'https://github.com': SpectreNutz
Password for 'https://SpectreNutz@github.com': 
Перечисление объектов: 10, готово.
Подсчет объектов: 100% (10/10), готово.
При сжатии изменений используется до 4 потоков
Сжатие объектов: 100% (7/7), готово.
Запись объектов: 100% (9/9), 937 байтов | 66.00 КиБ/с, готово.
Всего 9 (изменений 0), повторно использовано 0 (изменений 0), повторно использовано пакетов 0
To https://github.com/SpectreNutz/lab02.git
   44dae32..2059ca4  master -> master
dts@dts-HP-Pavilion-Notebook:~$ cd ~ SpecteNutz/workspace
bash: cd: слишком много аргументов
dts@dts-HP-Pavilion-Notebook:~$ cd ~/SpecteNutz/workspace
bash: cd: /home/dts/SpecteNutz/workspace: Нет такого файла или каталога
dts@dts-HP-Pavilion-Notebook:~$ ls
 boost_1_69_0   boost-libs   ligma   snap   SpectreNutz   Видео   Документы   Загрузки   Изображения   Музыка   Общедоступные   Прога  'Рабочий стол'   Шаблоны
dts@dts-HP-Pavilion-Notebook:~$ cd ~/SpectreNutz/workspace
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace$ export LAB_NUMBER=02
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace$ git clone https://github.com/tp-labs/lab${LAB_NUMBER}.git tasks/lab${LAB_NUMBER}
Клонирование в «tasks/lab02»...
remote: Enumerating objects: 96, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 96 (delta 0), reused 1 (delta 0), pack-reused 93 (from 1)
Получение объектов: 100% (96/96), 1.29 МиБ | 1.50 МиБ/с, готово.
Определение изменений: 100% (28/28), готово.
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace$ mkdir reports/lab${LAB_NUMBER}
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace$ cp tasks/lab${LAB_NUMBER}/README.md reports/lab${LAB_NUMBER}/REPORT.md
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace$ cd reports/lab${LAB_NUMBER}
dts@dts-HP-Pavilion-Notebook:~/SpectreNutz/workspace/reports/lab02$ edit REPORT.md


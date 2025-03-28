# GIT <img src="./assets/git-icon-logo-svgrepo-com.svg" width="40" height="40" alt="GIT logo"/>

Вітаю! ✨
Цей репозиторій містить вичерпний конспект, який я створила під час проходження курсу Нікіти Тимошенка про [Git та GitHub](https://www.youtube.com/watch?v=9CnZihyYjjA&list=WL&index=2&t=1s)

📌 Конспект у форматі питання-відповіді, щоб ви могли перевірити себе та швидко знаходити потрібну інформацію.

📌 Структура наближена до курсу, тож вам буде легко орієнтуватися в темах і знаходити потрібний матеріал.

📌 Раджу пройти сам [курс](https://www.youtube.com/watch?v=9CnZihyYjjA&list=WL&index=2&t=1s) та прочитати [конспект від Нікіти](https://github.com/NickTimosh/git_course/tree/main/notebooks) адже там багато корисного:

-   детальний опис команд,
-   практичні завдання,
-   корисні посилання.

✨ А цей конспект допоможе вам перевірити, наскільки добре ви засвоїли отримані знання! 🚀

Якщо є якісь зауваження, або пропозиції для покращення не соромтесь створювати issues або pull requests. Я відкрита до зворотного зв'язку 🙌

Легкого навчання!😊

---

<h2>Зміст</h2>

<details>
    <summary>Командний рядок</summary>
    <ul>
        <li><a href="#command-line-terms">Командний рядок — терміни</a></li>
        <li><a href="#files-system-terms">Файлова система — терміни</a></li>
        <li><a href="#path-to-files">Шлях до файлів</a></li>
        <li><a href="#read-folder-content">Читання вмісту папок(команди)</a></li>
        <li><a href="#interaction-with-folders">Взаємодія з папками(команди)</a></li>
        <li><a href="#interaction-with-files">Взаємодія з файлами(команди)</a></li>
    </ul>
</details>

<details>
  <summary>Git</summary>
  <ul>
    <li><a href="#git-overview">Короткий огляд</a></li>
    <li><a href="#git-config">Основні налаштування</a></li>
    <li><a href="#git-main-theory">Теорія, основні концепції</a></li>
    <li><a href="#git-main-commands">Основні команди</a></li>
    <li><a href="#git-extensions-basics">Розширення основ</a></li>
    <li><a href="#git-recovery-version">Вступ до відновлення версій</a></li>
    <li><a href="#git-branches">Вступ в git branch</a></li>
  </ul>
</details>

<details>
  <summary>GitHub</summary>
  <ul>
    <li><a href="#github-concept">Основні концепції</a></li>
    <li><a href="#github-first-repo">Перший репозиторій</a></li>
    <li><a href="#github-gitignore">Файл .gitignore</a></li>
    <li><a href="#github-watch-fork-stars">Watch, fork & stars</a></li>
    <li><a href="#github-fork">Копіювання репозиторію (Fork)</a></li>
    <li><a href="#github-pr">Створення Pull Requests (PR)</a></li>
    <li><a href="#github-issues">Створення Issues (задач)</a></li>
    <li><a href="#github-workflow">Огляд типового workflow</a></li>
    <li><a href="#github-ssh-key">SSH-ключ</a></li>
    <li><a href="#github-push-local-repo">Push локального репозиторію</a></li>
    <li><a href="#github-brach-and-pull">Гілки та pull request</a></li>
    <li><a href="#github-clone-repo">Клонування репозиторію</a></li>
  </ul>
</details>

---

<h2>Комадний рядок</h2>

[Конспект](https://github.com/NickTimosh/git_course/blob/main/notebooks/1.%20%D0%92%D1%81%D1%82%D1%83%D0%BF%20%D0%B2%20%D0%9A%D0%BE%D0%BC%D0%B0%D0%BD%D0%B4%D0%BD%D0%B8%D0%B9%20%D0%A0%D1%8F%D0%B4%D0%BE%D0%BA.md)

<h3 id="command-line-terms">Командний рядок — терміни</h3>

<details>
<summary>Що таке GUI?</summary>

-   графічний інтерфейс користувача (Graphical User Interface)
    -   спосіб взаємодії користувача з комп'ютером із використанням графічних елементів (вікна, кнопки і тд)

</details>

<details>
<summary>Що таке Сommand Line?</summary>

-   командний рядок
    -   текстовий інтерфейс для взаємодії з операційною системою
    -   простір, де вводяться текстові команди
    -   і тут же можуть викликатися і запускатися певні програми

</details>

<details>
<summary>Що таке термінал?</summary>

-   програма або інструмент, який надає доступ до командного рядка (вікно, куди команди вводяться)

</details>

<details>
<summary>Що таке Shell?</summary>

-   оболонка
    -   програма, яка виконує команди, введені у терміналі (інтерпретатор команд)

</details>

<details>
<summary>Принцип роботи Shell (схема)</summary>

<img src="./assets//images/working-principale-shell.png" width="800" alt="Schematic of the principle of shell operation"/>

</details>

<details>
<summary>Що таке Bash?</summary>

-   один із типів оболонок (Shell)
-   Bourne Again Shell (Bash)
-   підтримується у Windows через Git Bash

</details>

<details>
<summary>Взаємодія з ОС (схема)</summary>

<img src="./assets//images/interaction-with-OS.png" width="800" alt="Diagram of the stages of interaction with the operating system"/>

</details>

---

<h3 id="files-system-terms">Файлова система — терміни</h3>

<details>
<summary>Що таке каталог (директорія)?</summary>

-   структура, яка використовується для організації файлів у файловій системі

</details>

<details>
<summary>Що таке поточний каталог?</summary>

-   папка, в якій користувач перебуває прямо зараз
    -   команди по замовчуванню виконуються у поточному каталозі

</details>

<details>
<summary>Що таке батьківський каталог?</summary>

-   папка, що знаходиться на один рівень вища, за поточний

</details>

<details>
<summary>Що таке домашній каталог?</summary>

-   персональний каталог користувача
    -   Диск С —> Users —> User name (або USER)

</details>

<details>
<summary>Що таке кореневий каталог?</summary>

-   початкова точка файлової системи
    -   найвищий рівень ієрархії каталогів

</details>

<details>
<summary>Структура каталогів (схема)</summary>

<img src="./assets//images/directions-structure.png" width="800" alt="Directory structure"/>

</details>

---

<h3 id="path-to-files">Шлях до файлів</h3>

<details>
<summary>Що таке шлях (path)?</summary>

-   адреси файлів у каталозі файлової системи

</details>

<details>
<summary>Які є два види шляхів до файлів?</summary>

-   абсолютний
-   відносний

</details>

<details>
<summary>Де починається абсолютний шях?</summary>

-   з кореневого каталогу

</details>

<details>
<summary>Що визначає відносний шях?</summary>

-   розташування файлу по відношенню до поточного каталогу

</details>

<details>
<summary>Що таке розширення файлів?</summary>

-   частина назви файлу, що йде після крапки

</details>

<details>
<summary>Для чого потрібне розширення файлів?</summary>

-   для визначення типу файлу

</details>

---

<h3 id="read-folder-content">Командний рядок — читання вмісту папок (команди)</h3>

[Конспект](https://github.com/NickTimosh/git_course/blob/main/notebooks/2.%20git%20bash%20-%20%D0%BA%D0%BE%D0%BC%D0%B0%D0%BD%D0%B4%D0%B8.md)

[Практичні завдання](https://github.com/NickTimosh/git_course/blob/main/notebooks/3.%20git%20bash%20-%20%D0%BF%D1%80%D0%B0%D0%BA%D1%82%D0%B8%D0%BA%D0%B0.md)

<details>
<summary>Яка команда відображає вміст всієї папки, у якій знаходиться користувач?</summary>

-   ls

</details>

<details>
<summary>Яка команда дозволяє відобразити вміст каталогу відмінного від поточного?</summary>

-   ls `path` (вказати шлях)

</details>

<details>
<summary>Які типи шляхів це дозволяють?</summary>

-   обидва: відносний та абсолютний

</details>

<details>
<summary>Яка команда дозволяє повернути вмісти кореневого каталогу?</summary>

-   ls /

</details>

<details>
<summary>Яка команда дозволяє повернути вмісти батьківського каталогу?</summary>

-   ls ..

</details>

<details>
<summary>Яка команда очищає вікно терміналу?</summary>

-   clear

</details>

<details>
<summary>Як у Git Bash навігувати по командам, що вже були написані?</summary>

-   стрілочка вгору (до попередніх команд)
-   стрілочка вниз (до наступних команд, що були після попередніх)

</details>

<details>
<summary>Що таке прапорці команд?</summary>

-   додаткові опції команд

</details>

<details>
<summary>Як впроваджуються прапорці команд?</summary>

-   через дефіси, які ми пишемо після команди

</details>

<details>
<summary>Який прапорець надає довідку?</summary>

-   `комадна` --help

</details>

<details>
<summary>Яка команда дозволяє повернути вміст всіх папок у довгому форматі (з прапорцем)?</summary>

-   ls -l

</details>

<details>
<summary>Як вивести дані, які повертає команда у вигляді текстового файлу?</summary>

-   `your_command` > file_name.extension

</details>

<details>
<summary>Яка команда дозволяє вивести вміст папок у вигляді текстового файлу?</summary>

-   ls > `file_name.extension`
    -   наприклад, ls > output.txt

</details>

<details>
<summary>Яка команда дозволяє вивести вміст папок у вигляді текстового файлу у довгому форматі?</summary>

-   ls -l > `file_name.extension`
    -   наприклад, ls -l > output.txt

</details>

---

<h3 id="interaction-with-folders">Командний рядок — взаємодія з папками (команди)</h3>

[Конспект](https://github.com/NickTimosh/git_course/blob/main/notebooks/2.%20git%20bash%20-%20%D0%BA%D0%BE%D0%BC%D0%B0%D0%BD%D0%B4%D0%B8.md)

[Практичні завдання](https://github.com/NickTimosh/git_course/blob/main/notebooks/3.%20git%20bash%20-%20%D0%BF%D1%80%D0%B0%D0%BA%D1%82%D0%B8%D0%BA%D0%B0.md)

<details>
<summary>Яка команда показує поточну директорію?</summary>

-   pwd
    -   prind working directory

</details>

<details>
<summary>Що повертає ця команда?</summary>

-   шлях до каталогу, у якому ми знаходимось

</details>

<details>
<summary>Яка команда дозволяє змінити поточну директорію на домашній каталог користувача?</summary>

-   cd
    -   change directory

</details>

<details>
<summary>Як змінити поточну директорію на якусь конкретну іншу?</summary>

-   cd `path` (вказати шлях)

</details>

<details>
<summary>Яка команда повертає до батьківської директорії?</summary>

-   cd ..

</details>

<details>
<summary>Яка команда створює нову папку?</summary>

-   mkdir `directory_name`
    -   make directory

</details>

<details>
<summary>Як створити одразу кілька папок у поточній директорії?</summary>

-   mkdir `directory_name_1` `directory_name_2`
-   якщо потрібні вкладені каталоги:
    -   mkdir -p dir1/dir2/dir3

</details>

<details>
<summary>Яка команда дозволяє скопіювати директорію до певної папки?</summary>

-   cp -r `copy_directory to_directory`

</details>

<details>
<summary>Яка команда дозволяє видалити директорію?</summary>

-   rm -r `file_name` (рекурсивне видалення)
-   якщо директорія містить файли:
    -   rm -rf directory_name

</details>

---

<h3 id="interaction-with-files">Командний рядок — взаємодія з файлами (команди)</h3>

[Конспект](https://github.com/NickTimosh/git_course/blob/main/notebooks/2.%20git%20bash%20-%20%D0%BA%D0%BE%D0%BC%D0%B0%D0%BD%D0%B4%D0%B8.md)

[Практичні завдання](https://github.com/NickTimosh/git_course/blob/main/notebooks/3.%20git%20bash%20-%20%D0%BF%D1%80%D0%B0%D0%BA%D1%82%D0%B8%D0%BA%D0%B0.md)

<details>
<summary>Яка команда створює файл?</summary>

-   touch `file_name.extension`

</details>

<details>
<summary>Як команда дозволяє скопіювати файл і перенести його до іншої папки?</summary>

-   cp `copy_file destination_directory/`
    -   copy

</details>

<details>
<summary>Яка команда дозволяє записати щось у файл?</summary>

-   echo `print_something` > `in_file`

</details>

<details>
<summary>Яка команда дозволяє повернути вміст файлу?</summary>

-   cat `file_name`

</details>

<details>
<summary>Яка команда дозволяє видалити файл?</summary>

-   rm `file_name`

</details>

---

<h2>Git</h2>

<h3 id="git-overview">Git — короткий огляд</h3>

<details>
<summary>Що таке Git?</summary>

-   програмне забезпечення
-   система контролю версій (VCS — version control system)
    -   відстежує зміни у файлах
    -   дає змогу повернутися до попередніх версій
    -   забезпечує зручну співпрацю команд

</details>

<details>
<summary>Що пропонує Git?</summary>

-   локальну базу даних
-   синхронізацію з іншими серверами
-   відновлення даних у разі збою

</details>

<details>
<summary>Які основні стани файлів у Git?</summary>

1. modified — файл змінено, але не додано до бази даних
2. staged — файл підготовлено до збереження
3. committed — зміни збережено у локальній базі даних

</details>

<details>
<summary>Основні стани файлів у Git (схема)</summary>

<img src="./assets//images/main-states-files.png" width="800" alt="Basic file states"/>

</details>

<details>
<summary>Що робить звичайну папку локальним репозиторієм?</summary>

-   папка .git

</details>

<details>
<summary>Яка команда ініціалізує репозиторій?</summary>

-   git init
    -   після цієї команди з'являється папка .git і наша папка стала репозиторієм

</details>

---

<h3 id="git-config">Git — налаштування</h3>

<details>
<summary>Як переконатися, що Git встановлено (яка команда)?</summary>

-   git --version

</details>

<details>
<summary>Яка команда дозволяє змінити налаштування (конфігурацію) Git?</summary>

-   git config

</details>

<details>
<summary>Який прапорець дозволяє встановити зміни конфігурації для всіх репозиторіїв (теперішніх і майбутніх)?</summary>

-   --global

</details>

<details>
<summary>Як встановити ім'я користувача у конфігурації?</summary>

-   git config --global user.name `"your_name"`

</details>

<details>
<summary>Як встановити пошту (email) користувача у конфігурації?</summary>

-   git config --global user.email `"your_email"`

</details>

<details>
<summary>Навіщо потрібно встановлювати ці налаштування?</summary>

-   щоб git міг відслідковувати, хто автор змін

</details>

<details>
<summary>Яка команда перелік всіх налаштувань конфігурації?</summary>

-   git config --list

</details>

<details>
<summary>Яка команда дозволяє вивести всі папки, в тому числі приховані (трекінгові)?</summary>

-   ls -a

</details>

<details>
<summary>Яка команда дозволяє перевірити статус статуси файлів?</summary>

-   git status

</details>

<details>
<summary>Яка команда дозволяє отримати довідку?</summary>

-   git --help
-   git `your_command` --help (довідка для конкретної команди)

</details>

---

<h3 id="git-main-theory">Git — теорія, основні концепції</h3>

<details>
<summary>Які три основні концепції git?</summary>

-   коміти
-   збереження усіх версій файлів
-   гілки

</details>

<details>
<summary>Що таке коміт?</summary>

-   збереження файлу (його версії)
-   інформація про те:
    -   хто зберіг
    -   коли зберіг
    -   що саме було зроблено
-   можливість повернутися до попередніх версій файлів

</details>

<details>
<summary>Як зберігаються в комітах файли, в який не було жодних змін?</summary>

-   зберігається **посилання** на вихідний файл

</details>

<details>
<summary>Який порядок локального збереження версій файлів?</summary>

-   git add (staging area)
-   git commit (committed area)

</details>

<details>
<summary>Локальне збереження файлів (схема)</summary>

<img src="./assets//images/local-file-saving-scheme.png" width="800" alt="Local file storage scheme"/>

</details>

<details>
<summary>Які шляхи вказання шляху до потрібної директорії (команда і два варіанти відображення шляху)?</summary>

-   команда — **cd**
-   відображення шляху:
    -   перетягти папку у вікно git bash (і шлях відобразиться, треба тільки cd на початку дописати)
    -   написати повністю шлях самостійно

</details>

<details>
<summary>Які каталоги git не відстежує?</summary>

-   в яких немає файлів, або файлів, які ігноруються через .gitignore

</details>

---

<h3 id="git-main-commands">Git — основні команди</h3>

[Конспект](https://github.com/NickTimosh/git_course/blob/main/notebooks/5.%20git%20-%20%D0%91%D0%B0%D0%B7%D0%BE%D0%B2%D1%96%20%D0%9A%D0%BE%D0%BC%D0%B0%D0%BD%D0%B4%D0%B8.md)

<h4>Додавання коду і коміти</h4>

<details>
<summary>Як додати усі файли однією командою у staging area?</summary>

-   git add .

</details>

<details>
<summary>Як додати один файл у staging area?</summary>

-   git add `file_name`

</details>

<details>
<summary>Як додати коротке повідомлення до коміту?</summary>

-   git commit -m `"your_comment"`
-   вказується коротко, які зміни зроблено

</details>

<details>
<summary>Внесення комітів через Wim (схема)</summary>

<img src="./assets//images/commtted-with-WIM.png" width="800" alt="Commit scheme via Wim"/>

</details>

<details>
<summary>Внесення комітів через nano (схема)</summary>

<img src="./assets//images/edit-files-with-nano.png" width="800" alt="Commit scheme via Wim"/>

</details>

<details>
<summary>Внесення комітів через notepad (схема)</summary>

<img src="./assets//images/edit-files-with-notepad.png" width="800" alt="Commit scheme via Wim"/>

</details>

<details>
<summary>Як змінити текстовий редактор і встановити його основним (команда)?</summary>

-   git config --global core.editor `"your_editor"

</details>

<h4>Історія комітів</h4>

<details>
<summary>Яка команда виводить перелік всіх комітів?</summary>

-   git log

</details>

<details>
<summary>Який прапорець дозволяє вивести історію у більш компактному вигляді?</summary>

-   --oneline
-   повний варіант команди: git log --oneline

</details>

<details>
<summary>Яка команда (з прапорцем) дозволяє подивитися зміни комітів?</summary>

-   git log -p

</details>

<details>
<summary>Як вийти з інтерактивного режиму (яка клавіша)?</summary>

-   q (маленька)

</details>

<details>
<summary>Яка команда дозволяє подивитись відмінності  у файлах (і всього репозиторію)?</summary>

-   git diff (difference)

</details>

---

<h3 id="git-extensions-basics">Git — розширення основ</h3>

[Конспект](https://github.com/NickTimosh/git_course/blob/main/notebooks/6.%20git%20-%20%D0%A0%D0%BE%D0%B7%D1%88%D0%B8%D1%80%D0%B5%D0%BD%D0%BD%D1%8F%20%D0%9E%D1%81%D0%BD%D0%BE%D0%B2.md)

<details>
<summary>Яка загальноприйнята практика формулювання повідомлень для комітів?</summary>

-   наказова (імперативна) форма
    -   (add, write, remove, delete, change, fix etc.)

</details>

<details>
<summary>Як додати тіло коміту, щоб детальніше описати зміни (послідовність кроків)?</summary>

-   не закривати лапки
-   клікнути enter
-   перейти на новий рядок
-   продовжити писати
-   закрити лапки
-   enter (для відправки коміту)

</details>

<details>
<summary>Як додати зміни так, щоб вони були частиною попереднього коміту, а не новоствореним комітом?</summary>

-   git add .
-   git commit --amend --no-edit (замість повідомлення)
-   enter

</details>

<details>
<summary>Різниця у кроках між створення нового коміти і зміною існуючого (схема)</summary>

<img src="./assets//images/commit-creat.png" width="800" alt="Diagram of the difference in steps between creating a new commit and modifying an existing one"/>

</details>

<details>
<summary>Як накопичувати зміни з різних файлів для одного коміту?</summary>

-   внести зміни в різні файли та/або створити нові файли
-   git add . (додаємо всі файли)
-   git commit -m `"your_commit"`

</details>

<details>
<summary>Як додати кілька файлів (не всі) за один раз до staging area?</summary>

-   git add `<file_1> <file_3> <file_5>`

</details>

<details>
<summary>Як побачити різницю у файлах, що вже додані до staging area?</summary>

-   git diff --chached

</details>

<details>
<summary>Як повернути файли зі staging area до working area?</summary>

-   **після** git add але **до** git commit
    -   git restore --staged <file_name> or path to file

</details>

<details>
<summary>Як подивитися, який саме невідстежуваний файл користувач планує видалити (який прапорець)?</summary>

-   -n
-   повна команда: git clean -n

</details>

<details>
<summary>Яка команда дозволяє видалити невідстежувані файли з git (з прапорцем)?</summary>

-   git clean -f

</details>

<details>
<summary>Яка команда дозволяє видалити невідстежувані файли і каталоги з git (з прапорцем)?</summary>

-   git clean -fd
    -   **ця команда незворотна**

</details>

<details>
<summary>Яка команда дозволяє видалити відстежувані файли з індексу та робочого каталогу?</summary>

-   git rm `<file_name>` (remove)

</details>

<details>
<summary>Яка команда дозволяє видалити відстежувані файли тільки з індексу, залишивши його у робочому каталозі (з прапорцем)?</summary>

-   git rm --cached `<file_name>`

</details>

---

<h3 id="git-recovery-version">Git — вступ до відновлення версій</h3>

[Конспект](https://github.com/NickTimosh/git_course/blob/main/notebooks/7.%20git%20-%20%D0%A0%D0%BE%D0%B1%D0%BE%D1%82%D0%B0%20%D0%B7%20%D0%9A%D0%BE%D0%BC%D1%96%D1%82%D0%B0%D0%BC%D0%B8.md)

<details>
<summary>Що зберігається в комітах?</summary>

-   зміни, що були зроблені у файлах

</details>

<details>
<summary>Що має унікальне кожна нова версія файлів?</summary>

-   "#" — хеш-код (як id)
    -   є унікальним для кожної версії файлу

</details>

<details>
<summary>Основні area (схема)</summary>

<img src="./assets//images/main-areas-files.png" width="800" alt="Scheme of the main area files in git"/>

</details>

<details>
<summary>Яка команда дозволяє повернути закомічений файл (наприклад, після його видалення)?</summary>

-   git restore `file_name`
    -   за замовчування звернення до останньої закоміченої версії файлу

</details>

<details>
<summary>Яка команда дозволяє дізнатися, що було змінено в тому чи іншому коміті (по id)?</summary>

-   git show `commit_id`

</details>

<details>
<summary>Яка команда дозволяє повернутися до конкретної версії файлу (а не тільки останньої, по id)?</summary>

-   git restore --source=`commit_id` `file_name`

</details>

<details>
<summary>Яка команда дозволяє відмінити зміни, які вже були додані до staging area?</summary>

-   git restore --staged `file_name`

</details>

<details>
<summary>Яка команда дозволяє повернутися до попередньої (та/або конкретної версії всього проєкту)?</summary>

-   git reset `прапорець` `HEAD або ID`
-   `HEAD` — останній коміт
-   `ID` — конкретний коміт з переліку попередніх

</details>

<details>
<summary>Які прапорці має ця команда і чим вони відрізняються?</summary>

-   --hard — перезапише повністю до поточної версії, до якої ми звернемося (через id) і повністю видаляє всі зміни

-   --soft — дозволяє зберегти внесені зміни (у staging)

-   --mixed — **використовується за замовчуванням**

    -   всі зміни, які були додані до staging area, будуть прибрані назад у робочу директорію
    -   тобто файли, які були в staging, знову стають "modified", але не видаляються

-   повні команди:
    -   git reset --hard `ID`
    -   git reset --soft `ID`

</details>

---

<h3 id="git-branches">Git — вступ в git branch</h3>

[Конспект](<https://github.com/NickTimosh/git_course/blob/main/notebooks/8.%20git%20-%20Branches%20(%D0%B3%D1%96%D0%BB%D0%BA%D0%B8).md>)

<details>
<summary>Яка основна гілка проєкту?</summary>

-   main (master) — різна назва, але значить одне й те саме

</details>

<details>
<summary>Принцип роботи гілок (схема)</summary>

<img src="./assets//images/working-principale-branches.png" width="1000" alt="Diagram of how branches work in git"/>

</details>

<h4>HEAD</h4>

<details>
<summary>Що таке HEAD?</summary>

-   вказівник того, де ми знаходимось
    -   в якій гілці
    -   в якому коміті
-   за замовчуванням знаходимося в останньому коміті
-   кожна окрема гілка має свій HEAD

</details>

<details>
<summary>Що означає "detached HEAD"?</summary>

-   коли `HEAD` не вказує на останній коміт гілки, а вказує на конкретний коміт або тег

</details>

<details>
<summary>За допомогою якої команди HEAD переходить у стан detached HEAD?</summary>

-   git checkout `commit_hash`
-   у цьому випадку `HEAD` вказує на той коміт, а не на гілку

</details>

<details>
<summary>Що дає detached HEAD?</summary>

-   У стані detached HEAD можна переглядати або тестувати код на певному коміті, але будь-які нові коміти, які будуть зроблені, не будуть пов'язані з жодною гілкою
-   для збереження коміту, що був зроблений у цьому стані, потрібно створити нову гілку, щоб не втратити зміни

</details>

<details>
<summary>Як вийти зі стану "detached HEAD"?</summary>

-   використати команду `git checkout <branch-name>`, де `<branch-name>` — це назва гілки, на якій ви хотіли б продовжити працювати

</details>

<details>
<summary>Принцип роботи HEAD (схема)</summary>

<img src="./assets/images/working-principale-head.png" width="800" alt="Schematic diagram of the HEAD operating principle"/>

</details>

<h4>Конфлікти</h4>

<details>
<summary>Що таке конфлікти в git?</summary>

-   ситуація, коли на одних і тих самих рядках, в одних і тим самих файлах вказані різні дані

</details>

<details>
<summary>Що значить "вирішити конфлікт"?</summary>

-   конкретне вказання git, які саме зміни мають бути внесені

</details>

<h4>Merge vs Rebase</h4>

<details>
<summary>Що значить merge?</summary>

-   впровадити зміни до основої гілки (об'єднати всі додаткові гілки в main)

</details>

<details>
<summary>Яка є альтернативна merge?</summary>

-   rebase

</details>

<details>
<summary>Що дозволяє робити ця альтернатива?</summary>

-   інтегрувати зміни **після** останньої актуальної версії в main гілці

</details>

<details>
<summary>Які складнощі пов'язані з цим способом?</summary>

-   перезапис id деяких комітів, що може викликати певні складнощі, якщо виникне потреба відновити якісь попереднії версії

</details>

<details>
<summary>Різниця між merge і rebase (схема)</summary>

<img src="./assets/images/difference-between-merge-and-rebase.png" width="1000" alt="Diagram of the difference between merge and rebase"/>

</details>

<h4>Гілки</h4>

<details>
<summary>Яка команда виведе список всіх гілок?</summary>

-   якщо потрібно побачити тільки локальні гілки
    -   git branch
-   якщо потрібно побачити віддалені гілки
    -   git branch -r

</details>

<details>
<summary>Яка команда дозволяє створити нову гілку?</summary>

-   git branch `branch_name`

</details>

<details>
<summary>Яка команда дозволяє перемикатися між гілками?</summary>

-   git checkout `branch_name`

</details>

<details>
<summary>Яка команда дозволяє створити і перемкнутися на гілку (одна команда — дві дії)?</summary>

-   git checkout -b `branch_name`
    -   -b — від слова branch

</details>

<details>
<summary>Яка є альтернативна команда для зміни гілки?</summary>

-   git switch `branch_name`

</details>

<details>
<summary>Яка вона дозволяє за один крок створити гілку і одразу перемкнутися на неї (синтаксис команди)?</summary>

-   git switch -b `branch_name`

</details>

<details>
<summary>Яка різниця між цими двома варіантами команд?</summary>

-   git switch:
    -   більш проста у розуміння і використанні
    -   використовується спеціально для перемикання (та/або для створення і перемикання) між гілками
-   git checkout:
    -   більш універсальна
    -   використовується для:
        -   перемикання (та/або для створення і перемикання) між гілками
        -   зміни гілок
        -   відновлення файлів (скасування змін)
        -   перемикання між комітами

</details>

<details>
<summary>В якій гілці ми маємо знаходитися перед тим, як зробити об'єднання гілок?</summary>

-   в тій, в яку хочемо інтегрувати зміни (в цільовій)

</details>

<details>
<summary>Яка команда дозволяє об'єднати гілки?</summary>

-   git merge `branch_name`

</details>

<details>
<summary>Назву якої гілки ми маємо писати у команді об'єднання?</summary>

-   назву гілки, **яку об'єднуємо** з цільовою гілкою (тобто назву альтернативної, додаткової гілки)

</details>

<details>
<summary>Яка команда дозволяє тільки передати зміни, але не об'єднувати гілки?</summary>

-   git fetch

</details>

<details>
<summary>Яка команда (з прапорцем) дозволяє видалити гілку?</summary>

-   git branch -d `branch_name`
-   git branch -D `branch_name`

</details>

<details>
<summary>Яка різниця між цими двома прапорцями?</summary>

-   **-d** (soft delete) — не дозволить видалити гілку, яка ще не була передана до main (яка ще не інтегрована)
-   **-D** (hard delete) — видалить гілку незалежно від того, чи вона вже інтегрована у main чи ще ні (безумовне видалення гілки)

</details>

---

<h2>GitHub</h2>

<h3 id="github-concept">GitHub — основні концепції</h3>

<h4>Віддалений репозиторій</h4>

<details>
<summary>Які бувають git-сховища?</summary>

-   GitHub
-   GitLab
-   Bitbucket, Azure DevOps, SourceForge — також популярні віддалені репозиторії

</details>

<details>
<summary>Яке типове ім'я git?</summary>

-   origin - стандартна назва для віддаленого репозиторію, але її можна змінювати

</details>

<h4>Клонування (Clone)</h4>

<details>
<summary>Що передбачає концепція клонування?</summary>

-   створення локальної копії віддаленого репозиторію на комп'ютері

</details>

<h4>SSH-ключ (SSH-key)</h4>

<details>
<summary>Що передбачає концепція такого ключа?</summary>

-   спосіб безпечного підключення по GitHub без введення пароля
    -   SSH-ключ складається з публічного та приватного ключа. Публічний ключ додається до GitHub, а приватний зберігається локально

</details>

<h4>Пуш (Push)</h4>

<details>
<summary>Що передбачає концепція push?</summary>

-   надсилання змін у віддалений репозиторій

</details>

<details>
<summary>Яка команда?</summary>

-   git push

</details>

<h4>Пул (pull)</h4>

<details>
<summary>Що передбачає ця концепція?</summary>

-   завантаження змін з віддаленого репозиторію

</details>

<details>
<summary>Яка команда?</summary>

-   git pull

</details>

<h4>Пул-реквест (Pull Request, PR)</h4>

<details>
<summary>Що передбачає ця концепція?</summary>

-   запит на злиття змін із однієї гілки в іншу
-   часто використовується для перевірки коду

</details>

<details>
<summary>Як називається перевірка коду іншим розробником?</summary>

-   code review

</details>

<h4>Форк (Fork)</h4>

<details>
<summary>Що передбачає ця концепція?</summary>

-   копіювання репозиторію в акаунт користувача, що дозволяє експериментувати з кодом, не змінюючи оригінал

</details>

<h4>README.md</h4>

<details>
<summary>Що це за файл?</summary>

-   файл документації, що зазвичай містить опис проєкту, інструкції з використання та іншу корисну інформацію

</details>

<details>
<summary>Що означає розширення **.md**</summary>

-   формат markdown
-   система форматування тексту

</details>

<h4>Issues (Завдання)</h4>

<details>
<summary>Що передбачає ця концепція?</summary>

-   систему відстеження помилок, запитів на нові функції та обговорень у репозиторії

</details>

---

<h3 id="github-first-repo">GitHub — перший репозиторій</h3>

<details>
<summary>Яка має бути назва репозиторію?</summary>

-   унікальною в межах репозиторію

</details>

<details>
<summary>Які бувають типи репозиторіїв?</summary>

-   публічні
-   приватні

</details>

<details>
<summary>Що таке ліцензія?</summary>

-   документ, у якому прописано, що можна, а що заборонено робити з репозиторієм (чи можна завантажувати код, перевикористовувати його у власних проєктах і тд)
-   опис можливостей взаємодії з репозиторієм

</details>

<details>
<summary>Про що говорить ліцензія MIT?</summary>

-   про те, що код і файли з репозиторію можна використовувати як завгодно без обмежень, але **обов'язково потрібно вказати авторство власника репозиторію, з якого беруться дані**

</details>

<details>
<summary>Як можна додати файли у репозиторій?</summary>

-   створити прямо на платформі у github
-   завантажити з комп'ютера через командний рядок

</details>

---

<h3 id="github-gitignore">GitHub — файл .gitignore</h3>

<details>
<summary>Що таке .gitignore?</summary>

-   файл, який використовується для того, щоб ігнорувати певні файли та папки в git. Файли і теки, додані в .gitignore не будуть додватись у коміти та потрапляти у репозиторій

</details>

<details>
<summary>Яку папку ні в якому разі не можна додавати у репозиторій?</summary>

-   node_module — тека, яка містить всі залежності, встановлені у проєкті

</details>

<details>
<summary>Якою командою можна завантажити цю папку, не завантажуючи її у репозиторій?</summary>

-   npm install

</details>

---

<h3 id="github-watch-fork-stars">GitHub — watch, fork & stars</h3>

<details>
<summary>Що дає змогу робити кнопка "Watch" у репозиторії?</summary>

-   слідкувати за змінами репозиторію

</details>

<details>
<summary>Що дає змогу зробити кнопка "Fork"?</summary>

-   зробити повну копію репозиторію

</details>

<details>
<summary>Як використовується зірочка в репозиторіях?</summary>

-   як елементи рейтингу

</details>

---

<h3 id="github-fork">GitHub — копіювання репозиторію (Fork)</h3>

<details>
<summary>Чи впливають зміни, внесені у скопійований репозиторій на оригінал?</summary>

-   ніяким чином, це два окремі репозиторії

</details>

<details>
<summary>У якій вкладці можна подивитися, хто зробив копію репозиторію?</summary>

-   insights —> forks

</details>

<details>
<summary>Як можна змінити видимість репозиторію (яка вкладка і шлях)?</summary>

-   settings —> general —> danger zone —> change repository visibility

</details>

---

<h3 id="github-pr">GitHub — створення Pull Requests (PR)</h3>

<details>
<summary>Що таке pull request?</summary>

-   запит на об'єднання змін, які розробник вніс в код, з основною гілкою проєкту

</details>

<details>
<summary>Де розробник може вносити зміни віддалено без шкоди основному репозиторію (два варіанти)?</summary>

-   створити окрему гілку (git branch -b `branch_name`)
-   повністю скопіювати репозиторій (fork)

</details>

<details>
<summary>Яка вкладка відповідає за створення pull request?</summary>

-   однойменна "Pull request"

</details>

<details>
<summary>Який статус повідомляє про те, що об'єднання можливе?</summary>

-   able to merge

</details>

<details>
<summary>Головна анатомія створення реквесту (схема)</summary>

<img src="./assets/images/main-anatomy-create-request.png" width="1000" alt="The scheme of creating a pull request"/>

</details>

---

<h3 id="github-issues">GitHub — створення Issues (задач)</h3>

<details>
<summary>Яка вкладка відповідає за створення завдання?</summary>

-   однойменна "Issues"

</details>

<details>
<summary>Як можна створити задачу?</summary>

-   натиснути на кнопку "New issue"
-   ввести title — лаконічно пояснити, яка проблема виникла
-   написати description (за потреби додати якісь додаткові матеріали) — запропонувати кілька рішень
-   натиснути кнопку "create"

</details>

---

<h3 id="github-workflow">GitHub — огляд типового workflow</h3>

<details>
<summary>Огляд workflow роботи git-github (схема)</summary>

<img src="./assets/images/workflow-git-github.png" width="1000" alt="The scheme of workflow"/>

</details>

<details>
<summary>Які основні кроки?</summary>

1. **connection** — утворення зв'язку між git & github
    1. ssh-key
2. **sync** — синхронізація того, що є на комп'ютері і того, що є на github
    1. **push** local to remote repo або
    2. **clone** remote to local repo
3. **pull** — завантажити собі останню актуальну версію проєкту (оновлення локального репо)
4. **branch** — створюємо нову гілку
5. **commit** — передаємо зміни з гілки до локального репо
6. **push** — відправляємо всю гілку зі змінами до віддаленого репо
7. **pull request** — інформація про зміни, які ми плануємо передати до main
    1. code review
    2. merge
8. повторюємо цикл з пункту три

</details>

---

<h3 id="github-ssh-key">GitHub — SSH-ключ</h3>

<details>
<summary>Що таке ssh-ключ?</summary>

-   файл, який має зберігати приватний ключ на комп'ютері та одночасно публічний ключ на github

</details>

<details>
<summary>У якій вкладці ці ключі зберігаються на github?</summary>

-   profile settings —> SSH and GPG keys

</details>

<details>
<summary>Яка послідовність створення і збереження?</summary>

1. створити файл на машині, де буде зберігатися ключ
2. додати його на github

</details>

<details>
<summary>Скільки разів має створюватися цей ключ?</summary>

-   один раз на одну машину

</details>

[Мега важливий конспект по створенню і збереженню ssh ключа](https://github.com/NickTimosh/git_course/blob/main/notebooks/9.%20Github%20-%20SSH%20keys.md)

---

<h3 id="github-push-local-repo">GitHub — push локального репозиторію</h3>

<details>
<summary>Яка послідовність ініціалізацї, комітів та додавання файлів до локального репо (крок — команда)?</summary>

1. ініціалізація репозиторію
    1. git init
2. додати файли до staging area
    1. git add .
3. зробити коміт
    1. git commit -m `"Initial commit"`
4. перевірка статусу (за потреби)
    1. git status

</details>

<details>
<summary>Яка команда дозволяє відправити зміни на github?</summary>

-   git remote add origin `repo_link` (https or ssh)

</details>

<details>
<summary>Що означає "origin"?</summary>

-   використовується як псевдонім до посилання

</details>

<details>
<summary>Звідки можна взяти посилання на repo?</summary>

-   з github
    -   при створення порожнього репозиторію це вікно відкривається по дефолту з детальним описом, як віддалений репозиторій підв'язати до локального

</details>

<details>
<summary>Яка команда дозволяє відправити весь код з локальної машини на віддалений репозиторій після об'єднання цих репозиторіїв?</summary>

-   git push -u origin main
-   -u — від слова "upstream"

</details>

<details>
<summary>За що відповідає upstream?</summary>

-   повідомляє github з якої гілки брати зміни та/або в яку гілку зміни завантажувати
    -   Upstream гілка — це віддалена гілка, до якої підключено локальну гілку для відправки та отримання змін

</details>

<details>
<summary>Яка команда дозволяє перейменувати головну гілку (з master на main)?</summary>

-   git branch -M main

</details>

---

<h3 id="github-brach-and-pull">GitHub — гілки та pull request</h3>

<details>
<summary>Яка команда дозволяє відправити на віддалений репозиторій гілку, яка була створено локально?</summary>

-   git push --set -upstream origin `branch_name`
    -   зазвичай git одразу пропонує цю команду за замовчування після команди push, тому залишається тільки скопіювати її і вставити в термінал

</details>

<details>
<summary>Що робить --set upstream?</summary>

-   встановлює гілку на віддаленому репозиторії origin
    -   --set-upstream встановлює зв'язок між локальною і віддаленою гілкою для автоматичної синхронізації

</details>

<details>
<summary>Анатомія гілок при pull request (схема)</summary>

<img src="./assets//images/pull-requrst-anatomy-branches.png" width="800" alt="Schematic of the pull request branch"/>

</details>

---

<h3 id="github-clone-repo">GitHub — клонування репозиторію</h3>

<details>
<summary>За допомогою якої команди можна скопіювати репозиторій собі локально?</summary>

-   git clone `repo_link` (https or ssh)

</details>

<details>
<summary>Яка різниця між використання https та ssh посилання?</summary>

-   https вимагає явної авторизації
-   з ssh ключем проводиться неявна авторизація (немає потреби кожен раз вводити логін і пароль для підтвердження)

</details>

<details>
<summary>Яка команда дозволяє відобразити які локальні гілки пов'язані з віддаленими гілками?</summary>

-   git branch -vv
-   також ця команда показує інформацію про останні коміти в цих гілках

</details>

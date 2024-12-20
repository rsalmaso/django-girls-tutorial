# Вступ до інтерфейсу командного рядка

Це захоплює, чи не так?! Ви напишете свій перший рядок коду через декілька хвилин :)

__Дозвольте нам представити вас вашому новому другові: командний рядок!__

Наступні кроки покажуть вам, як користуватися чорним вікном хакерів. Спочатку це може видаватися трохи жахливим, однак насправді - це лише командна підказка, що очікує від вас певних команд.

> **Примітка.** Зауважте, що в цій книзі ми використовуємо терміни 'директорія', 'каталог' та 'папка' взаємозамінно, ці слова означають одне й те саме.

## Що таке командний рядок?

Вікно, яке зазвичай називають __командним рядком__ або __інтерфейсом командного рядка__, є текстовою програмою для перегляду, обробки і управління файлами на вашому комп'ютері. Як Провідник на Windows чи Finder на Mac, але без графічного інтерфейсу. Інші назви командного рядка: *cmd*, *CLI*, *prompt*, *console* або *terminal*.

## Відкриваємо інтерфейс командного рядка

Щоб почати експериментувати, нам потрібно спочатку відкрити наш інтерфейс командного рядка.

### Windows

Перейдіть до меню Пуск → Усі програми → Стандартні → Командний рядок.

### macOS

Додатки → Утиліти → Термінал.

### Linux

Скоріш за все Додатки → Стандартні → Термінал, але це може залежати від вашої системної версії. Якщо тут його немає, просто загугліть :)

## Командний рядок

Має з'явитися біле або чорне вікно, що очікує на ваші команди.

Якщо ви працюєте на Mac або на Linux, ви напевно побачите `$`, на зразок:

    $

На Windows, це знак `>`:

    >

Кожній команді буде передувати цей знак і один пробіл, але ви не мусите набирати їх. Ваш комп'ютер робитиме це для вас сам :)

> Просто маленьке зауваження: у вашому випадку ви побачите щось на кшталт `C:\Users\ola>` або `Olas-MacBook-Air:~ ola$` перед знаком командного рядка і це на 100% є правильним.

Частина до `$` або `>` включно називається *запрошенням командного рядка* або скорочено *командним рядком*. Вона запрошує вас ввести туди щось.

У посібнику, коли нам потрібно, щоб ви набрали щось в командний рядок, ми включатимемо `$` або `>`, а іноді й більше символів зліва. Ви можете ігнорувати ліву частину і друкувати в командний рядок лише те, що починається після `$`.

## Ваша перша команда (ЙОЙ!)

Почнемо з чогось простенького. Наберіть команду:

    $ whoami

або

    > whoami

Далі натисніть `enter`. Це наш результат:

    $ whoami
    olasitarska

Як бачимо, комп'ютер лише виводить ваше ім'я користувача. Файно, еге ж?:)

> Спробуйте набирати кожну команду, а не копіювати і вставляти. Таким чином ви більше запам'ятаєте!

## Основи

У кожної операційної системи є трохи відмінні набори команд для командного рядку, отже, будьте певними, що виконуєте інструкції саме для вашої операційної системи. Давайте спробуємо?

### Поточна директорія

Було б чудово знати, де ми перебуваємо зараз, чи не так? Давайте подивимося. Введіть цю команду і натисніть `enter`:

    $ pwd
    /Users/olasitarska

Якщо ви працюєте на Windows:

    > cd
    C:\Users\olasitarska

Можливо, ви побачите щось схоже на вашій машині. Після того, як ви відкрили командний рядок, ви зазвичай починаєте зі своєї домашньої папки.

> Зауваження: 'pwd' відповідає 'print working directory' (англ. надрукувати робочу папку).

---

### Список файлів і папок

Отже, що ж всередині? Було б круто з'ясувати. Давайте подивимось:

    $ ls
    Applications
    Desktop
    Downloads
    Music
    ...

Windows:

    > dir
     Directory of C:\Users\olasitarska
    05/08/2014 07:28 PM <DIR>      Applications
    05/08/2014 07:28 PM <DIR>      Desktop
    05/08/2014 07:28 PM <DIR>      Downloads
    05/08/2014 07:28 PM <DIR>      Music
    ...

---

### Змінити поточну директорію

Тепер давайте перейдемо до директорії робочого столу:

    $ cd Desktop

Windows:

    > cd Desktop

Перевірте, чи дійсно щось змінилось:

    $ pwd
    /Users/olasitarska/Desktop

Windows:

    > cd
    C:\Users\olasitarska\Desktop

Ось!

> ПРОФІ хитрощі: якщо ви наберете `cd D` і потім натиснете `tab` на клавіатурі, командний рядок автоматично заповнить решту імені, таким чином можна переходити швидше. Якщо папок, що починаються з "D" більше однієї, натисніть кнопку `tab` двічі для отримання списку варіантів.

* * *

### Створити директорію

Як щодо створення каталогу `practice` на вашому робочому столі? Ви можете зробити це таким чином:

    $ mkdir practice

Windows:

    > mkdir practice

Ця коротка команда створить папку з іменем `practice` на вашому робочому столі. Може перевірити чи є вона там, просто глянувши на свій Робочий стіл або запустивши команду `ls` або `dir`! Спробуйте :)

> ПРОФІ хитрощі: Якщо ви не хочете кожного разу набирати одну й ту ж команду, спробуйте натиснути кнопки `стрілка вгору` та `стрілка вниз` на своїй клавіатурі щоб повторити нещодавно використовувані команди.

---

### Вправа!

Невеличке випробування для вас: в щойно створеній директорії `practice` створіть папку `test`. Використайте команди `cd` та `mkdir`.

#### Розв'язання:

    $ cd practice
    $ mkdir test
    $ ls
    test

Windows:

    > cd practice
    > mkdir test
    > dir
    05/08/2014 07:28 PM <DIR>      test

Вітаємо! :)

---

### Прибираємо

Ми не хочемо залишити безлад, то ж давайте видалимо усе, що ми створили до цього моменту.

Спочатку нам потрібно повернутися назад до директорії Робочий стіл:

    $ cd ..

Windows:

    > cd ..

Використання `cd` із `..` змінить вашу поточну директорію на батьківську (тобто папка, що містить вашу поточну папку).

Перевірте де ми:

    $ pwd
    /Users/olasitarska/Desktop

Windows:

    > cd
    C:\Users\olasitarska\Desktop

Тепер час видалити директорію `practice`:

> __Увага__: Видалення файлів за допомогою `del`, `rmdir` або `rm` є безповоротнім, тобто *файли будуть видалені назавжди*! То ж, будьте конче обережними із цими командами.

    $ rm -r practice

Windows:

    > rmdir /S practice
    practice, Are you sure <Y/N>? Y

Виконано! Щоб переконатися, що папку дійсно видалена, давайте перевіримо:

    $ ls

Windows:

    > dir

### Вихід

Це все наразі! Можна тепер спокійно закрити командний рядок. Давайте зробимо це хакерським методом, добре?:)

    $ exit

Windows:

    > exit

Круто, га?:)

## Підсумок

Тут наведено підсумок деяких корисних команд:

| Команда (Windows) | Команда (Mac OS / Linux) | Опис                     | Приклад                                           |
| ----------------- | ------------------------ | ------------------------ | ------------------------------------------------- |
| exit              | exit                     | закрити вікно            | **exit**                                          |
| cd                | cd                       | змінити директорію       | **cd test**                                       |
| dir               | ls                       | список директорій/файлів | **dir**                                           |
| copy              | cp                       | скопіювати файл          | **copy c:\test\test.txt c:\windows\test.txt** |
| move              | mv                       | перемістити файл         | **move c:\test\test.txt c:\windows\test.txt** |
| mkdir             | mkdir                    | створити нову директорію | **mkdir testdirectory**                           |
| del               | rm                       | видалити директорію/файл | **del c:\test\test.txt**                        |

Тут наведено лише невелику кількість команд, котрі можна запускати у вашому командному рядку, однак, на даний момент ми не збираємося використовувати щось більше.

Якщо вас цікавить, [ss64.com](http://ss64.com) містить повний список посилань на команди для усіх операційних систем.

## Готові?

Давайте зануримось у Python!

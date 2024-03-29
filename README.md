Інструкція як користуватись Telegram-remote-shell Як встановити бота для роботи програми? в коді є такий елемент як “Token” в ньому вказаний API-ключ який дозволяє транслювати всі дії на комп’ютері та керування комп’ютером в якому запущена програма В ЖОДНОМУ ВИПАДКУ НЕ ВИКОРИСТОВУЙТЕ ПРОГРАМУ З ІДЕНТИЧНИМ ТОКЕНОМ НА РІЗНИХ ПРИСТРОЯХ, бо в такому випадку програма буде працювати не коректно або взагалі не буде працювати або буде працювати але від цього ніякої користі не буде! Новий токен можна отримати через телеграм бота https://t.me/BotFather там ви можете створити свого бота та отримати його API ключ який ви вказуєте в коді, що дозволить використовувати бота на окремому пристрої. 

Щоб створити бота на https://t.me/BotFather
потрібно зайти до телеграм бота, написати команду /start, пришемо команду /new bot, пишемо будь-яку назвусвого бота але в кінці обов'язково має бути приписка "bot"

![image](https://github.com/SunsetTekila/TelegramRemoteControl/assets/157602307/78fe1ae9-ec1a-46c4-828f-ffa25ec5ddc5)

![image](https://github.com/SunsetTekila/TelegramRemoteControl/assets/157602307/351837e0-d93e-4b51-a852-abf9ee718d24)

![image](https://github.com/SunsetTekila/TelegramRemoteControl/assets/157602307/a9f64200-5e97-4d22-b95b-24ff6d5cf700)

Тепер у вас є АРІ ключ і бот з якими ви будете працювати. заходьте до свого телеграм бота. 

![image](https://github.com/SunsetTekila/TelegramRemoteControl/assets/157602307/1fd904ad-e428-4882-9cb5-a7c664f9a20c)


Писати АРІ ключ потрібно в самій програмі а саме у нижче показаному елементі коду:

![image](https://github.com/SunsetTekila/TelegramRemoteControl/assets/157602307/8dbd0f57-399c-446d-b260-920896c87a6c)


треба писати так: TOKEN = "Your API"


Ще спробуйте скористатись віртуальним рередовищем python це можна зробити так:
* відкриваємо командну строку через команду cd преходимо в корінну папку програми
* пишемо команду .env\scripts\activate
* тепер у вас в строці з'явиться помітка "(.env)" :
*  ![image](https://github.com/SunsetTekila/TelegramRemoteControl_DynamicConfig/assets/157602307/6034594c-ddb4-42f5-bc9f-d69e84d39e09)
* тепер ви можете використовувати готовий набір бібліотек і маєте можливість використовувати "pyinstaller" а саме введіть команду: "pyinstaller --noconfirm --onefile --windowed (назва програми.py)". Ще ви можете запустити програму, щоб це зробити вам потрібно ввести команду "python telegram-remote-shell.py"


ІНТЕРФЕЙС
* при натисканні кнопки «розпочати» або написанні команди /start бот розпочне роботу
* /info – видає ім’я користувача ір адреси
* dir – показує в якій папці ви знаходитесь
* /SYSTEMINFO - Відображає докладні відомості про конфігурацію комп'ютера та його операційної системи, включаючи конфігурацію операційної системи, відомості про безпеку, ідентифікатор продукту та властивості обладнання (наприклад, ОЗП, дисковий простір та мережні картки).
* /charset 866 - Ця частина коду призначена для обробки команди /charset у вашому Telegram-боті. Коли користувач вводить команду /charset разом із параметром, наприклад, /charset utf-8, скрипт виконує наступні дії: Витягує значення параметра команди, тобто кодування символів (utf-8). Присвоює це значення глобальній змінній decode_charset. Якщо користувач вводить лише команду /charset без параметра, скрипт виконує наступні дії: Відправляє користувачеві повідомлення, що містить поточне значення глобальної змінної decode_charset. Приведені вище дії можуть бути корисні для визначення чи зміни кодування символів, яке використовується для обробки тексту в боті. Наприклад, користувач може встановити нове кодування, яке відповідає його потребам, за допомогою команди /charset. 
* /HelpMe – показує команди які ви можете ввести через командну строку “/cmd <будь-яка команда яка вводиться через cmd>”
* /keylog – розпочинає запис кнопок які натискались на клавіатурі
* /getkeylog – показує вже записані кнопки
* /screenshot – робить знімок екрану (рекомендується натискати цю кнопку двічі щоб відправити собі актуальний знімок екрану)
* /add_to_task_scheduler – додати програму до автоматичного ввімкнення програми після наступного входу в систему через Task Scheduller (якщо комп'ютер знову уввімкнеться, то після входу в систему програма знову запуститься автоматично) (кнопка може не спрацювати у зв’язку з системою безпеки та правами адміністратора)
* /get “назва програми” завантажити програму
* /help – (команда вводиться вручну для отримання додаткової інформації про деякі команди які вводяться вручну)
* /cd .. – вийти з папки;
* /cd назва папки або програми файла і тд (вказуйте формат якщо він є наприклад cat.png; music.mp3; video.mp4; folder; )
* /Start_Upload активовує фунцію яка дозволяє завантажувати різні документи, фото, відео, аудіо. В відкритій на даний момент директорії. Директорію можна дізнатись за допомогою кнопки /dir.
* /Stop_Upload зупиняє роботу функції для завантаження файлів.

 РЕДАГУВАННЯ ПРОГРАМИ ТА КОНВЕРТУВАННЯ В ЕКСЕШНИК

Якщо ви хочете редагувати програму, то вам потрібно завантажити собі python (не беріть найновіші версії обирайте більш стабільні версії наприклад python 3.10) встановіть pip install завантажте всі зазначені в програмі бібліотеки "import (назва бібліотеки)" список основних бібліотек: Для роботи програми треба встановити бібліотеки Python:

* os
* mss
* subprocess
* telebot
* ReplyKeyboardMarkup, KeyboardButton
* requests
* types
* StringIO
* sys
* time
* traceback
* threading
* util
* config
* keyboard
* ctypes

Якщо виникла помилка з розряду такої зверніть увагу що там пишеться: ![image](https://github.com/SunsetTekila/TelegramRemoteControl_DynamicConfig/assets/157602307/5f74bd0f-5856-498b-a5b6-9ea015061a4e)
причиною може бути недостаюча бібліотека, щоб встановити бібліотеку, вам потрібно написати в командній строці pip install "назва бібліотеки" 
у вище показаній ситуації треба ввести pip install mss

Щоб встановити бібліотеку в командній строці (її можна відкрити в меню пуск написаши cmd в пошук) пишіть pip install назва бібліотеки ще вам треба буде встановити pyinstaller через pip install коли все буде працювати в командній строці прейдіть в файл з кодом та введіть команду pyinstaller --noconfirm --onefile --windowed (назва програми.py) (назва config.py) в папці dist буде ваша програма в форматі exe

Решта інформації знаходиться в файлах у вигляді docx документів з інструкціями в папці "main"


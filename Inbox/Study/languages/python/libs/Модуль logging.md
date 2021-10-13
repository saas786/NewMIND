


Мощный модуль для составления логгов 
`import logging`

Для правильной работы нужно определить свой собственный **logger**, создав объект класса **Logger**, особенно если ваше приложение имеет несколько модулей. Давайте посмотрим на некоторые классы и функции в модуле.

-   **`Logger`:** Это класс, чьи объекты будут использоваться в коде приложения напрямую для вызова функций.
-   **`LogRecord`:** Logger автоматически создает объект **LogRecord**, в котором находиться вся информация, относящаяся к регистрируемому событию, например, имя логера, функции, номер строки, сообщение и т. д. 
-   **`Handler`:** Обработчики отправляют **LogRecord** в требуемое место назначения вывода, такое как консоль или файл. Обработчик является основой для подклассов, таких как **StreamHandler**, **FileHandler**, **SMTPHandler**, **HTTPHandler** и других. Эти подклассы отправляют выходные данные журнала соответствующим адресатам, таким как **sys.stdout** или файл на диске.
-   **`Formatter`:** Здесь вы указываете формат вывода, задавая строковый формат, в котором перечислены атрибуты, которые должны содержать выходные данные.

```
import logging


\# Create a custom logger

logger = logging.getLogger(\_\_name\_\_)

\# Create handlers

c\_handler = logging.StreamHandler()

f\_handler = logging.FileHandler('file.log')

c\_handler.setLevel(logging.WARNING)

f\_handler.setLevel(logging.ERROR)

\# Create formatters and add it to handlers

c\_format = logging.Formatter('%(name)s - %(levelname)s - %(message)s')

f\_format = logging.Formatter('%(asctime)s - %(name)s - %(levelname)s - %(message)s')

c\_handler.setFormatter(c\_format)

f\_handler.setFormatter(f\_format)

\# Add handlers to the logger

logger.addHandler(c\_handler)

logger.addHandler(f\_handler)

logger.warning('This is a warning')

logger.error('This is an error')


```

У модуля есть 5 уровней 
```

-   DEBUG
-   INFO
-   WARNING
-   ERROR
-   CRITICAL

```

```
import logging

logging.debug('This is a debug message')

logging.info('This is an info message')

logging.warning('This is a warning message')

logging.error('This is an error message')

logging.critical('This is a critical message')

Вывод 

WARNING:root:This is a warning message

ERROR:root:This is an error message

CRITICAL:root:This is a critical message

выводит только critical error and warning

```

Изменить уровень вывода `logging.basicConfig(level=logging.DEBUG)`

Запись в файл а не в консоль с помощью filename с ключом **w** - перезапись или с ключом **a** добавление

```

import logging

logging.basicConfig(filename='app.log', filemode='w', format='%(name)s - %(levelname)s - %(message)s')

logging.warning('This will get logged to a file')

```


**Формат Вывода**

с помощью format выводит разные типы логов

`logging.basicConfig(format='%(process)d-%(levelname)s-%(message)s', datefmt='%d-%b-%y %H:%M:%S')`

datefmt='%d-%b-%y %H:%M:%S' -тек. время в указаном формате


+ %(asctime)s - текущее время
+ %(message)s' - текст ошибки
+ %(levelname)s - уровень ошибки
+ %(process)d - текущий id процесса


# Логирование переменных #

```

import logging

name = 'John'

logging.error(f'{name} raised an error')

ВЫВОД

ERROR:root:John raised an error

```



# Логирование в блоке try Expect #

c помощью метода **logging.exception()**

```
import logging

a = 5

b = 0

try:

c = a / b

except Exception as e:

logging.exception("Exception occurred")


ВЫВОД

ERROR:root:Exception occurred

Traceback (most recent call last):

File "exceptions.py", line 6, in <module\>

c = a / b

ZeroDivisionError: division by zero

\[Finished in 0.2s\]

```

[[Словарь по python]]
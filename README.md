# Задание №1
## Выбран сервис http://mail.google.com/

    Gmail - почтовый сервис от компании Google. 
    Предоставляет услуги по пересылке, получению и хранению электронных сообщений.
    
## Декомпозировать функционал сервиса на блоки функционала, если необходимо, в каждом блоке выделить подблоки 

    Для авторизованного пользователя:

    Блоки, подблоки:
    1. Поисковая строка - сверху
    2. Меню - слева
      2.1. Написать сообщение
      2.2. Отображение сообщений
        2.2.1. Входящие
        2.2.2. Помеченные
        2.2.3. Важные
        2.2.4. Отправленные
        2.2.5. Черновики
        2.2.6. Круги
        2.2.7. Ещё
          2.2.7.1. Чаты
          2.2.7.2. Вся почта
          2.2.7.3. Спам
          2.2.7.4. Корзина
          2.2.7.5. Категории
      2.3. Настройки ярлыков
        2.3.1. Управление ярлыками
        2.3.2. Создать ярлык
    3. Чат - слева снизу
      3.1. Поиск людей
      3.2. Начать чат
    4. Сообщения - по-центру
      4.1. Фильтры сообщений
        4.1.1. Фильтры, отвечающие за выделение сообщений
        4.1.2. Фильтры, отвечающие за выбор группы (несорированные, соцсети, и т.д.)
        4.1.3. Переход на следующую/предыдущую страницу с сообщениями
        4.1.4. Выбор сообщения для просмотра
      4.2. Статусы сообщений
        4.2.1. Выделено сообщение или нет
        4.2.2. Помечено сообщение, как избранное, или нет
        4.2.3. Помечено сообщение, как важное, или нет
        4.2.4. Наличие вложенных файлов
      4.3. Автор сообщения/участники переписки
      4.4. Заголовок сообщения
      4.5. Дата получения сообщения
    5. Настройки профиля - справа сверху
      5.1. Имя пользователя
      5.2. Приложния Google
        5.2.1. Мой аккаунт
        5.2.2. Поиск
        5.2.3. Карты
        5.2.4. YouTube
        5.2.5. Play
        5.2.6. Новости
        5.2.7. Почта
        5.2.8. Диск
        5.2.9. Календарь
        5.2.10. Google+
        5.2.11. Переводчик
        5.2.12. Фотографии
        5.2.13. Ещё
          5.2.13.1. Документы
          5.2.13.2. Blogger
          5.2.13.3. Контакты
          5.2.13.4. Другие сервисы Google
      5.3. Оповещения Google
      5.4. Настройки аккаунта
    6. Дополнительные ссылки - снизу
      6.1. Информация об использованном пространстве
      6.2. Условия, конфиденциальность
      6.3. Дополнительная информация

## Оформить в виде MindMap

    Ссылка на MindMap
    https://www.mindmeister.com/606664072#

# Задание №2
## Для выполнения данного задания выбран блок "Написать сообщение" из предыдущего задания.

    То есть тестируется функционал отправки сообщений. Данный функционал состоит из следующих подблоков:
      1. Формирование сообщений
        1.1. Получатели
        1.2. Тема сообщения
        1.3. Текст сообщения
        1.4. Вложенные файлы
      2. Назначение сообщения
        2.1. Отправка сообщения
        2.2. Сохранение в черновиках
        
      Тестирование 1 подблока:
      
      1. Подблок "Формирование собщений":
          1.1. Получатели. 
          Имя каждого получателя должно соответствовать следующему формату: <строка1>@<строка2>.<строка3>, где строка1, строка2 и строка3 не являются пустыми строками и не содержат специальных символов.
          Имена получателей должны разделяться через символ ','.
          Используем технику разделения на классы: 
          - введенное поле соответсвует формату;
          - введенное поле не соответсвует формату.
          Несоответствие формату дополнительно можно разбить на: 
          - отсутствие одного или обоих из символов '@', '.' в имени одного из получателей;
          - есть строка, содержащая специальные символы в имени одного из получателей;
          - есть пустая строка в имени одного из получателей.
          По количеству получателей можно разбить на:
          - нет получателей;
          - один получатель;
          - несколько имен получателей (>1).
          
        1.2. Тема сообщения
          Должена быть указана тема сообщения, которая состоит из любого набора символов. Кроме того, если тема сообщения является пустой строкой, то она автоматически заменяется на <без темы>.
          Используем технику разделения на классы: 
          - введенное поле не пустая строка;
          - введенное поле пустая строка.
          
        1.3. Текст сообщения
          Текст сообщения дожным вводиться именно так, как это хочет видеть пользователь. Необходимо:
          - убедиться в том, что нет ограничений на длину текста; 
          - кликабельные ссылки подсвечиваются, и при нажатии на них осуществляется переход;
          - смайлики вставляются корректно.
          Также необходимо проверить различные варианты форматирования текста:
          - без форматирования;
          - различные варианты шрифта;
          - размер текста;
          - цвет текста;
          - жирный шрифт;
          - курсив;
          - подчеркнутый шрифт;
          - выравнивание по левому краю;
          - выравнивание по центру;
          - выравнивание по правому краю;
          
        1.4. Вложенный файлы
          Вложенные файлы необходимо протестировать относительно их веса и формата. 
          Разбиение на классы (и граница между классами) относительно веса файла:
          - файлов меньшего размера, чем максимально допустимый;
          - файлов большего размера, чем максимально допустимый;
          - размер файла близок к верхней границе, но не превышает её.
          Разбиение на классы относительно формата файла:
          - архив;
          - аудиофайл;
          - видеофайл;
          - документ;
          - изображение;
          - исполняемый файл.
          
      Тестирование 2 подблока:
      
      2. Подблок "Назначение сообщения":
        2.1. Отправка сообщения
          Для того, чтобы проверить эту функцию, необходимо все тесты из подблока "Формирование собщений".
        2.2. Сохранение в черновиках
          Для того, чтобы проверить эту функцию, достаточно проверить тесты из подблоков "Тема сообщения", "Текст сообщения", "Вложенные файлы". Тесты из подблока "Получатели" нет необходимости проверять, потому что при сохранении в чернивиках это поле не подвергается проверке.
      
      Тесты занесены в ТестРейл.


# V380-Web
Web server for ip cameras V380.  

The HTTP server allows you to:
- perform all sorts of manipulations with the records on the sd card. Now you do not need to take it out of the camera every time;
- watch the video archive on sd online without removing the card;
- display camera information;
- launch services (RTSP, telnet, HTTP);
- restart and safely shut down the camera before turning off the power.  

HTTP-сервер позволяет:
- производить всевозможные манипуляции с записями на sd-карте. Теперь вынимать её из камеры каждый раз вам нет необходимости;
- смотреть видео-архив на sd онлайн, не вынимая карты;
- отображать сведения о камере;
- производить запуск служб (RTSP, telnet, HTTP);
- перезагружать и безопасно завершать работу камеры перед отключением питания.

Для каждой модели камеры с разными Hwname/Soft-id свой установщик. Вы должны знать этот код. Но если ошибетесь — ничего страшного... патч будет игнорирован. Никаких изменений в камере не производится. Только обеспечивается запуск командного файла на sd в папке ark-add-on — startup.sh, если этот запускной файл есть на карте. Ваша базовая прошивка может быть самой последней. Вся установка происходит на sd-карту. Если после установки очистить или вынуть sd, то камера будет работать в обычном режиме, как работала до установки. Для подготовки установщика к новым моделям — сообщите её Hwname. Узнать Hwname можно по трафику с камеры в момент захода на смартфоне в пункт "версия прошивки". Также можно определить Hwname, если взять скриншот с экрана смартфона при отображении информации о выходе новой прошивки по её идентификатору.

Установка:
1. Отформатировать sd-карту в FAT32.
2. Записать в корень карты содержимое архива в составе:
- ark-add-on
- updatepatch
- local_update.conf
- patch_reuse
3. Вставить карту в камеру и включить её... ждать пару минут. Камера должна перезагрузится. После чего можно заходить с помощью обозревателя интернета на адрес камеры.  

Installation:
1. Format the sd card to FAT32.
2. Write to the root of the sd-card the contents of the archive as part of:
- ark-add-on
- updatepatch
- local_update.conf
- patch_reuse
3. Insert the card into the camera and turn it on... wait a couple of minutes. The camera should reboot. After that, you can use the Internet browser to access the address of the camera.  

![Просмотр папок с записями](Screenshots/image_2021_05_30T07_36_48_243Z.png?raw=true)

---
$title@: Razrabotka-android-prilozheniya-vvedenie
author@: Viktor Zharina
$order: 25
$dates:
  published: 2012-09-12 06:04:26
---
<h1>Предисловие</h1>

Не так давно я обзавелся планшетом Ritmix RMD-1030 c ОС Android 4.0. Планшет, в основном, использую для серфинга интернета и чтения электронных книг. Не так давно на стационарном ПК я обнаружил документ, в котором составлен список лекарств, где напротив названия указана дата окончания срока годности. Периодически я анализирую этот список и выбрасываю лекарства с истекшим сроком годности. Проблема заключается в том, что этим списком я пользуюсь значительно реже, чем планшетом и лекарства с истекшим сроком годности копятся и оперативно не заменяются. Мне захотелось автоматизировать этот процесс и написать приложение для планшета, которое будет сверять текущую дату с датой окончания срока годности и уведомлять меня в случае если срок годности истек каждый раз, когда я запускаю приложение.

В данном посте я постараюсь ввести в курс дела и коротко рассказать о том, что необходимо для того, чтобы приступить к написанию приложения.

<!--more-->

Я не буду описывать процессы установки ПО и приводить куски кода, потому что данной информации и так полно в сети. Вместо этого я попробую расширить кругозор человека, который также как и я ни разу не писал приложения для мобильных устройств для того, чтобы он смог приступить к разработке.



<h1> Сокращения и определения</h1>

<a href="http://ru.wikipedia.org/wiki/Android" target="_blank">Android</a>

<a href="http://ru.wikipedia.org/wiki/Dalvik_virtual_machine" target="_blank">Dalvik Virtual Machine или просто Dalvik</a>

Android SDK - обеспечивает разработчика библиотеками и утилитами необходимыми для разработки, тестирования и отладки приложения для Android.

Эмулятор Android - программа, которая позволяет воспроизвести работу устройства на базе Android на вашей рабочей станции. Основана на quemu.

<a href="http://ru.wikipedia.org/wiki/Java_Virtual_Machine" target="_blank">Java_Machine</a>

<a href="http://ru.wikipedia.org/wiki/Java" target="_blank">Java</a>

<a href="http://ru.wikipedia.org/wiki/Eclipse_(%D1%81%D1%80%D0%B5%D0%B4%D0%B0_%D1%80%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B8)" target="_blank">Eclipse</a>



<h1>Общие сведения</h1>

Приложение под Android может быть написано на языке java. Для запуска и работы приложения ОС использует виртуальную машину Dalvik. Данная виртуальная машина это оптимизированная версия Java машины.



Код приложения может быть написан в любом текстовом редакторе, однако можно использовать среду разработки, например, <a href="http://www.eclipse.org/downloads/packages/eclipse-ide-java-ee-developers/junor" target="_blank">Eclipse</a>, которая специально сделана для того, чтобы писать код было удобнее и быстрее. В среде пишется код приложения, который далее преобразуется в программу, которую можно запустить на самом устройстве или в эмуляторе, который входит в состав <a href="http://developer.android.com/sdk/index.html target="_blank"">Android SDK</a>.



Про программный стек и архитектуру можно прочитать в статье "<a href="http://android-shark.ru/arhitektura-operatsionnoy-sistemyi-android/" target="_blank">Архитектура операционной системы Android</a>" или в книге "Разработка приложений для Android" (С. Хашими, С. Коматинени, Д. Маклинг, 2011).



Много дополнительной информации предоставляет <a href="http://developer.android.com/" target="_blank">http://developer.android.com/</a>



<h1>Заключение</h1>

В данном посте я постарался кратко ввести в курс дела. Дал общую информацию об операционной системе и инструменте, с помощью которого можно приступить к разработке приложения. В следующем посте я опубликую требования к разрабатываемому приложению и представлю прототип интерфейса.






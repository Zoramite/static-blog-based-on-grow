---
$title@: Interfejs-rs-485-sxemy-podklyucheniya-rekomendacii-po-rabote-s-dlinnymi-liniyami-rekomendacii-po-prokladke
author@: Viktor Zharina
$order: 44
$dates:
  published: 2013-02-05 08:48:20
---
Интерфейс RS-485 - широко распространенный высокоскоростной и помехоустойчивый промышленный последовательный интерфейс передачи данных. Практически все современные компьютеры в промышленном исполнении, большинство интеллектуальных датчиков и исполнительных устройств, программируемые логические контроллеры наряду с традиционным интерфейсом RS-232 содержат в своем составе ту или иную реализацию интерфейса RS-485. Интерфейс RS-485 основан на стандарте EIA RS-422/RS-485. К сожалению, полноценного эквивалентного российского стандарта не существует, поэтому в данном разделе предлагаются некоторые рекомендации по применению интерфейса RS-485.



Традиционный интерфейс RS-232 в промышленной автоматизации применяется достаточно редко. Сигналы этого интерфейса передаются перепадами напряжения величиной (3…15) В, поэтому длина линии связи RS-232, как правило, ограничена расстоянием в несколько метров из-за низкой помехоустойчивости. Интерфейс RS-232 имеется в каждом PC – совместимом компьютере, где используется в основном для подключения манипулятора типа “мышь”, модема, и реже – для передачи данных на небольшое расстояние из одного компьютера в другой. Передача производится последовательно, пословно, каждое слово длиной (5…8) бит предваряют стартовым битом и заканчивают необязательным битом четности и стоп-битами. Интерфейс RS-232 принципиально не позволяет создавать сети, так как соединяет только 2 устройства (так называемое соединение “точка - точка”).



[caption id="attachment_524" align="aligncenter" width="484"]<img class="size-medium wp-image-524" alt="rs232 to PC" src="http://viktor.zharina.info/wp-content/uploads/2013/02/rs232-300x43.jpg" width="484" height="68" /> rs232 to PC[/caption]



Сигналы интерфейса RS-485 передаются дифференциальными перепадами напряжения величиной (0,2…8) В, что обеспечивает высокую помехоустойчивость и общую длину линии связи до 1 км (и более с использованием специальных устройств – повторителей. Кроме того, интерфейс RS-485 позволяет создавать сети путем параллельного подключения многих устройств к одной физической линии (так называемая “мультиплексная шина”).

<!--more-->



В обычном PC-совместимом персональном компьютере (не промышленного исполнения) этот интерфейс отсутствует, поэтому необходим специальный адаптер - преобразователь интерфейса RS-485/232.



[caption id="attachment_525" align="aligncenter" width="300"]<img class="size-medium wp-image-525" alt="rs485" src="http://viktor.zharina.info/wp-content/uploads/2013/02/rs485-300x105.jpg" width="300" height="105" /> rs485[/caption]



Существуют преобразователи двух видов:

<ul>

	<li>преобразователи, требующие жесткого указания скорости обмена и длины передаваемого слова (с учетом стартовых, стоповых бит и бита четности) для расчета времени окончания передачи: например, преобразователь ADAM-4520 производства компании Advantech. Все параметры задаются переключателями в самом преобразователе, причем для задания этих параметров корпус преобразователя необходимо разобрать;</li>

	<li>преобразователи на основе технологий “Self Tuner” и им подобных, не требующие никаких указаний вообще, и, соответственно, не имеющие никаких органов управления: например, преобразователь I-7520 производства компании ICP DAS.</li>

</ul>

В автоматических преобразователях выходы интерфейса RS-485 обычно имеют маркировку “DATA+” и “DATA-“. В I-7520 и ADAM-4520 вывод “DATA+” функционально эквивалентен выводу “A”, вывод “DATA-“ - выводу “B”.



Подключение преобразователей интерфейса ADAM-7520 и I-7520 к порту RS-232 осуществляется так называемым “модемным” кабелем. Преобразователь имеет 9-контактный разъем (DB9, гнездо), персональный компьютер может иметь разъемы как 9-контактные (DB9, штырь), так и 25-контактные (DB25, штырь). Для 9-контактного разъема распайка кабеля осуществляется “один в один”, то есть RX к RX, TX к TX и т.д. Этот стандартный кабель производится многими изготовителями. Автоматическим преобразователям, как правило, достаточно линий к контактам 2,3 и 5.



Устройства, подключаемые к интерфейсу RS-485, характеризуются важным параметром по входу приемопередатчика: “единица нагрузки” (“Unit Load” - UL). По стандарту в сети допускается использование до 32 единиц нагрузки, т.е. до 32 устройств, каждое из которых нагружает линию в 1 UL. В настоящее время существуют микросхемы приемопередатчиков с характеристикой менее 1 UL, например - 0,25 UL. В этом случае количество физически подключенных к линии устройств можно увеличить, но суммарное количество UL в одной линии не должно превышать 32.



В качестве линии связи используется экранированная витая пара с волновым сопротивлением ≈120 Ом. Для защиты от помех экран (оплетка) витой пары заземляется в любой точке, но только один раз: это исключает протекание больших токов по экрану из-за неравенства потенциалов “земли”. Выбор точки, в которой следует заземлять кабель, не регламентируется стандартом, но, как правило, экран линии связи заземляют на одном из ее концов.



[caption id="attachment_529" align="aligncenter" width="300"]<img class="size-medium wp-image-529" alt="Заземление_экрана" src="http://viktor.zharina.info/wp-content/uploads/2013/02/zazemlenie_ekrana-300x60.jpg" width="300" height="60" /> Заземление_экрана[/caption]



Устройства к сети RS-485 подключаются последовательно, с соблюдением полярности контактов A и B.



[caption id="attachment_530" align="aligncenter" width="300"]<img class="size-medium wp-image-530" alt="Подключение нескольких устройств rs 485" src="http://viktor.zharina.info/wp-content/uploads/2013/02/rs485_neskolko_ustroistv-300x84.jpg" width="300" height="84" /> Подключение нескольких устройств rs 485[/caption]



Как видно из рисунка, длинные ответвления (шлейфы) от магистрали до периферийных устройств не допускаются. Стандарт исходит из предположения, что длина шлейфа равна нулю, но на практике этого достичь невозможно (небольшой шлейф всегда имеется внутри любого периферийного устройства: от клеммы до микросхемы приемопередатчика).



Качество витой пары оказывает большое влияние на дальность связи и максимальную скорость обмена в линии. Существуют специальные методики расчета допустимых скоростей обмена и максимальной длины линии связи, основанные на паспортных параметрах кабеля (волновое сопротивление, погонная емкость, активное сопротивление) и микросхем приемопередатчиков (допустимые искажения фронта сигнала). Но на относительно низких скоростях обмена (до 19200 бит/с) основное влияние на допустимую длину линии связи оказывает активное сопротивление кабеля. Опытным путем установлено, что на расстояниях до 600 м допускается использовать кабель с медной жилой сечением 0,35 мм (например, кабель КММ 2х0,35), на большие расстояния сечение кабеля необходимо пропорционально увеличить. Этот эмпирический результат хорошо согласуется с результатами, полученными расчетными методами.



Даже для скоростей обмена порядка 19200 бит/с кабель уже можно считать длинной линией, а любая длинная линия для исключения помех от отраженного сигнала должна быть согласована на концах. Для согласования используются резисторы сопротивлением 120 Ом (точнее, с сопротивлением, равным волновому сопротивлению кабеля, но, как правило, используемые витые пары имеют волновое сопротивление около 120 Ом и точно подбирать резистор нет необходимости) и мощностью не менее 0,25 Вт – так называемый “терминатор”. Терминаторы устанавливаются на обоих концах линии связи, между контактами A и B витой пары.



В сетях RS-485 часто наблюдается состояние, когда все подключенные к сети устройства находятся в пассивном состоянии, т.е. в сети отсутствует передача и все приемопередатчики “слушают” сеть. В этом случае приемопередатчики не могут корректно распознать никакого устойчивого логического состояния в линии, а непосредственно после передачи все приемопередатчики распознают в линии состояние,  соответствующее последнему переданному биту, что эквивалентно помехе в линии связи. На эту проблему не так часто обращают внимания, борясь с ее последствиями программными методами, но тем не менее решить ее аппаратно несложно. Достаточно с помощью специальных цепей смещения создать в линии потенциал, эквивалентный состоянию отсутствия передачи (так называемое состояние “MARK”: передатчик включен, но передача не ведется). Цепи смещения и терминатор реализованы в преобразователе I-7520. Для корректной работы цепей смещения необходимо наличие двух терминаторов в линии связи. В сети RS-485 возможна конфликтная ситуация, когда 2 и более устройства начинают передачу одновременно. Это происходит в следующих случаях:

<ol>

	<li>в момент включения питания из-за переходных процессов устройства кратковременно могут находится в режиме передачи;</li>

	<li>одно или более из устройств неисправно;</li>

	<li>некорректно используется так называемый “мультимастерный” протокол, когда инициаторами обмена могут быть несколько устройств.</li>

</ol>

В первых двух случаях быстро устранить конфликт невозможно, что теоретически может привести к перегреву и выходу из строя приемопередатчиков RS-485. К счастью, такая ситуация предусмотрена стандартом и дополнительная защита приемопередатчика обычно не требуется. В последнем случае необходимо предусмотреть программное разделение канала между устройствами - инициаторами обмена, так как в любом случае для нормального функционирования линия связи может одновременно предоставляться только одному передатчику.



При создании материала очень активно использовал информацию из <a href="http://contravt-metodichka.ru/?id=3937" target="_blank">методички компании Контрафт</a>
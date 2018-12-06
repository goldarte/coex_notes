# Расшифровка полётных логов с APM

В связи с событиями 3х-месячной давности \(один коптер из 9 роевых разбил машину\) мне нужно общаться со страховой, директором ВИСТ моторс, нашим юристом и т.д. 

Страховая запросила логи и их расшифровку, а я ни разу не работал с APM логами. Что же, шанс появился.

Итак, обзор методов и средств для анализа APM логов.

1. Mission Planer. Имеет встроенный интерфейс для построения графиков, отображает сообщения, ошибки и полётные режимы на таймлайне, пытается показать карту с точками полёта \(не загружается\). 
   Есть инструкция по анализу: [http://ardupilot.org/copter/docs/common-diagnosing-problems-using-logs.html](http://ardupilot.org/copter/docs/common-diagnosing-problems-using-logs.html "ссылка")  
   Однако мне эта тулза не понравилась: графики отображаются неудобно, больше полэкрана занимает отображение сообщений лога в сыром формате \(зачем?\), их нельзя скрыть или уменьшить по ширине, карта не грузит картинку со спутника.  
   ![](/assets/Снимок.PNG)

2. MAVExplorer. Это дополнительный инструмент, поставляемый вместе с MAVProxy \([https://github.com/ArduPilot/MAVProxy](https://github.com/ArduPilot/MAVProxy "MAVProxy")\). Выглядит как GUI + консольный интерфейс, если проще, то генерит столько окошек, сколько требуется для полного анализа. Позволяет достаточно гибко отображать графики из разных источников, отображает путь коптера на карте, имеет парочку фич \(показ сообщений и работа с функциями от отображаемых данных\). Уже симпатичнее.  
   Для него тоже есть документация: [http://ardupilot.org/dev/docs/using-mavexplorer-for-log-analysis.html](http://ardupilot.org/dev/docs/using-mavexplorer-for-log-analysis.html)  
   ![](/assets/Снимок2.PNG)

3. Утилиты MAVProxy. Наткнулся здесь: [https://erlerobotics.gitbooks.io/erle-robotics-mav-tools-free/content/en/index.html  
   ](https://erlerobotics.gitbooks.io/erle-robotics-mav-tools-free/content/en/index.html)Позволяют проделывать ещё кое-что с данными логов. Мне, например, пригодился скрипт mavtogpx, который данные по GPS позиции конвертнул в GPX формат, который можно загрузить в Google Earth, например \(предварительно конвертнув .gpx в .kml через [https://gpx2kml.com](https://gpx2kml.com)\).  





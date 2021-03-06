## Риски реализации ##
Основные риски (бизнес, технические), владельцы рисков.

### Стек технологий и кадры
Владельцы: **IT, HR**

**Дефицит специалистов на проекте** (бекенд-разработчики, разработчики мобильных приложений, фулл-стек разработчики), работающих с выбранным стеком технологий. Причины: увольнение, дефицит кадров на рынке, обширная требуемая область знаний (работа с контейнерами, гит, брокером, api и т.д.). 

_Минимизация риска_: разграничение разработки на дробный конкретный стек технологий, ограничение кол-ва используемых инструментов и технологий на позиции, выбор широкоиспользуемых и недорогих (для кадров) технологий.

### Отсутствие требований к разрабатываемым функциям
Владельцы: **Маркетинг, Продажи**

Проблема получения обратной связи от стейкхолдеров может затормозить разработку или направить её не по тому пути. Особенно это важно на старте проекта, когда собираются требования от всех заинтересованных лиц. Может случиться так, что какое-то лицо не учли, не занесли в требования важный пункт (например, требования регулятора относительно хранения и обработки персональных данных).

_Минимизация риска_: SMART задачи стейкхолдеров, назначение ответственных.

### Ошибки проектирования инфраструктуры
Владельцы: **IT**

Плохо спроектированная и проработанная структура, может оказать крайне негативное влияние на проект (от затягивания сроков, до невозможности запуска в эксплуатацию). 

_Минимизация риска_: детальная проработка (на разных уровнях детализации) инфраструктуры, тщательный подбор компонентов и технологий (модули, плагины, sdk, фреймворки), их совместимость, поддерживаемость, отказоустойчивость, возможность запуска в целевой среде выполнения. Так же фактором, позволяющим снизить риск, является запуск пилотных версий, "демок", концептов. На таком этапе запуска могут вылезти проблемы с которыми можно столкнуться только на этапе эксплуатации ПО. 

### Ошибки планирования
Владельцы: **IT**

Неверно составленный план-график и бюджет проекта так же может оказать негативное влияние: недостаточно заложили денег в бюджет (зп не по рынку), требуется покупать ресурсы (сервера, хостинг, облако), требуется покупка или лицензирование ПО (IDE, сервер БД, фреймворки, шина данных), требуется ресурс для поддержки используемых технологий (брокер, шина, кубернетес).

_Минимизация риска_: привлечение опытного прожект-менеджера в команду, работа по всем областям знаний и этапов проекта (по PMBOK).

### Внешние угрозы, доступ к внешним сервисам
Владельцы: **IT**

Доступ к арендуемой инфраструктуре может быть ограничен или прекращен всвязи с внешними факторами (политический фактор). Всвязи с этим, могут быть проблемы к работе с провадерами облачных услуг. 

_Минимизация риска_: проектирование и разработка ПО таким образом, что бы инфраструктуру можно было "развернуть" на своих ЦОДах: конфигурации kubernetes должны быть совместимы и разворачиваться на внутренних серверах. Предусмотреть полуавтоматический режим с использованием специализированного ПО (например terraform). Дистрибутивы ПО, пакеты и библиотеки, бекапы так же должны быть локально сохранены (идеальный вариант - внутренний репозиторий (Gitlab registry)). Т.к. приложением могут пользоваться по всему миру, необходимо продумать возможность (и оценить реализуемость) "локального" использования в отдельных странах (в рамках локдауна).

## Функциональные требования


**Реализация персональной составляющей приложения**

Реализовать сбор и хранение, синхронизацию персональных данных: предпочтения, тренировки, данные пользователя, подписки, настройки приложения, бонусный счет пользователя. Реализовать авторизацию через соцсети (facebook, google, vk).

**Реализация функции геймификации приложения**

Реализация небольших игр, квестов или маркетинговых активностей, направленных на получения “вознаграждения” в виде бонусных баллов: подписка на новости, заполнение информации о себе(профиля), установка других приложений, покупка продукции компании, участие/победа в соревнованиях.

**Реализация маркетинговой составляющей**

Отображение рекламных блоков, баннеров, новостей, специализированных акций (по предпочтениям). 


## Нефункциональные требования


**Интеграция с приложениями**

Доступ к данным других приложений должен осуществляться через тот же API шлюз, к которому подключено данное приложение (посредством REST-запросов). Доступ к другим приложениям определяется моделью доступа ABAC. Авторизация и аутентификация происходит на уровне API Gateway. Предпочтения загружаются и формируются отдельно на стороне бэкенда под конкретного пользователя (через REST запрос)

**Интеграция функций телефона**

Приложение должно получать необходимые данные из текущей операционной системы (Android Fitness/iOS Health APIs)

**Реализация социальной составляющей приложения**

Необходимо реализовать поставку (REST-запросы к API Gateway) и локальное хранение социальных данных: news, groups, competitions, friendships, maps, places, tracks. И реализован поиск по данным сущностям в API.
# Цели 
- Основаная цель написания данного приложения - изучить технологии которые я не затрагивал в ходе обучения на курсах в SkyPro
- Хотелось попробовать написать, что-то на архитектуре микросервисов, с некоторыми интеграционными решениями
  
# Интеграции
- Приложение интегрировано с OpenCage Geocoding API - для поиска квартир по геолокации
- Приложение интегрировано  с Openweathermap API - для предоставления данных о погоде
- Yandex mail API  - для email рассылки пользователей

# Структура 
- rent-application-microservices - внешний проект в котором лежат все остальные модули
- rent-server - Eureka Server - сервер на котором запускаются все клиенты
- rent-config-server - позволяет хранить настройки конфигурации сервисов в git-репозитории
- rent-utils - вспомогательны модуль в котором лежат общие компаненты для всех клиентов
- rent-gateway - для маршрутизации к API 
- rent-flat-sharing - клиент с основной логикой приложения, с базой данных квартир, адресов, юзеров
- rent-info - клиент со своей отдельной базой данных, в которой хранится общая информация
- Сервисы rent-flat-sharing и rent-info - общаются между собой с помощью RestTemplate

# Используемые технологии
Основной проект:
- Java 17
- Maven
- Spring Boot
- Spring Web
- Spring Data JPA
- Spring Security
- Spring Cloud
- Swagger
- Lombok
- 
# Работа БД:
- PostgreSQL
- Flyway

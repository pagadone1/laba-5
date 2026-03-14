# Настройка PO5

## 1. База данных (pgAdmin)

```sql
CREATE DATABASE carservice;
```

## 2. Запуск приложения

```bash
cd demo
mvn spring-boot:run
```

## 3. Postman

1. Импорт: `postman/Car-Service-PO5.postman_collection.json` и `postman/Car-Service-PO5.postman_environment.json`
2. Выбрать окружение **PO5 local**
3. **Порядок запросов:**
   - **1. Register** → Send (создать пользователя)
   - **2. Login** → Send (получить токены)
   - **Если токены не сохранились** — Car Service PO5 → Edit → Variables → вставить accessToken вручную в Current Value
   - **Create customer**, **Create mechanic** и т.д. → Send (токен подставится автоматически)

## 4. Переменные

- `baseUrl`: http://localhost:8080
- `username`: admin
- `password`: SecurePass1!
- `accessToken` — вставить после Login (если скрипт не сохранил)

# Test task

### Запуск:
```bash
git clone https://github.com/s1kle/test-case
cd test-case
docker-compose up -d
```

### Проверка результата:
```bash
curl http://localhost
```

### Схема работы:
1. nginx слушает запросы на порту 80
2. запрос передается на backend по внутренней сети Docker
3. fastapi обрабатывает запрос
4. ответ возвращается через nginx обратно на клиента

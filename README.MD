Инструкция

1. Подготовить сервер. ОС Ubuntu 22.04 LTS
2. Установить Docker engine https://docs.docker.com/engine/install/ubuntu/
3. Установить gdown https://github.com/wkentaro/gdown
4. Скачать снапшот с гугл диска ```python3 -m  "gdown" https://drive.google.com/uc?id=12EC3s5GDmrIWfq5jWwaKYmW9DXzIyId1```
5. Распакавать снапшот ```tar -xzf node.tar.gz ```
6. Вставить в файл node.env приватный ключ от валидатора
7. Поднять контейнер командой ```sudo docker compose up -d```
8. Проверить, что нода работает ```curl http://<ip сервера>:8546 \
   -X POST \
   -H "Content-Type: application/json" \
   --data '{"method":"eth_chainId","params":[],"id":1,"jsonrpc":"2.0"}'```
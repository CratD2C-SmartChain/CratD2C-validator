Инструкция

1. Подготовить сервер. ОС Ubuntu 22.04 LTS
2. Установить Docker engine https://docs.docker.com/engine/install/ubuntu/
3. Скачать снапшот в текущую папку ```curl -O https://staking-testnet.cratd2csmartchain.io/downloads/node.tar.gz```
4. Распакавать снапшот ```tar -xzf node.tar.gz ```
5. Вставить в файл node.env приватный ключ от валидатора
6. Поднять контейнер командой ```sudo docker compose up -d```
7. Проверить, что нода работает ```curl http://<ip сервера>:8546 \
   -X POST \
   -H "Content-Type: application/json" \
   --data '{"method":"eth_chainId","params":[],"id":1,"jsonrpc":"2.0"}'```
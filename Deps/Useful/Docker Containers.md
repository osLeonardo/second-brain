- **RabbitMq**
>docker run -d --name rabbitmq -p 5672:5672 -p 15672:15672 --hostname rabbitmq-master rabbitmq:3-management

- **Redis**
>docker run --name redis -p 6379:6379 -d redis:7-alpine

- **Redis CLI (rdcli)**
>npm install redis-cli -g

- **Limpar Cache do Banco do Redis**>
>***Banco Local***
>rdcli
>flushall
>
>***Banco QA***
>rdcli -h 64.227.104.246
>flushall
>
>![[RedisCache.png]]
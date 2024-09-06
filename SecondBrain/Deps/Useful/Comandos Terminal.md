#### Docker
- **Docker Compose**
>Atualizar: 
>
>	docker compose pull
>Parar:
>
>	docker compose down
>Iniciar:
>
>	docker compose up -d --remove-orphans --force-recreate
>Iniciar específico:
>
>	docker compose up -d [container-name] --force-recreate
>Remove unused or dangling contaners, images and volumes:
>
>	docker system prune -a
>Remove dangling Images:
>
>	docker image prune


- **Erros do Docker**
>Erro 125 - No powershell do Visual Studio:
>
>	docker network create portal-net
>Não funciona de jeito nenhum:
>
>	Optimize-VHD -Path .\ext4.vhdx -Mode full

---
#### Redis
- **Redis**
>	docker run --name redis -p 6379:6379 -d redis:7-alpine

- **Redis CLI (rdcli)**
>	npm install redis-cli -g

- **Limpar Cache do Banco do Redis**>
>***Banco Local***
>qualquer terminal:
>
>	rdcli
>então:
> 
>	flushall
>---
>***Banco QA***
>qualquer terminal:
>
>	rdcli -h 64.227.104.246
> então:
> 
>	flushall

---
#### Others
- **Rider**
>	`Build` -> `Clean`
>	`Build` -> `Rebuild Solution`
>	`File` -> `Invalidate Caches / Restart`

- **RabbitMq**
>	docker run -d --name rabbitmq -p 5672:5672 -p 15672:15672 --hostname rabbitmq-master rabbitmq:3-management

- **Bluetooth**
>Reiniciar: 
>
>	sudo /etc/init.d/bluetooth restart

- **Git**
>Rebase: 
>
>	git pull origin master --rebase
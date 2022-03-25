## Tutorial Consul como servicy discovery

Entra no docker em modo interativo
```sudo docker exec -it consul01 sh```

Cria um cara tipo agent
```consul agent -dev```

Cria outro terminal e veja quais sao os server iniciados
```consul members```

Verficar na API do consul as informacoes
```curl localhost:8500/v1/catalog/nodes```


Consultas de DNS para ver os IP daqueles servicos
Instala o dig em um linux alphine
```apk -U add bind-tools```
Chama o dig no host e porta
```dig @localhost -p 8600 consul01.node.consul```
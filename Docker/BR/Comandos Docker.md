
# Guia de Comandos Docker

Este documento fornece uma visão geral dos comandos Docker mais comuns, incluindo descrições e parâmetros.

## 1. `docker --version`

Verifica a versão do Docker instalada.

### Parâmetros:
- **N/A**: Este comando não possui parâmetros.

### Exemplo:
```bash
docker --version
```

---

## 2. `docker pull <imagem>`

Baixa uma imagem do Docker Hub ou de um repositório específico.

### Parâmetros:
- `<imagem>`: O nome da imagem que você deseja baixar (ex: `ubuntu`, `nginx`).

### Exemplo:
```bash
docker pull ubuntu
```

---

## 3. `docker images`

Lista todas as imagens disponíveis localmente.

### Parâmetros:
- **N/A**: Este comando não possui parâmetros.

### Exemplo:
```bash
docker images
```

---

## 4. `docker rmi <imagem>`

Remove uma imagem local.

### Parâmetros:
- `<imagem>`: O nome ou ID da imagem que você deseja remover.

### Exemplo:
```bash
docker rmi ubuntu
```

---

## 5. `docker run <opções> <imagem>`

Executa um contêiner a partir de uma imagem.

### Parâmetros:
- `<opções>`: Opções adicionais (veja a lista abaixo).
  - `-d`: Executa o contêiner em segundo plano (modo detach).
  - `--name <nome>`: Atribui um nome ao contêiner.
  - `-p <host_port>:<container_port>`: Mapeia a porta do host para a porta do contêiner.
  - `-v <host_dir>:<container_dir>`: Monta um diretório do host no contêiner.

- `<imagem>`: O nome da imagem que você deseja executar.

### Exemplo:
```bash
docker run -d --name meu_nginx -p 8080:80 nginx
```

---

## 6. `docker ps`

Lista os contêineres em execução.

### Parâmetros:
- **-a**: Lista todos os contêineres, incluindo os parados.

### Exemplo:
```bash
docker ps
```
```bash
docker ps -a
```

---

## 7. `docker stop <container_id>`

Para um contêiner em execução.

### Parâmetros:
- `<container_id>`: O ID ou nome do contêiner que você deseja parar.

### Exemplo:
```bash
docker stop meu_nginx
```

---

## 8. `docker start <container_id>`

Inicia um contêiner parado.

### Parâmetros:
- `<container_id>`: O ID ou nome do contêiner que você deseja iniciar.

### Exemplo:
```bash
docker start meu_nginx
```

---

## 9. `docker rm <container_id>`

Remove um contêiner.

### Parâmetros:
- `<container_id>`: O ID ou nome do contêiner que você deseja remover.

### Exemplo:
```bash
docker rm meu_nginx
```

---

## 10. `docker exec <opções> <container_id> <comando>`

Executa um comando em um contêiner em execução.

### Parâmetros:
- `<opções>`: Opções adicionais (veja a lista abaixo).
  - `-it`: Permite a interação com o terminal.
  
- `<container_id>`: O ID ou nome do contêiner em que você deseja executar o comando.
- `<comando>`: O comando que você deseja executar dentro do contêiner.

### Exemplo:
```bash
docker exec -it meu_nginx /bin/bash
```

---

## 11. `docker logs <container_id>`

Exibe os logs de um contêiner.

### Parâmetros:
- `<container_id>`: O ID ou nome do contêiner cujos logs você deseja visualizar.

### Exemplo:
```bash
docker logs meu_nginx
```

---

## 12. `docker-compose up`

Inicia os serviços definidos no arquivo `docker-compose.yml`.

### Parâmetros:
- `-d`: Executa os serviços em segundo plano.
  
### Exemplo:
```bash
docker-compose up -d
```

---

## 13. `docker-compose down`

Para e remove todos os contêineres, redes e volumes definidos no arquivo `docker-compose.yml`.

### Parâmetros:
- **N/A**: Este comando não possui parâmetros.

### Exemplo:
```bash
docker-compose down
```

---

## Conclusão

Este guia oferece uma visão geral básica dos comandos do Docker. Para mais informações, consulte a [documentação oficial do Docker](https://docs.docker.com/).

# 🧪 Desafio Apache com Docker - DIO

Este projeto é parte do **Desafio Docker** da Digital Innovation One (DIO), com foco na criação de um ambiente básico com o **Apache HTTP Server** usando **Docker Compose**.

---

## 📦 Tecnologias Utilizadas

- Docker
- Docker Compose
- Apache HTTP Server (`httpd`)

---

## ⚙️ Estrutura do Container

O serviço `web` é definido com as seguintes configurações:

| Configuração       | Valor                                               |
|--------------------|-----------------------------------------------------|
| Imagem             | `httpd:latest`                                      |
| Nome do Container  | `desafio-apache-dio`                                |
| Porta              | `80:80` (exposta localmente)                        |
| Volume Montado     | `/data/apache` → `/usr/local/apache2/htdocs/`       |
| Rede personalizada | `minha-rede` (driver: bridge)                       |

---

## 🚀 Como Executar o Projeto

1. Clone o repositório:

   ```bash
   git clone https://github.com/abrdevelopment/desafio-docker-dio.git
   cd desafio-docker-dio
   ```

2. Inicie o container Apache:

```bash
docker-compose up -d
```

3. Acesse a aplicação via navegador:
```bash
http://localhost
```
Certifique-se de que o diretório /data/apache contenha o conteúdo HTML da sua aplicação.

## 🛑 Como Parar e Remover

```bash
docker-compose down
```

## 📚 Conceitos Praticados
- Criação de ambientes com Apache via Docker
- Montagem de volumes locais para servir conteúdo estático
- Uso de redes personalizadas no Docker Compose
- Orquestração de serviços via YAML

## 👨‍💻 Autor
Feito com 💻 por abrdevelopment

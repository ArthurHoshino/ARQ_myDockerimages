# Imagens Docker para instância de ambientes (in progress)

### Imagens para instanciar ambientes de desenvolvimento sem precisar instalar linguagens e bibliotecas local e aprender a mexer com Docker
---
## 🧑‍💻 Como instanciar os ambientes

### Requisitos básicos
* Ter Docker instalado

### Criar a imagem
Clone o repositório ou pegue o arquivo Dockerfile do ambiente desejado e acesse a pasta onde o arquivo foi salvo. Em seguida, rode o comando para criar a imagem a partir do arquivo Dockerfile:

``` bash
docker build -t <nome-da-image> .
```

Se quiser ter certeza de que a imagem foi criada, rode o seguinte comando para listar todas as imagens. Procure pelo nome que você escolheu:

```bash
docker image ls -a
```

Para utilizar a imagem e instanciar o container do ambiente acesse a pasta do projeto ou a pasta com todos os projetos e rode o comando:
```bash
docker run --rm -it --name <nome-do-container> -v $(pwd):/app <nome-da-imagem>:latest
```

    OBJETIVO 

 

Desenvolvimento do meu portfólio pessoal. 

 

    FERRAMENTAS 

 

Angular, FastAPI, MySQL e Docker. 

 

    AMBIENTES DE DESENVOLVIMENTO 

 

    AMBIENTE DE DESENVOLVIMENTO BACKEND 

 

	O ambiente de desenvolvimento backend consiste em dois containers: um rodando o serviço UVICORN com FastAPI e outro com MySQL. O código-fonte do backend, localizado na pasta app, será executado no container do FastAPI, que por sua vez se conectará ao banco de dados MySQL, abaixo serão listados os elementos do ambiente de desenvolvimento do backend: 

    ~/backend -> Diretório raiz do backend, contendo os arquivos necessários para a execução do serviço FastAPI e sua configuração no Docker. 

    ~/backend/dependenciaspython.txr -> Arquivo que lista todas as dependências necessárias para a execução do container fastapiservice. 

    ~/backend/Dockerfile -> Arquivo que define as intruções para a contrução da imagem Docker do serviço fastapiservice, que executará o backend FastAPI. 

    Comandos do arquivo Dockerfile: 

    FROM python: 3 -> usa a imagem oficial na versão 3 como base do container. 

    WORKDIR /usr/src/app: Define o diretório de trabalho dentro do container. 

    COPY . /usr/src/app -> Copia todos os arquivos do diretório “backend” para o diretório “/usr/scr/app” que está dentro do container. 

    RUN pip install –no-cash-dir –r dependenciaspython.txt -> Instala todas as dependências necessárias para rodar o FastAPI. 

	 

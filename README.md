# stress-test

Esta aplicação permite realizar testes de carga em um serviço web através de comandos CLI.

#### Entrada de parâmetros via CLI:
* --url: URL do serviço a ser testado.
* --requests: Número total de requests.
* --concurrency: Número de chamadas simultâneas.

#### Dados do relatório final:
* Tempo total gasto na execução.
* Quantidade total de requests realizados.
* Quantidade de requests com status HTTP 200.
* Distribuição de outros códigos de status HTTP (como 404, 500, etc.).


## Executando o teste de stress em ambiente local
1. Certifique-se de ter o Docker instalado.
2. Executar o comando:
    ```bash
    docker-compose build
    ```
3. Inicie o teste de stress.
    ```bash
    docker run tester --url=http://google.com --requests=1000 --concurrency=10
    ```
4. Aguarde até que o relatório seja gerado.
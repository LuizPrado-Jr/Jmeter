# JMeter Performance Testing

Este projeto utiliza o [Apache JMeter](https://jmeter.apache.org/) para testes de performance e carga em aplicações web.

## Estrutura do Projeto

- `apache-jmeter-5.6.3/`: Ferramenta JMeter e seus arquivos.
- `jmeter-tests/`: Scripts de teste (`.jmx`) criados para execução.
- `jmeter-report/`: Relatórios gerados após execução dos testes.
- `html/`: Página web para visualização dos resultados.

- No 'Out Tests' consegue visualizar e alterar as threads properties, conforme desejar executar os testes.
- 'Http Request' estão as informações da api utilizada para teste e o request e abaixo dle estão os relatórios gerados.

## Linguagem Utilizada

- **Java**: O JMeter é uma aplicação Java.
- **XML**: Os scripts de teste (`.jmx`) são arquivos XML.
- **HTML**: Relatórios e visualizações.

## Como Executar os Testes

1. Certifique-se de ter o Java instalado (JDK 8+).
2. Navegue até a pasta `apache-jmeter-5.6.3/bin`.
3. Na pasta execute o arquivo 'jmeter.bat'.
4. Abra o script desejado em 'Jmeter_OutPerformance.jmx.'
5. Configure os parâmetros conforme necessário.
6. Execute o teste.

## Como Visualizar o Relatório

Após a execução, abra o arquivo index.html em seu navegador para visualizar os resultados detalhados do teste.

Mais Informações
Scripts de teste podem ser editados e versionados em jmeter-tests.
Backups automáticos são salvos em backups/.
Relatórios brutos em jmeter-report/Summary Report.jtl.

## Informações importantes

Dentro do projeto tem mais relatórios que foram configurados para gerar como: View Result Tree, Summary Report, Aggregate Report, Graph Results e Response Time Graph que auxiliam na visualização dos resultados.

Para esse teste em si: Jmeter_OutPerfrmance.jmx foi executado um teste em uma api publica: jsonplaceholder.typicode.com

um Get no path /posts com as seguintes configurações:
500 users com um ramp-up de 60 segundos por 5 minutos

Resultado pode ser verificado no html dentro da pasta jmeter-report

Nele, você encontrará gráficos e tabelas que mostram:

Quantidade de requisições realizadas: Total de GETs feitos para /posts.
Tempo de resposta: Média, mínimo e máximo do tempo que a API levou para responder.
Taxa de erros: Percentual de requisições que falharam.
Throughput: Número de requisições processadas por segundo.
Distribuição dos usuários: Como os 500 usuários virtuais se comportaram durante o ramp-up de 60 segundos e os 5 minutos de teste.
Essas informações ajudam a identificar gargalos, quedas de performance e a estabilidade da API sob carga. O relatório HTML facilita a análise dos resultados por meio de gráficos interativos e estatísticas detalhadas.
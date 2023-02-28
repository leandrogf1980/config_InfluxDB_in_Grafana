# Configuração do InfluxDB no Grafana

1- Abra o Grafana acessando a URL: http://localhost:3000.  
No primeiro acesso informe o usuário e senha padrão, ***admin/admin***.

2- Criando o Data Source.
2.1- Clique no menu ***Configuration*** e em ***Data source***.

![image](https://user-images.githubusercontent.com/126198206/221891456-7dad7569-76d8-4c24-99ee-d9076b7dc6b0.png)

2.2- Clique no botão ***Add data source***.

![image](https://user-images.githubusercontent.com/126198206/221891608-86a0bbe5-5a83-4417-9519-94b6d4c3b361.png)

2.3- Localize em ***Time series databases*** o ***InfluxDB***.

![image](https://user-images.githubusercontent.com/126198206/221891997-284635ad-4fb1-487c-b69b-66a8b034e5c7.png)

3- Configurando o ***Data Source***.  
3.1- Em ***Query Language***, selecione ***Flux***.  
3.2- Na ***URL***, precisará informar o ***IP do container do InfluxDB*** seguido da porta. Para capturar o IP, precisa acessar o terminal Linux e informar o seguinte comando:  
**`sudo docker inspect --format '{{ .NetworkSettings.IPAddress }}' influxdb`**

![image](https://user-images.githubusercontent.com/126198206/221892439-71cc51b1-fecd-4d7c-b85c-43b8dda0beb2.png)

3.2- Nos campos ***Organization*** e ***Default Bucket*** informe os mesmos cadastrados no primeiro acesso do InfluxDB, conforme publicado em: https://github.com/leandrogf1980/first_Access_to_InfluxDB.git.  
3.3- No campo ***Token***, informe o token gerado no InfluxDB.  
Ao clicar no botão ***Save & test***, você será informado se a conexão com o influxDB foi realizada com sucesso.

![image](https://user-images.githubusercontent.com/126198206/221893353-88816c08-5772-4f40-9cf4-4f9be4a3b06f.png)

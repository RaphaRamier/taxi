# Introdução

O projeto tem como finalidade encontrar padrões nas informações disponíveis sobre o aplicativo de carona. Entender as preferências dos passageiros e o impacto de fatores externos nas corridas.

Será analisado dados de concorrentes e será testado uma hipótese sobre o impacto do clima na frequência das viagens.


---


## Descrição dos dados

Um banco de dados com informações sobre corridas de táxi em Chicago:

Tabela `neighborhoods`: dados sobre os bairros da cidade:

- name: nome do bairro
- neighborhood_id: código do bairro

---

Tabela `cabs`: dados sobre os táxis:
- cab_id: código do veículo
- vehicle_id: a identificação técnica do veículo
- company_name: a empresa proprietária do veículo

---

Tabela `trips`: dados sobre corridas:
- trip_id: código da corrida
- cab_id: código do veículo que opera a corrida
- start_ts: data e hora do início da corrida (tempo arredondado para a hora)
- end_ts: data e hora do final da corrida (tempo arredondado para a hora)
- duration_seconds: duração da corrida em segundos
- distance_miles: distância percorrida em milhas
- pickup_location_id: código do bairro de retirada
- dropoff_location_id: código do bairro de entrega

---

Tabela ``weather_records``: dados sobre o clima:
- record_id: código de registro meteorológico
- ts: grava data e hora (tempo arredondado para a hora)
- temperature: temperatura quando o registro foi feito
- description: breve descrição das condições meteorológicas, ex. "chuva leve" ou "nuvens esparsas"


# Conclusão


Fica evidente a predileção dos clientes pela empresa Flash Cab, talvez pela quantidade ou área em que os seus serviços abrangem ela se destaque tanto, mas tal tópico não pode ser avaliado por falta de dados a respeito dessas questões. Mas em um período de 2 dias, ela apresentou quase 20000 corridas, o que é uma quantidade considerável.

Já a cidade de Loop parece ser destino de muitas pessoas em Chicago, sendo seguida logo por River North como visto graficamente acima, com números também consideráveis mais de 10000 corridas que a teve como destino. 

A respeito da Hipótese testada o alpha escolhido foi de .5 pois é o comum, até pelo tamanho da amostra que é pequena, acredito ser o mais indicado. Como visto gráficamente a distribuição das corridas elas diferem consideravelmente, enquanto a condição "good" é assimétrica a esquerda a "bad" é assimétrica a direita. 
O teste  estatistico as médias uma diferença estatistica significante. 
Ou seja, em sábados chuvosos a média de tempo das corridas são maiores que em sábados não chuvosos. 
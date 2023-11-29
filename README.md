# chatgpt-data-science-ml

Projeto e anotações do curso [ChatGPT](./chat-gpt.md) para Ciência de Dados e Machine Learning na IA Expert Academy

Usando o próprio ChatGPT perguntamos : 

```
Como o ChatGPT pode ser utilizado por Cientistas de Dados e Engenheiros de Machine Learning ? 
```
_*E a Resposta foi a seguinte :*_ 

```
O ChatGPT pode ser uma ferramenta valiosa para cientistas de dados e engenheiros de machine learning em várias capacidades. Aqui estão algumas maneiras de como o ChatGPT pode ser utilizado por profissionais dessas áreas:

1. Geração de Código e Texto Técnico:
   - Pode ser usado para gerar trechos de código em várias linguagens de programação com base em descrições ou pedidos específicos.
   - Auxilia na redação de documentação técnica, relatórios e resumos.

2. Suporte em Problemas Técnicos:
   - Oferece assistência na solução de problemas técnicos ao responder perguntas sobre algoritmos, frameworks e conceitos de machine learning.

3. Experimentação e Ideação:
   - Facilita a exploração e geração de ideias durante a fase de experimentação em projetos de machine learning.

4. Explicabilidade e Interpretação de Modelos:
   - Ajuda na interpretação e explicação de modelos de machine learning, fornecendo descrições em linguagem natural sobre como os modelos estão tomando decisões.

5. Geração de Dados Sintéticos:
   - Pode ser utilizado para gerar dados sintéticos para testar modelos ou preencher lacunas em conjuntos de dados.

6. Prototipagem Rápida:
   - Facilita a prototipagem rápida de soluções, gerando código inicial ou esboços para novos projetos.

7. Treinamento e Educação:
   - Serve como uma fonte interativa para aprendizado sobre conceitos de machine learning e práticas recomendadas.

Ao utilizar o ChatGPT, é importante ter em mente que ele não possui conhecimento específico sobre dados confidenciais ou informações proprietárias, então é necessário ter cautela ao compartilhar detalhes sensíveis. Além disso, embora seja uma ferramenta poderosa, não substitui completamente a experiência e o conhecimento humano.

A integração do ChatGPT no fluxo de trabalho pode ser feita por meio de APIs disponíveis, permitindo que cientistas de dados e engenheiros de machine learning incorporem a capacidade de geração de linguagem natural em suas aplicações e processos de desenvolvimento.
```

O mesmo pode ser feito utilizando a api da OpenAI : 

<img width="1377" alt="image" src="https://github.com/sayymon/chatgpt-data-science-ml/assets/6488266/f7fcede8-f819-40a6-af92-8733963d4fe1">

Ex : 
```
curl --location --request POST 'https://api.openai.com/v1/chat/completions' \
--header 'Authorization: Bearer TOKEN_OPEN_AI' \
--header 'Content-Type: application/json' \
--data-raw '{
    "model": "gpt-3.5-turbo",
    "messages": [
        {
            "role": "user",
            "content": "Como o ChatGPT pode ser utilizado por Cientistas de Dados e Engenheiros de Machine Learning ?"
        }
    ],
    "temperature": 0.7
}'
```
Onde o parâmetro `temperature` no corpo da solicitação POST para a API https://api.openai.com/v1/chat/completions controla a "temperatura" da geração de texto. A temperatura afeta a aleatoriedade das respostas geradas pelo modelo:

**Baixa Temperatura (próxima de 0)**: Torna a saída mais determinística e focada. O modelo tende a gerar respostas mais óbvias e prováveis.

**Alta Temperatura (próxima de 1):** Torna a saída mais diversificada e aleatória. O modelo é mais propenso a gerar respostas inesperadas e criativas.

Sendo possivel tambem integrar com alguma SDK nas linguagens de preferencia Exemplo em python:

https://platform.openai.com/docs/quickstart?context=python

```
from openai import OpenAI
client = OpenAI()

completion = client.chat.completions.create(
  model="gpt-3.5-turbo",
  messages=[
    {"role": "user", "content": "Como o ChatGPT pode ser utilizado por Cientistas de Dados e Engenheiros de Machine Learning ?"}
  ]
)

print(completion.choices[0].message)
```

No tópico de Análise e exploração de dados , foram tratados os seguintes assuntos : 

- Estatísticas básicas
- Valores faltantes
- Outliers
- Relação entre pares
- Gráficos – atributos categóricos
- Gráficos – atributos numéricos
- Gráficos dinâmicos

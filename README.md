# Dio-MS-ai900-DP01-ModeloPrevisao
Desafio de Projeto da DIO para bootcamp ai900 Azure AI Fundamentals


Para a entrega do desafio vamos utilizar a documentação => https://aka.ms/ai900-auto-ml

## Step 1
- Dentro do Portal Azure vamos criar um novo recurso de Azure Machine Learning
![Screenshot 2024-03-29 143350](https://github.com/c23b/Dio-MS-ai900-DP01-ModeloPrevisao/assets/12342627/6ba37491-5441-42b3-804d-e57203f27599)


## Step 2
- Clique em "Criar" para iniciar a criação de um novo workspace.
![Screenshot 2024-03-29 144742](https://github.com/c23b/Dio-MS-ai900-DP01-ModeloPrevisao/assets/12342627/08b96834-11d3-4241-99c2-1b3bed7029a4)


## Step 3
- Crie um novo "**Resource group**", defina um **Name**. (DICA: selecione a região EAST US para consumir menos créditos)

![Screenshot 2024-03-29 145017](https://github.com/c23b/Dio-MS-ai900-DP01-ModeloPrevisao/assets/12342627/a8abea00-ae46-485a-b957-ab2a2f2df63a)



- Cloque em "**Review + create**", aguarde a mensagem de conclusão de validações positiva e clique em "**Create**".

![Screenshot 2024-03-29 145222](https://github.com/c23b/Dio-MS-ai900-DP01-ModeloPrevisao/assets/12342627/baf7fa42-9f20-4fe1-9e79-c64e05ea5443)


## Step 4
- A implantação está em andamento.
![Screenshot 2024-03-29 150007](https://github.com/c23b/Dio-MS-ai900-DP01-ModeloPrevisao/assets/12342627/c5d8a3f4-7638-4db8-b03b-1f68f0c97773)

- Após a conclusão do deploy, clique em **Go to resource**.
![Screenshot 2024-03-29 153156](https://github.com/c23b/Dio-MS-ai900-DP01-ModeloPrevisao/assets/12342627/39c6e8fa-741a-4fdc-a09e-cae0d9c87614)

- Na tela do Resource, clique em "**Launch studio**".
![Screenshot 2024-03-29 153618](https://github.com/c23b/Dio-MS-ai900-DP01-ModeloPrevisao/assets/12342627/9f7c43f9-78b3-4427-b02b-e8c7a2568f4d)


## Step 5
- O diretório do workspace será aberto. 
![Screenshot 2024-03-29 154332](https://github.com/c23b/Dio-MS-ai900-DP01-ModeloPrevisao/assets/12342627/5305876a-45f8-411c-b393-1697ff736a7c)

**Você pode visualizar todos os workspaces existentes clicando em "All workspaces".**
**Caso não houver nenhum workspace será necessario criar**

## Step 6
- Abra o workspace escolhido. Em seguida, acesse o ambiente "**Automated ML**" e clique em "**New Automated ML job**".
![Screenshot 2024-03-29 154901](https://github.com/c23b/Dio-MS-ai900-DP01-ModeloPrevisao/assets/12342627/f6ddf6cd-c089-4b90-996e-a78132abf9b6)

- Siga os Steps e preenchendo os dados do job com as informações fornecidas pela documentação da Microsoft.
  - Preencha as "**Basic settings**".
  - Job name: mslearn-bike-automl
  - New experiment name: mslearn-bike-rental
  - Description: Automated machine learning for bike rental prediction
  - Tags: none
    
![Screenshot 2024-03-29 160106](https://github.com/c23b/Dio-MS-ai900-DP01-ModeloPrevisao/assets/12342627/5b530704-70dc-429b-8f74-6c8b8ba2238f)

- Escolha o tipo de tarefa "**Regression**" e crie o dataset.
![Screenshot 2024-03-29 160225](https://github.com/c23b/Dio-MS-ai900-DP01-ModeloPrevisao/assets/12342627/8fb67766-7783-4590-a008-77806da576ad)


- Preencha as informações do dataset.
  - Name: bike-rentals
  - Description: Historic bike rental data
  - Type: Tabular
    
![Screenshot 2024-03-29 160424](https://github.com/c23b/Dio-MS-ai900-DP01-ModeloPrevisao/assets/12342627/fb67a791-a1a5-44d5-8712-5e3bc5496787)


- Selecione a fonte dos dados como "**From web files**".
![Screenshot 2024-03-29 160551](https://github.com/c23b/Dio-MS-ai900-DP01-ModeloPrevisao/assets/12342627/8b22ffd3-1638-43f1-b246-d35e272fb788)


- Inclua a URL do Dataset. A URL será verificada e validada.
  - Web URL: https://aka.ms/bike-rentals
  - Skip data validation: do not select
    
![Screenshot 2024-03-29 160701](https://github.com/c23b/Dio-MS-ai900-DP01-ModeloPrevisao/assets/12342627/984a5e78-aac5-49d9-b703-f352452ec7ba)


- Os dados devem estar configurados conforme especificado.
  - File format: Delimited
  - Delimiter: Comma
  - Encoding: UTF-8
  - Column headers: Only first file has headers
  - Skip rows: None
  - Dataset contains multi-line data: do not select
    
![Screenshot 2024-03-29 160841](https://github.com/c23b/Dio-MS-ai900-DP01-ModeloPrevisao/assets/12342627/23abfb12-1a0d-46b1-82a4-0c859eac27ae)


- O schema será visualizado. Não é necessário alterar nenhuma informação.
![Screenshot 2024-03-29 161125](https://github.com/c23b/Dio-MS-ai900-DP01-ModeloPrevisao/assets/12342627/7745f7a3-d29b-47ec-a63b-4ffe0c355e92)


- Revise todas as informações e clique em "criar" para criar o dataset.
![Screenshot 2024-03-29 161217](https://github.com/c23b/Dio-MS-ai900-DP01-ModeloPrevisao/assets/12342627/00fe9391-6a91-4f20-8302-2e68cb6afb9f)

- Selecione o dataset e clique em "next" para avançar.
![Screenshot 2024-03-29 161321](https://github.com/c23b/Dio-MS-ai900-DP01-ModeloPrevisao/assets/12342627/75e9695d-cd74-4787-a5af-c3e3d628548c)

- Configure a "**Task type**".
  - Task type: Regression
  - Dataset: bike-rentals
  - Target column: Rentals (integer)
  - Additional configuration settings:
    - Primary metric: Normalized root mean squared error
    - Explain best model: Unselected
    - Use all supported models: Unselected. You’ll restrict the job to try only a few specific algorithms.
    - Allowed models: Select only RandomForest and LightGBM — normally you’d want to try as many as possible, but each model added increases the time it takes to run the job. 

![Screenshot 2024-03-29 161734](https://github.com/c23b/Dio-MS-ai900-DP01-ModeloPrevisao/assets/12342627/cc4046c1-4dbd-485d-adc5-7af80112ba1a)

- Limits: Expand this section
    - Max trials: 3
    - Max concurrent trials: 3
    - Max nodes: 3
    - Metric score threshold: 0.085 (so that if a model achieves a normalized root mean squared error metric score of 0.085 or less, the job ends.)
    - Timeout: 15
    - Iteration timeout: 15
    - Enable early termination: Selected
  - Validation and test:
    - Validation type: Train-validation split
    - Percentage of validation data: 10
    - Test dataset: None

![Screenshot 2024-03-29 162140](https://github.com/c23b/Dio-MS-ai900-DP01-ModeloPrevisao/assets/12342627/3cd57905-9d52-4b45-af1c-ea083305e6a0)

- Não é necessário definir informações na parte de Computação.
  - Select compute type: Serverless
  - Virtual machine type: CPU
  - Virtual machine tier: Dedicated
  - Virtual machine size: Standard_DS3_V2*
  - Number of instances: 1
  
![Screenshot 2024-03-29 162423](https://github.com/c23b/Dio-MS-ai900-DP01-ModeloPrevisao/assets/12342627/4ec01c68-96cb-4826-b097-11051061962f)

- No step de review clique em "**Submit training job**".
![Screenshot 2024-03-29 162545](https://github.com/c23b/Dio-MS-ai900-DP01-ModeloPrevisao/assets/12342627/3884a1c5-754c-4bfc-8f33-825e53694a68)


## Step 7
- Aguarde o modelo entraá em status "**Ruinning**".
![Screenshot 2024-03-29 162730](https://github.com/c23b/Dio-MS-ai900-DP01-ModeloPrevisao/assets/12342627/2f2f7fe3-1b61-422e-b019-0b5412ed4ff1)

- Aguarde alguns minutos até o Status mudar para "**Completed***"
![Screenshot 2024-03-29 170032](https://github.com/c23b/Dio-MS-ai900-DP01-ModeloPrevisao/assets/12342627/6f7b0c87-8f7b-4b26-aa81-12d7b063b8d4)


## Step 8
- Navegue, verifique as étricas e entre no modelo.
![Screenshot 2024-03-29 170357](https://github.com/c23b/Dio-MS-ai900-DP01-ModeloPrevisao/assets/12342627/c8aaedc5-98b0-443a-ab3a-dcb6eb9d6fb0)
![Screenshot 2024-03-29 170855](https://github.com/c23b/Dio-MS-ai900-DP01-ModeloPrevisao/assets/12342627/ea8b1700-ca28-4b14-a4e3-c52a96762f74)
![Screenshot 2024-03-29 170813](https://github.com/c23b/Dio-MS-ai900-DP01-ModeloPrevisao/assets/12342627/1f0f8a5f-0148-45d0-b2e5-be24d55b54f1)
![Screenshot 2024-03-29 171002](https://github.com/c23b/Dio-MS-ai900-DP01-ModeloPrevisao/assets/12342627/a76249c7-34a9-425f-90bd-7ff1aadfb9c8)
![Screenshot 2024-03-29 171056](https://github.com/c23b/Dio-MS-ai900-DP01-ModeloPrevisao/assets/12342627/59214915-4d70-4ace-8005-91e9d2af8551)

- As métricas incluem os gráficos predicted_true e residuals, onde estará as informações e valores previstos em comparação com os reais.
![Screenshot 2024-03-29 171156](https://github.com/c23b/Dio-MS-ai900-DP01-ModeloPrevisao/assets/12342627/b578f358-b544-4e57-aa76-930ea9f0d630)


## Step 9
- Volta ao overview para criar o Deploy e teste do modelo. Selecione "**Deploy Web Service**".
![Screenshot 2024-03-29 171316](https://github.com/c23b/Dio-MS-ai900-DP01-ModeloPrevisao/assets/12342627/91e621e7-3103-4954-95d4-dcd398b4afd1)

- Preencha as informações.
  - Name: predict-rentals
  - Description: Predict cycle rentals
  - Compute type: Azure Container Instance
  - Enable authentication: Selected
    
![Screenshot 2024-03-29 171538](https://github.com/c23b/Dio-MS-ai900-DP01-ModeloPrevisao/assets/12342627/3e1cae2d-4f3d-42fc-b5ef-6d91f2343349)


- Aguarde a conclusão do deploy, navegue até "**Endpoints**"
![Screenshot 2024-03-29 173255](https://github.com/c23b/Dio-MS-ai900-DP01-ModeloPrevisao/assets/12342627/00318fe0-d12d-4a7b-84bd-bfdbdb678626)

- Agora podemos vizuaisar o swagger e configurar "**Test**".
![Screenshot 2024-03-29 173407](https://github.com/c23b/Dio-MS-ai900-DP01-ModeloPrevisao/assets/12342627/dbf59708-5696-48c1-9356-ca15aaf24353)

- Clique "**Test**" em Substitua o JSON existente pelo código fornecido pela documentação e clique no botão "**Test**".
```
 {
   "Inputs": { 
     "data": [
      {
         "day": 1,
         "mnth": 1,   
         "year": 2022,
         "season": 2,
         "holiday": 0,
         "weekday": 1,
         "workingday": 1,
         "weathersit": 2, 
         "temp": 0.3, 
         "atemp": 0.3,
         "hum": 0.3,
         "windspeed": 0.3 
       }
     ]    
   },   
   "GlobalParameters": 1.0
 }
```

- Será gerado o resultado do teste.
![Screenshot 2024-03-29 173553](https://github.com/c23b/Dio-MS-ai900-DP01-ModeloPrevisao/assets/12342627/ea9b478c-64a8-492b-88b7-dbbaeafc00f6)

## Fim

- Não esqueça de deletar o deploy, job e resource. Para não continuar a cobrar seus créditos.

# Power Apps Flow for Exchange Value

I devoloper this flow in my intern program, his function is get a yesterday exchange value (USD and EUR) utilizing a [BACEN API](https://olinda.bcb.gov.br/olinda/servico/PTAX/versao/v1/aplicacao#!/recursos/CotacaoMoedaPeriodoFechamento#eyJmb3JtdWxhcmlvIjp7IiRmb3JtYXQiOiJqc29uIiwiY29kaWdvTW9lZGEiOiJVU0QiLCJkYXRhSW5pY2lhbENvdGFjYW8iOiIwMS0xNy0yMDI1IiwiZGF0YUZpbmFsQ290YWNhbyI6IjAxLTE3LTIwMjUifSwicGVzcXVpc2FkbyI6dHJ1ZSwiYWN0aXZlVGFiIjoidGFibGUiLCJncmlkU3RhdGUiOnsDMAM6W3sDQgMiBDAEIiwDQQN9LHsDQgMiBDEEIiwDQQN9LHsDQgMiBDIEIiwDQQN9LHsDQgMiBDMEIiwDQQN9XSwDMQM6e30sAzIDOltdLAMzAzp7fSwDNAM6e30sAzUDOnt9fSwicGl2b3RPcHRpb25zIjp7A2EDOnt9LANiAzpbXSwDYwM6NTAwLANkAzpbXSwDZQM6W10sA2YDOltdLANnAzoia2V5X2FfdG9feiIsA2gDOiJrZXlfYV90b196IiwDaQM6e30sA2oDOnt9LANrAzo4NSwDbAM6ZmFsc2UsA20DOnt9LANuAzp7fSwDbwM6IkNvbnRhZ2VtIiwDcAM6IlRhYmxlIn19), this datas supplies a SharePoint List wich connects a PowerBI Report. 

I utilize a alternative method for extract the data, why a Get API action is a Premium on Automate, the alternative utilize  a One Drive action when save a JSON and read after this file for create a SharePoint Item.

#### Steps: 
<ol>
  <li>Download a Microsoft.Flow</li>
  <li>Import Flow in PowerAutomate Web</li>
  <li>Connect a Flow in your DataBase</li>
</ol>

### Parameters:
<ol> 
<li>Recurrency: Change by necessity your data uptade</li>
<li>Data (Compose): The default is configurated for get a today currency value</li>
<li>Upload file for URL: Change a URL for you necessity: 
<ul>
  <li>@codigoMoeda: Add a currency you need </li>
  <li>@dataInicialCotacao & @dataFinalCotacao: get a data configured before on compose action; 
  <li> Destination File Path: Is where your file it will be saved. PS: Is necessary incluide a file name and .json, Example: Dolar.Json</li>
</ul> 
</li>
<li>Compose: Is configurated for read a Json file</li>
<li>Create a Item: Create a Item on SharePoint List with a json values, change as your necessity</li>
</ol>

**This Flow is a default configurated for a single currency value for day, Maybe you neeed a other parammeters change a Flow actions and triggers**


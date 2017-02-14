---
layout: page-classic-sidebar-left
title: Análise
featimg: MapAntifraud.png
previous: /docs/1.0/autenticacao
next: /docs/1.0/postnotification
---
---

Esta página descreve os campos do contrato do Antifraude Gateway, além de conter exemplos de requisições HTTP.  

  
<a name="contract"></a>
  
## Campos do Contrato
-----------------------------------

**MerchantOrderId**{:.custom-attrib}  `required`{:.custom-tag} `100`{:.custom-tag} `string`{:.custom-tag}  
Número do Pedido da Loja.  

**TotalOrderAmount**{:.custom-attrib} `required`{:.custom-tag} `long`{:.custom-tag}  
Valor total do pedido em centavos.  
Ex.: 150000 (Valor equivalente a R$1.500,00)

**TransactionAmount**{:.custom-attrib} `required`{:.custom-tag} `long`{:.custom-tag}  
Valor da transação financeira a ser analisada.  
Ex.: 123456 Valor equivalente a R$1.234,56)

**Currency**{:.custom-attrib} `required`{:.custom-tag} `3`{:.custom-tag} `string`{:.custom-tag}  
Moeda no formato ISSO 4217  
Ex.: BRL (Real Brasileiro)

**Provider**{:.custom-attrib} `required`{:.custom-tag} `15`{:.custom-tag} `string`{:.custom-tag}  
Nome do Provedor da Solução de Analise de Fraude.  
Ex.: ReDShield

**OrderDate**{:.custom-attrib} `required`{:.custom-tag} `datetime`{:.custom-tag}  
Data do pedido.  
Ex.: 2016-12-09T19:16:38.155Z

**BraspagTransactionId**{:.custom-attrib} `optional`{:.custom-tag} `Guid`{:.custom-tag}  
Id da transação no Pagador da Braspag.  
Ex.: ED3B6646-5B6E-451C-B3CF-4FF5E807CB69

**CardData.Number**{:.custom-attrib}  `required`{:.custom-tag} `19`{:.custom-tag} `string`{:.custom-tag}  
Número do cartão de crédito.

**CardData.Holder**{:.custom-attrib}  `required`{:.custom-tag} `50`{:.custom-tag} `string`{:.custom-tag}  
Nome do cartão de crédito.  

**CardData.ExpirationDate**{:.custom-attrib}  `required`{:.custom-tag} `7`{:.custom-tag} `string`{:.custom-tag}  
Data de expiração do cartão de crédito.  
Ex.: 01/2023

**CardData.CVV**{:.custom-attrib}  `required`{:.custom-tag} `4`{:.custom-tag} `string`{:.custom-tag}  
Código de segurança do cartão de crédito.  

**CardData.Brand**{:.custom-attrib}  `required`{:.custom-tag} `10`{:.custom-tag} `string`{:.custom-tag}  
Bandeira do cartão de crédito.  

**CardData.EciThreeDSecure**{:.custom-attrib}  `optional`{:.custom-tag} `10`{:.custom-tag} `string`{:.custom-tag}  
Código do ECI (Eletronic Commerce Indicator) de autenticação  

**BillingData.Street**{:.custom-attrib}  `optional`{:.custom-tag} `255`{:.custom-tag} `string`{:.custom-tag}  
Logradouro do endereço de cobrança.  

**BillingData.Number**{:.custom-attrib}  `optional`{:.custom-tag} `100`{:.custom-tag} `string`{:.custom-tag}  
Número do endereço de cobrança.

**BillingData.Complement**{:.custom-attrib}  `optional`{:.custom-tag} `50`{:.custom-tag} `string`{:.custom-tag}  
Complemento do endereço de cobrança.

**BillingData.Neighborhood**{:.custom-attrib}  `optional`{:.custom-tag} `50`{:.custom-tag} `string`{:.custom-tag}  
Bairro do endereço de cobrança.

**BillingData.City**{:.custom-attrib}  `optional`{:.custom-tag} `50`{:.custom-tag} `string`{:.custom-tag}  
Cidade do endereço de cobrança.

**BillingData.State**{:.custom-attrib}  `optional`{:.custom-tag} `2`{:.custom-tag} `string`{:.custom-tag}  
Estado do endereço de cobrança.

**BillingData.Country**{:.custom-attrib}  `optional`{:.custom-tag} `255`{:.custom-tag} `string`{:.custom-tag}  
País do endereço de cobrança.

**BillingData.ZipCode**{:.custom-attrib}  `optional`{:.custom-tag} `9`{:.custom-tag} `string`{:.custom-tag}  
Código postal do endereço de cobrança.

**ShippingData.Street**{:.custom-attrib}  `optional`{:.custom-tag} `255`{:.custom-tag} `string`{:.custom-tag}  
Logradouro do endereço de entrega.  

**ShippingData.Number**{:.custom-attrib}  `optional`{:.custom-tag} `100`{:.custom-tag} `string`{:.custom-tag}  
Número do endereço de entrega.

**ShippingData.Complement**{:.custom-attrib}  `optional`{:.custom-tag} `50`{:.custom-tag} `string`{:.custom-tag}  
Complemento do endereço de entrega.

**ShippingData.Neighborhood**{:.custom-attrib}  `optional`{:.custom-tag} `50`{:.custom-tag} `string`{:.custom-tag}  
Bairro do endereço de entrega.

**ShippingData.City**{:.custom-attrib}  `optional`{:.custom-tag} `50`{:.custom-tag} `string`{:.custom-tag}  
Cidade do endereço de entrega.

**ShippingData.State**{:.custom-attrib}  `optional`{:.custom-tag} `2`{:.custom-tag} `string`{:.custom-tag}  
Estado do endereço de entrega.

**ShippingData.Country**{:.custom-attrib}  `optional`{:.custom-tag} `255`{:.custom-tag} `string`{:.custom-tag}  
País do endereço de entrega.

**ShippingData.ZipCode**{:.custom-attrib}  `optional`{:.custom-tag} `9`{:.custom-tag} `string`{:.custom-tag}  
Código postal do endereço de entrega.

**ShippingData.Email**{:.custom-attrib}  `optional`{:.custom-tag} `100`{:.custom-tag} `string`{:.custom-tag}  
E-mail do responsável a receber o produto no endereço de entrega.

**ShippingData.FirstName**{:.custom-attrib}  `optional`{:.custom-tag} `100`{:.custom-tag} `string`{:.custom-tag}  
Primeiro nome do responsável a receber o produto no endereço de entrega.

**ShippingData.MiddleName**{:.custom-attrib}  `optional`{:.custom-tag} `100`{:.custom-tag} `string`{:.custom-tag}  
Nome do meio do responsável a receber o produto no endereço de entrega.

**ShippingData.LastName**{:.custom-attrib}  `optional`{:.custom-tag} `100`{:.custom-tag} `string`{:.custom-tag}  
Último nome do responsável a receber o produto no endereço de entrega.

**ShippingData.Phone**{:.custom-attrib}  `optional`{:.custom-tag} `100`{:.custom-tag} `string`{:.custom-tag}  
Número do telefone do responsável a receber o produto no endereço de entrega.

**ShippingData.WorkPhone**{:.custom-attrib}  `optional`{:.custom-tag} `100`{:.custom-tag} `string`{:.custom-tag}  
Número do telefone de trabalho do responsável a receber o produto no endereço de entrega.

**ShippingData.Mobile**{:.custom-attrib}  `optional`{:.custom-tag} `100`{:.custom-tag} `string`{:.custom-tag}  
Número do celular do responsável a receber o produto no endereço de entrega.

**ShippingData.ShippingMethod**{:.custom-attrib}  `optional`{:.custom-tag} `50`{:.custom-tag} `string`{:.custom-tag}  
Meio de entrega.  
Ex.: None | SameDay | NexDay | TwoDay | ThreeDay | LowCost | CarrierDesignatedByCustomer | Pickup | International | Military | Other

**ShippingData.Comment**{:.custom-attrib}  `optional`{:.custom-tag} `100`{:.custom-tag} `string`{:.custom-tag}  
Referências do endereço de entrega.

**CustomerData.MerchantCustomerId**{:.custom-attrib}  `required`{:.custom-tag} `255`{:.custom-tag} `string`{:.custom-tag}  
Número do documento de identificação do comprador.  
Ex.: CPF | CNPJ | Passaporte

**CustomerData.FirstName**{:.custom-attrib}  `required`{:.custom-tag} `255`{:.custom-tag} `string`{:.custom-tag}  
Primeiro nome do comprador.

**CustomerData.MiddleName**{:.custom-attrib}  `optional`{:.custom-tag} `255`{:.custom-tag} `string`{:.custom-tag}  
Nome do meio do comprador.

**CustomerData.LastName**{:.custom-attrib}  `required`{:.custom-tag} `255`{:.custom-tag} `string`{:.custom-tag}  
Último nome do comprador do comprador.

**CustomerData.BirthDate**{:.custom-attrib}  `required`{:.custom-tag} `datetime`{:.custom-tag}  
Data de nascimento do comprador.  
Ex.: 1983-10-01T00:00:00.000Z

**CustomerData.Gender**{:.custom-attrib}  `optional`{:.custom-tag} `35`{:.custom-tag} `string`{:.custom-tag}  
Sexo do comprador.  

**CustomerData.Identity**{:.custom-attrib}  `optional`{:.custom-tag} `100`{:.custom-tag} `string`{:.custom-tag}  
Identidade do comprador.

**CustomerData.IdentityType**{:.custom-attrib}  `optional`{:.custom-tag} `35`{:.custom-tag} `string`{:.custom-tag}  
Tipo de identidade do comprador.

**CustomerData.Email**{:.custom-attrib}  `optional`{:.custom-tag} `100`{:.custom-tag} `string`{:.custom-tag}  
E-mail do comprador.

**CustomerData.Phone**{:.custom-attrib}  `optional`{:.custom-tag} `35`{:.custom-tag} `string`{:.custom-tag}  
Telefone do comprador.

**CustomerData.Ip**{:.custom-attrib}  `optional`{:.custom-tag} `35`{:.custom-tag} `string`{:.custom-tag}  
Endereço de IP do comprador.

**CustomerData.Mobile**{:.custom-attrib}  `optional`{:.custom-tag} `35`{:.custom-tag} `string`{:.custom-tag}  
Celular do comprador.

**CustomerData.WorkPhone**{:.custom-attrib}  `optional`{:.custom-tag} `35`{:.custom-tag} `string`{:.custom-tag}  
Telefone de trabalho do comprador.

**CustomerData.BrowserFingerPrint**{:.custom-attrib}  `required`{:.custom-tag} `6010`{:.custom-tag} `string`{:.custom-tag}  
Impressão digital de dispositivos e geolocalização real do IP do comprador.  
[Configuração do Fingerprint]({{ site.baseurl }}{% link docs/1.0/fingerprint.md %})

**CustomerData.Status**{:.custom-attrib}  `optional`{:.custom-tag} `35`{:.custom-tag} `string`{:.custom-tag}  
Status do comprador na loja.  
Ex.: NEW | EXISTING

**CartItem[n].ProductName**{:.custom-attrib}  `optional`{:.custom-tag} `50`{:.custom-tag} `string`{:.custom-tag}  
Nome do produto.

**CartItem[n].UnitPrice**{:.custom-attrib}  `optional`{:.custom-tag} `long`{:.custom-tag}  
Preço unitário do produto.
Ex.: 10950 (Valor equivalente a R$109,50)

**CartItem[n].MerchantItemId**{:.custom-attrib}  `optional`{:.custom-tag} `36`{:.custom-tag} `string`{:.custom-tag}  
ID do produto na loja.

**CartItem[n].Sku**{:.custom-attrib}  `optional`{:.custom-tag} `50`{:.custom-tag} `string`{:.custom-tag}  
Sku do produto.

**CartItem[n].Quantity**{:.custom-attrib}  `optional`{:.custom-tag} `int`{:.custom-tag}  
Quantidade do produto.

**CartItem[n].OriginalPrice**{:.custom-attrib}  `optional`{:.custom-tag} `long`{:.custom-tag}  
Preço original do produto.
Ex.: 11490 (Valor equivalente a R$114,90)

**CartItem[n].GiftMessage**{:.custom-attrib}  `optional`{:.custom-tag} `50`{:.custom-tag} `string`{:.custom-tag}  
Mensagem de presente.

**CartItem[n].ShippingInstructions**{:.custom-attrib}  `optional`{:.custom-tag} `255`{:.custom-tag} `string`{:.custom-tag}  
Instruções de entrega do produto.

**CartItem[n].ShippingMethod**{:.custom-attrib}  `optional`{:.custom-tag} `255`{:.custom-tag} `string`{:.custom-tag}  
Meio entrega do produto.  
Ex.: None | SameDay | NexDay | TwoDay | ThreeDay | LowCost | CarrierDesignatedByCustomer | Pickup | International | Military | Other

**CartItem[n].ShippingTranckingNumber**{:.custom-attrib}  `optional`{:.custom-tag} `50`{:.custom-tag} `string`{:.custom-tag}  
Número de ratreamento do produto.

**CustomerConfigurationData.ServiceId**{:.custom-attrib}  `optional`{:.custom-tag} `50`{:.custom-tag} `string`{:.custom-tag}  
Id do serviço no sistema de risco. Esse campo geralmente é definido por alguma configuração, mas em algumas situações, você pode querer usar a opção baseada em solicitação dinâmica.
Para o ReDShield isso define qual serviço de triagem de fraude deve ser usado.

**CustomerConfigurationData.RiskAmount**{:.custom-attrib}  `optional`{:.custom-tag} `long`{:.custom-tag}  
Valor de risco do pedido.  
Ex.: 1090 (Valor equivalente a R$10,90)

**CustomerConfigurationData.RiskBrand**{:.custom-attrib}  `optional`{:.custom-tag} `50`{:.custom-tag} `long`{:.custom-tag}  
Bandeira de risco do pedido.  

**CustomerConfigurationData.Website**{:.custom-attrib}  `optional`{:.custom-tag} `100`{:.custom-tag} `string`{:.custom-tag}  
Website da loja.

**CustomerConfigurationData.AccessTokenS**{:.custom-attrib}  `optional`{:.custom-tag} `255`{:.custom-tag} `string`{:.custom-tag}  

**MerchantDefinedData.Key**{:.custom-attrib}  `optional`{:.custom-tag} `255`{:.custom-tag} `string`{:.custom-tag}  
Campo definido junto ao provider.

**MerchantDefinedData.Value**{:.custom-attrib}  `optional`{:.custom-tag} `255`{:.custom-tag} `string`{:.custom-tag}  
Campo definido junto ao provider.

**TravelData.CompleteRoute**{:.custom-attrib}  `optional`{:.custom-tag} `100`{:.custom-tag} `string`{:.custom-tag}  
Rota completa da viagem. Concatenação das pernas (código do aeroporto) de origem e destino da viagem no formato, ORIG1-DEST1:ORIG2-DEST2.  
Ex.: SFO-JFK:JFK-LHR:LHR-CDG

**TravelData.DepartureTime**{:.custom-attrib}  `optional`{:.custom-tag} `datetime`{:.custom-tag}  
Data de partida do vôo.  
Ex.: 2017-03-01T15:10:00.000Z

**TravelData.JouneyType**{:.custom-attrib}  `optional`{:.custom-tag} `100`{:.custom-tag} `string`{:.custom-tag}  
Tipo de viagem.  
Ex.: Só ida | Ida e Volta.  

**TravelData.TravelLeg[n].Origin**{:.custom-attrib}  `optional`{:.custom-tag} `5`{:.custom-tag} `string`{:.custom-tag}  
Código do aeroporto de origem da viagem.  
Ex.: SFO

**TravelData.TravelLeg[n].Destination**{:.custom-attrib}  `optional`{:.custom-tag} `5`{:.custom-tag} `string`{:.custom-tag}  
Código do aeroporto de destino da viagem.  
Ex.: JFK

**PassengerData[n].FirstName**{:.custom-attrib} `optional`{:.custom-tag} `255`{:.custom-tag} `string`{:.custom-tag}  
Primeiro nome do passageiro.

**PassengerData[n].MiddleName**{:.custom-attrib} `optional`{:.custom-tag} `255`{:.custom-tag} `string`{:.custom-tag}  
Nome do meio do passageiro.

**PassengerData[n].LastName**{:.custom-attrib} `optional`{:.custom-tag} `255`{:.custom-tag} `string`{:.custom-tag}  
Último nome do comprador do passageiro.

**PassengerData[n].DateOfBirth**{:.custom-attrib} `optional`{:.custom-tag} `datetime`{:.custom-tag}  
Data de nascimento do passageiro.  
Ex.: 1985-07-22T00:00:00.000Z

**PassengerData[n].PassangerId**{:.custom-attrib} `optional`{:.custom-tag} `50`{:.custom-tag} `string`{:.custom-tag}  
ID do passageiro a quem o passageiro foi emitido.  

**PassengerData[n].Status**{:.custom-attrib} `optional`{:.custom-tag} `15`{:.custom-tag} `string`{:.custom-tag}  
Classificação da empresa aérea.
Ex.: Gold | Platinum

**PassengerData[n].PassengerType**{:.custom-attrib} `optional`{:.custom-tag} `35`{:.custom-tag} `string`{:.custom-tag}  
Tipo do passageiro.  
Ex.: Adult | Child | Infant | Youth | Student | SeniorCitizen | Military

**PassengerData[n].Email**{:.custom-attrib} `optional`{:.custom-tag} `100`{:.custom-tag} `string`{:.custom-tag}  
E-mail do passageiro.

**PassengerData[n].Phone**{:.custom-attrib} `optional`{:.custom-tag} `35`{:.custom-tag} `string`{:.custom-tag}  
Telefone do passageiro.

<a style="float: right;" href="#attributes"><i class="fa fa-angle-double-up fa-fw"></i></a>

<a name="http_operations"></a>

## Operações HTTP
-----------------------------------

`POST`{:.http-post} [https://riskhomolog.braspag.com.br/Analysis/](#post_analise){:.custom-attrib}  
Análise da transação  

`GET`{:.http-get} [https://riskhomolog.braspag.com.br/Analysis/{Id}](#get_analise){:.custom-attrib}  
Obter detalhes da Análise da transação  

<a style="float: right;" href="#http_operations"><i class="fa fa-angle-double-up fa-fw"></i></a>

<a name="post_analise"></a>

#### `POST`{:.http-post} Análise da Transação 
-------------------------------------------

**REQUEST:**  

``` http
POST https://riskhomolog.braspag.com.br/Analysis/ HTTP/1.1
Host: {antifraude endpoint}
Authorization: Bearer {access_token}
Content-Type: application/json
```

``` json
{
  "MerchantOrderId": "4493d42c-8732-4b13-aadc-b07e89732c26",
  "TotalOrderAmount": 1500,
  "TransactionAmount": 1000,
  "Currency": "BRL",
  "Provider": "RedShield",
  "OrderDate": "2016-12-09",
  "Card": {
  "Number" : "4000111231110112",
    "Holder": "Fernando Test",
    "ExpirationDate": "12/2023",
    "Cvv": "999",
    "Brand": "VISA",
    "EciThreeDSecure": "05"
  },
  "Billing": {
    "Street": "AV Marechal Camara",
    "Number": "160",
    "Complement": "Sala 934",
    "Neighborhood": "Castelo",
    "City": "Rio de janeiro",
    "State": "RJ",
    "Country": "BR",
    "ZipCode": "20020060"
  },
  "Shipping": {
        "Street": "Avenida Rio Branco",
        "Number": "30000",
        "Complement": "Complemento",
        "Neighborhood": "Centro",
        "City": "Rio de Janeiro",
        "State": "RJ",
        "Country": "BR",
        "ZipCode": "123456789",
        "Email": "ffigueiredo@braspag.com.br",
        "FirstName": "Fernando",
        "MiddleName": "Souza",
        "LastName": "Figueiredo",
        "ShippingMethod": "SameDay",
        "Phone": "12315454-8787878",
        "WorkPhone": "123456789-78945612",
        "Mobile": "987456-123456",
        "Comment": "Em frente ao 322."
    },
  "Customer": {
        "MerchantCustomerId": "baa0e542-bf10-4e03-9cda-c660c3246650",
        "FirstName": "Fernando",
        "MiddleName": "Souza",
        "LastName": "Figueiredo",
        "BirthDate": "2016-12-09T19:16:38.155Z",
        "Gender": "M",
        "Identity": "38303106171",
        "IdentityType": "1",
        "Email": "ffigueiredo@braspag.com.br",
        "Phone": "12315454-8787878",
        "WorkPhone": "123456789-78945612",
        "Mobile": "987456-123456",
        "Ip": "127.0.0.1",
        "BrowserFingerprint": "04003hQUMXGB0poNf94lis1ztuLYRFk+zJ17aP79a9O8mWOBmEnKs6ziAo94ggAtBvKEN6/FI8Vv2QMAyHLnc295s0Nn8akZzRJtHwsEilYx1P+NzuNQnyK6+7x2OpjJZkl4NlfPt7h9d96X/miNlYT65UIY2PeH7sUAh9vKxMn1nlPu2MJCSi12NBBoiZbfxP1Whlz5wlRFwWJi0FRulruXQQGCQaJkXU7GWWZGI8Ypycnf7F299GIR12G/cdkIMFbm6Yf0/pTJUUz1vNp0X2Zw8QydKgnOIDKXq4HnEqNOos1c6njJgQh/4vXJiqy0MXMQOThNipDmXv9I185O+yC2f3lLEO0Tay66NZEyiLNePemJKSIdwO9O5ZtntuUkG6NTqARuHStXXfwp8cyGF4MPWLuvNvEfRkJupBy3Z8hSEMEK7ZWd2T2HOihQxRh4qp+NANqYKBTl3v6fQJAEKikeSQVeBN8sQqAL0BZFaIMzbrnMivi6m6JRQUIdvEt+MbJEPFc0LjRycC5ApUmJO+Aoo9VKL1B8ftMSQ1iq1uTKn16ZOmDpzZrZhMPbH83aV0rfB2GDXcjpghm9klVFOw7EoYzV7IDBIIRtgqG9KZ+8NH/z6D+YNUMLEUuK1N2ddqKbS5cKs2hplVRjwSv7x8lMXWE7VDaOZWB8+sD1cMLQtEUC0znzxZ4bpRaiSy4dJLxuJpQYAFUrDlfSKRv/eHV3QiboXLuw9Lm6xVBK8ZvpD5d5olGQdc+NgsqjFnAHZUE+OENgY4kVU9wB84+POrI4MkoD4iHJ5a1QF8AZkZDFo1m1h9Bl+J2Ohr6MkBZq8DG5iVaunHfxUdHou5GL7lS1H7r+8ctfDXi8AfOPjzqyODJQ74Aiel35TKTOWG8pq1WO6yzJ1GNmMuMWZBamlGXoG/imnjwHY9HQtQzpGfcm0cR8X2Fd1ngNFGLDGZlWOX0jWtOwU6XVGT37JFD9W/cx4kzI+mPNi65X5WFPYlDG9N0Lbh5nOj3u3DXqRCiKCUrsEkMt8z9fxO9pLLGVQUKIYR2wTw53CiWK96FOpPevDWtH2XR0QkfOd02D73n81x6hEMCy0s3hRLn08Th9FlNHDMJBqLj+Tz8rG2TtNki3mJC7Ass1MT2qnKBI77n6vsQkAp59TfbZm/tBXwAoYdLJXge8F/numhd5AvQ+6I8ZHGJfdN3qWndvJ2I7s5Aeuzb8t9//eNsm73fIa05XreFsNyfOq1vG2COftC6EEsoJWe5h5Nwu1x6PIKuCaWxLY+npfWgM0dwJPmSgPx7TNM31LyVNS65m83pQ+qMTRH6GRVfg7HAcS5fnS/cjdbgHxEkRmgkRq1Qs48sbX9QC8nOTD0ntb6FcJyEOEOVzmJtDqimkzDq+SXR1/63AYe4LEj+ogRgN+Z8HAFhGFzd/m6snVviELfRqJ4LLQIk9Y/fzqnsF6I5OGxfdT2sxxK2Vokpi3jWhCcEknw7dYlHYpOnCHZO7QVgjQTngF2mzKf4GeOF4ECFsWTgLy6HFEitfauYJt1Xh1NfZZerBMwXLFzdhzoTQxGlcXc8lZIoEG1BLYv/ScICf8Ft9PEtpEa+j0cDSlU99UoH2xknwR1W9MRGc5I/euE63/IMJTqguZ3YcnJpjSVnAGSpyz/0gKjypJ3L86rHFRGXt0QbmaXtSl2UmmjI0p0LCCdx7McatCFEVI6FwPpPV0ZSMv/jM75eBid1X/lTV4XNzjowzR/iFlKYMzHZtVO9hCBPKlTwblRXNn4MlvNm/XeSRQ+Mr0YV5w5CL5Z/tGyzqnaLPj/kOVdyfj8r2m5Bcrz4g/ieUIo8qRFv2T2mET46ydqaxi27G4ZYHj7hbiaIqTOxWaE07qMCkJw==",
        "Status": "NEW"
    },
  "CartItems": [
    {
      "ProductName": "Mouse",
      "UnitPrice": "12000",
      "MerchantItemId": "4",
      "Sku": "0",
      "Quantity": 1,
      "OriginalPrice": "12000",
      "GiftMessage": "Te amo!",
      "Description": "Uma description do Mouse",
      "ShippingInstructions": "Proximo ao 546",
      "ShippingMethod": "SameDay",
      "ShippingTrackingNumber": "123456"
    },
    {
      "ProductName": "Teclado",
      "UnitPrice": "96385",
      "MerchantItemId": "3",
      "Sku": "0",
      "Quantity": 1,
      "OriginalPrice": "96385",
      "GiftMessage": "Te odeio!",
      "Description": "Uma description do Teclado",
      "ShippingInstructions": "Proximo ao 123",
      "ShippingMethod": "SameDay",
      "ShippingTrackingNumber": "987654"
    }
  ],
  "CustomConfiguration": {
    "ServiceId": "0",
    "RiskAmount": 0,
    "RiskBrand": "0",
    "MerchantWebsite": "www.test.com",
    "AccountTokenS": "acc123"
  },
  "MerchantDefinedData": [
    {
      "Key": "Segment",
      "Value": "8999"
    }
  ],
  "Travel": {
    "CompleteRoute": "GIG-CGH-EZE",
    "DepartueTime": "2016-12-10",
    "JouneyType": "JT",
    "TravelLegs": [
      {
        "Origin": "GIG",
        "Destination": "CGH"
      },
      {
        "Origin": "CGH",
        "Destination": "EZE"
      }
    ]
  },
  "Passengers": [
    {
      "FirstName": "Fernando",
      "MiddleName": "Souza",
      "LastName": "Figueiredo",
      "PassengerId": "1",
      "Status": "NEW",
      "PassengerType": "Adult",
      "Email": "ffigueiredo@braspag.com.br",
    "Phone" : "984554545454545",
      "DateOfBirth": "1982-04-30 17:00:00"
    }
  ]
}
```

**RESPONSE:**  

``` http
HTTP/1.1 201 Created
Content-Type: application/json;charset=UTF-8
```
``` json
{
  "Id": "22b5e829-edf1-e611-9414-0050569318a7",
  "AnalysisResult": {
    "Status": "Review",
    "Message": "Payment void and transaction challenged by ReD Shield",
    "ProviderCode": "100.400.148",
    "ProviderTransactionId": "8a8394865a353cc4015a37947c5f7e35",
    "ProviderOrderId": "487931363026"
  },
  "MerchantOrderId": "4493d42c-8732-4b13-aadc-b07e89732c26",
  "TotalOrderAmount": 1500,
  "TransactionAmount": 1000,
  "Currency": "BRL",
  "Provider": "RedShield",
  "OrderDate": "2016-12-09",
  "Card": {
  "Number" : "4000111231110112",
    "Holder": "Fernando Test",
    "ExpirationDate": "12/2023",
    "Cvv": "999",
    "Brand": "VISA",
    "EciThreeDSecure": "05"
  },
  "Billing": {
    "Street": "AV Marechal Camara",
    "Number": "160",
    "Complement": "Sala 934",
    "Neighborhood": "Castelo",
    "City": "Rio de janeiro",
    "State": "RJ",
    "Country": "BR",
    "ZipCode": "20020060"
  },
  "Shipping": {
        "Street": "Avenida Rio Branco",
        "Number": "30000",
        "Complement": "Complemento",
        "Neighborhood": "Centro",
        "City": "Rio de Janeiro",
        "State": "RJ",
        "Country": "BR",
        "ZipCode": "123456789",
        "Email": "ffigueiredo@braspag.com.br",
        "FirstName": "Fernando",
        "MiddleName": "Souza",
        "LastName": "Figueiredo",
        "ShippingMethod": "SameDay",
        "Phone": "12315454-8787878",
        "WorkPhone": "123456789-78945612",
        "Mobile": "987456-123456",
        "Comment": "Em frente ao 322."
    },
  "Customer": {
        "MerchantCustomerId": "baa0e542-bf10-4e03-9cda-c660c3246650",
        "FirstName": "Fernando",
        "MiddleName": "Souza",
        "LastName": "Figueiredo",
        "BirthDate": "2016-12-09T19:16:38.155Z",
        "Gender": "M",
        "Identity": "38303106171",
        "IdentityType": "1",
        "Email": "ffigueiredo@braspag.com.br",
        "Phone": "12315454-8787878",
        "WorkPhone": "123456789-78945612",
        "Mobile": "987456-123456",
        "Ip": "127.0.0.1",
        "BrowserFingerprint": "04003hQUMXGB0poNf94lis1ztuLYRFk+zJ17aP79a9O8mWOBmEnKs6ziAo94ggAtBvKEN6/FI8Vv2QMAyHLnc295s0Nn8akZzRJtHwsEilYx1P+NzuNQnyK6+7x2OpjJZkl4NlfPt7h9d96X/miNlYT65UIY2PeH7sUAh9vKxMn1nlPu2MJCSi12NBBoiZbfxP1Whlz5wlRFwWJi0FRulruXQQGCQaJkXU7GWWZGI8Ypycnf7F299GIR12G/cdkIMFbm6Yf0/pTJUUz1vNp0X2Zw8QydKgnOIDKXq4HnEqNOos1c6njJgQh/4vXJiqy0MXMQOThNipDmXv9I185O+yC2f3lLEO0Tay66NZEyiLNePemJKSIdwO9O5ZtntuUkG6NTqARuHStXXfwp8cyGF4MPWLuvNvEfRkJupBy3Z8hSEMEK7ZWd2T2HOihQxRh4qp+NANqYKBTl3v6fQJAEKikeSQVeBN8sQqAL0BZFaIMzbrnMivi6m6JRQUIdvEt+MbJEPFc0LjRycC5ApUmJO+Aoo9VKL1B8ftMSQ1iq1uTKn16ZOmDpzZrZhMPbH83aV0rfB2GDXcjpghm9klVFOw7EoYzV7IDBIIRtgqG9KZ+8NH/z6D+YNUMLEUuK1N2ddqKbS5cKs2hplVRjwSv7x8lMXWE7VDaOZWB8+sD1cMLQtEUC0znzxZ4bpRaiSy4dJLxuJpQYAFUrDlfSKRv/eHV3QiboXLuw9Lm6xVBK8ZvpD5d5olGQdc+NgsqjFnAHZUE+OENgY4kVU9wB84+POrI4MkoD4iHJ5a1QF8AZkZDFo1m1h9Bl+J2Ohr6MkBZq8DG5iVaunHfxUdHou5GL7lS1H7r+8ctfDXi8AfOPjzqyODJQ74Aiel35TKTOWG8pq1WO6yzJ1GNmMuMWZBamlGXoG/imnjwHY9HQtQzpGfcm0cR8X2Fd1ngNFGLDGZlWOX0jWtOwU6XVGT37JFD9W/cx4kzI+mPNi65X5WFPYlDG9N0Lbh5nOj3u3DXqRCiKCUrsEkMt8z9fxO9pLLGVQUKIYR2wTw53CiWK96FOpPevDWtH2XR0QkfOd02D73n81x6hEMCy0s3hRLn08Th9FlNHDMJBqLj+Tz8rG2TtNki3mJC7Ass1MT2qnKBI77n6vsQkAp59TfbZm/tBXwAoYdLJXge8F/numhd5AvQ+6I8ZHGJfdN3qWndvJ2I7s5Aeuzb8t9//eNsm73fIa05XreFsNyfOq1vG2COftC6EEsoJWe5h5Nwu1x6PIKuCaWxLY+npfWgM0dwJPmSgPx7TNM31LyVNS65m83pQ+qMTRH6GRVfg7HAcS5fnS/cjdbgHxEkRmgkRq1Qs48sbX9QC8nOTD0ntb6FcJyEOEOVzmJtDqimkzDq+SXR1/63AYe4LEj+ogRgN+Z8HAFhGFzd/m6snVviELfRqJ4LLQIk9Y/fzqnsF6I5OGxfdT2sxxK2Vokpi3jWhCcEknw7dYlHYpOnCHZO7QVgjQTngF2mzKf4GeOF4ECFsWTgLy6HFEitfauYJt1Xh1NfZZerBMwXLFzdhzoTQxGlcXc8lZIoEG1BLYv/ScICf8Ft9PEtpEa+j0cDSlU99UoH2xknwR1W9MRGc5I/euE63/IMJTqguZ3YcnJpjSVnAGSpyz/0gKjypJ3L86rHFRGXt0QbmaXtSl2UmmjI0p0LCCdx7McatCFEVI6FwPpPV0ZSMv/jM75eBid1X/lTV4XNzjowzR/iFlKYMzHZtVO9hCBPKlTwblRXNn4MlvNm/XeSRQ+Mr0YV5w5CL5Z/tGyzqnaLPj/kOVdyfj8r2m5Bcrz4g/ieUIo8qRFv2T2mET46ydqaxi27G4ZYHj7hbiaIqTOxWaE07qMCkJw==",
        "Status": "NEW"
    },
  "CartItems": [
    {
      "ProductName": "Mouse",
      "UnitPrice": "12000",
      "MerchantItemId": "4",
      "Sku": "0",
      "Quantity": 1,
      "OriginalPrice": "12000",
      "GiftMessage": "Te amo!",
      "Description": "Uma description do Mouse",
      "ShippingInstructions": "Proximo ao 546",
      "ShippingMethod": "SameDay",
      "ShippingTrackingNumber": "123456"
    },
    {
      "ProductName": "Teclado",
      "UnitPrice": "96385",
      "MerchantItemId": "3",
      "Sku": "0",
      "Quantity": 1,
      "OriginalPrice": "96385",
      "GiftMessage": "Te odeio!",
      "Description": "Uma description do Teclado",
      "ShippingInstructions": "Proximo ao 123",
      "ShippingMethod": "SameDay",
      "ShippingTrackingNumber": "987654"
    }
  ],
  "CustomConfiguration": {
    "ServiceId": "0",
    "RiskAmount": 0,
    "RiskBrand": "0",
    "MerchantWebsite": "www.test.com",
    "AccountTokenS": "acc123"
  },
  "MerchantDefinedData": [
    {
      "Key": "Segment",
      "Value": "8999"
    }
  ],
  "Travel": {
    "CompleteRoute": "GIG-CGH-EZE",
    "DepartueTime": "2016-12-10",
    "JouneyType": "JT",
    "TravelLegs": [
      {
        "Origin": "GIG",
        "Destination": "CGH"
      },
      {
        "Origin": "CGH",
        "Destination": "EZE"
      }
    ]
  },
  "Passengers": [
    {
      "FirstName": "Fernando",
      "MiddleName": "Souza",
      "LastName": "Figueiredo",
      "PassengerId": "1",
      "Status": "NEW",
      "PassengerType": "Adult",
      "Email": "ffigueiredo@braspag.com.br",
    "Phone" : "984554545454545",
      "DateOfBirth": "1982-04-30 17:00:00"
    }
  ],
  "SplitingPaymentMethod": "Undefined",
  "IsRetryTransaction": false
}
```
  
<a style="float: right;" href="#http_operations"><i class="fa fa-angle-double-up fa-fw"></i></a>
  
<a name="get_analise"></a>

#### `GET`{:.http-get} Obtenção do Detalhe da Análise
-------------------------------------------------

**PARÂMETROS:**  

``` csharp
Id: Guid  // Id da Transação no Antifraude
```

**REQUEST:**  

``` http
GET https://riskhomolog.braspag.com.br/Analysis/{Id} HTTP/1.1
Host: riskhomolog.braspag.com.br
Authorization: Bearer {access_token}
Content-Type: application/json
```

**RESPONSE:**  

``` http
HTTP/1.1 200 OK
Content-Type: application/json;charset=UTF-8
```
``` json
{
  "AnalysisResult": {
    "Id": "2ab5e829-edf1-e611-9414-0050569318a7",
    "CreatedDate": "2017-02-13T11:06:04.98",
    "ProviderCode": "100.400.148",
    "Status": 3,
    "Message": "Payment void and transaction challenged by ReD Shield",
    "ProviderOrderId": "487931363026"
  },
  "Id": "22b5e829-edf1-e611-9414-0050569318a7",
  "CreatedDate": "2017-02-13T11:05:57.8876743",
  "OrderDate": "2016-12-09T00:00:00",
  "Status": 2,
  "Provider": 1,
  "MerchantId": "51dd5477-f8c1-428d-a9fd-5d2faf40c25c",
  "TotalOrderAmount": 1500,
  "TransactionAmount": 1000,
  "MerchantOrderId": "4493d42c-8732-4b13-aadc-b07e89732c26",
  "Currency": "BRL",
  "ProviderTransactionId": "8a8394865a353cc4015a37947c5f7e35",
  "SplitingPaymentMethod": 0,
  "IsRetryTransaction": false
}
```
  
<a style="float: right;" href="#http_operations"><i class="fa fa-angle-double-up fa-fw"></i></a>
  


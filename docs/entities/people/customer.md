---
id: customer_entity
title: Cliente
---

### Campos

- **id**: Identificador único do cliente (UUID).
- **name**: Nome completo do cliente (string).
- **cpfCnpj**: CPF ou CNPJ do cliente (string).
- **personType**: Tipo de pessoa (Física ou Jurídica) (string).
- **rgIe**: RG ou Inscrição Estadual do cliente (string).
- **birthdate**: Data de nascimento do cliente (Date).
- **email**: Endereço de email do cliente (string).
- **phone1**: Primeiro número de telefone do cliente (string).
- **phone2**: Segundo número de telefone do cliente (opcional) (string).
- **notes**: Notas adicionais sobre o cliente (opcional) (string).
- **active**: Indica se o cliente está ativo ou não (boolean).
- **address**: Objeto contendo informações de endereço:
  - **zipCode**: CEP do cliente (string).
  - **address**: Endereço completo do cliente (string).
  - **addressNumber**: Número do endereço do cliente (string).
  - **complement**: Complemento do endereço (opcional) (string).
  - **district**: Bairro do cliente (string).
  - **city**: Objeto contendo informações da cidade:
    - **id**: Identificador único da cidade (string).
    - **name**: Nome da cidade (string).
  - **lat**: Latitude do endereço (opcional) (number).
  - **lng**: Longitude do endereço (opcional) (number).

### Métodos

- **validate()**: Valida os dados do cliente, garantindo que campos obrigatórios estejam preenchidos e que o formato do CPF/CNPJ esteja correto.
- **activate()**: Ativa o cliente, definindo o campo `active` como `true`.
- **deactivate()**: Desativa o cliente, definindo o campo `active` como `false`.
- **isValidCPF(cpf: string)**: Verifica se o CPF fornecido é válido.
- **isValidCNPJ(cnpj: string)**: Verifica se o CNPJ fornecido é válido.

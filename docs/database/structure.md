---
id: structure
title: Estrutura do Banco de Dados
---

## Tabelas e Campos

### Banks

- **id**: Identificador único do banco.
- **name**: Nome do banco.

### Cities

- **id**: Identificador único da cidade.
- **name**: Nome da cidade.
- **state**: Estado da cidade.
- **region**: Região da cidade.
- **lat**: Latitude.
- **lng**: Longitude.

### Companies

- **id**: Identificador único da empresa.
- **cnpj**: CNPJ da empresa.
- **name**: Nome da empresa.
- **city_id**: Identificador da cidade.
- **logo**: URL do logotipo da empresa.
- **sidebar_logo**: URL do logotipo para a barra lateral.
- **sidebar_logo_mini**: URL do logotipo mini para a barra lateral.
- **active**: Indica se a empresa está ativa.

### Contract Logs

- **id**: Identificador único do log de contrato.
- **contract_id**: Identificador do contrato.
- **contract_status_id**: Identificador do status do contrato.
- **comments**: Comentários.
- **created_by**: Usuário que criou o log.
- **created_at**: Data de criação.

### Contract Status

- **id**: Identificador único do status do contrato.
- **name**: Nome do status.
- **color**: Cor do status.

### Contracts

- **id**: Identificador único do contrato.
- **number**: Número do contrato.
- **person_id**: Identificador da pessoa.
- **plan_id**: Identificador do plano.
- **price**: Preço do contrato.
- **start_date**: Data de início.
- **end_date**: Data de término.
- **billing_day**: Dia de cobrança.
- **username**: Nome de usuário.
- **password**: Senha.
- **installation_address**: Endereço de instalação.
- **contract_status_id**: Identificador do status do contrato.
- **cancellation_date**: Data de cancelamento.
- **cancellation_reason**: Motivo do cancelamento.
- **created_by**: Usuário que criou o contrato.
- **created_at**: Data de criação.
- **updated_by**: Usuário que atualizou o contrato.
- **updated_at**: Data de atualização.
- **deleted_by**: Usuário que deletou o contrato.
- **deleted_at**: Data de deleção.

### Financial

- **id**: Identificador único.
- **type**: Tipo.
- **financial_account_id**: Identificador da conta financeira.
- **category_id**: Identificador da categoria.
- **schedule_id**: Identificador do agendamento.
- **number**: Número.
- **value**: Valor.
- **due_date**: Data de vencimento.
- **description**: Descrição.
- **person_id**: Identificador da pessoa.
- **notes**: Notas.
- **payment_method_id**: Identificador do método de pagamento.
- **payment_date**: Data de pagamento.
- **paid_value**: Valor pago.
- **seq**: Sequência.
- **created_at**: Data de criação.
- **created_by**: Usuário que criou.
- **updated_at**: Data de atualização.
- **updated_by**: Usuário que atualizou.
- **deleted_at**: Data de deleção.
- **deleted_by**: Usuário que deletou.

### Financial Accounts

- **id**: Identificador único da conta financeira.
- **name**: Nome da conta.
- **type**: Tipo da conta.
- **bank_id**: Identificador do banco.
- **agency**: Agência.
- **account**: Conta.
- **notes**: Notas.
- **active**: Indica se a conta está ativa.
- **created_by**: Usuário que criou.
- **created_at**: Data de criação.
- **updated_by**: Usuário que atualizou.
- **updated_at**: Data de atualização.
- **deleted_by**: Usuário que deletou.
- **deleted_at**: Data de deleção.

### Financial Categories

- **id**: Identificador único da categoria financeira.
- **parent_id**: Identificador da categoria pai.
- **type**: Tipo da categoria.
- **name**: Nome da categoria.
- **active**: Indica se a categoria está ativa.
- **created_at**: Data de criação.
- **created_by**: Usuário que criou.
- **updated_at**: Data de atualização.
- **updated_by**: Usuário que atualizou.
- **deleted_at**: Data de deleção.
- **deleted_by**: Usuário que deletou.

### Financial Schedule

- **id**: Identificador único do agendamento financeiro.
- **frequency**: Frequência.
- **interval**: Intervalo.
- **quantity**: Quantidade.
- **first_date**: Primeira data.
- **value**: Valor.
- **created_at**: Data de criação.
- **created_by**: Usuário que criou.
- **updated_at**: Data de atualização.
- **updated_by**: Usuário que atualizou.

### Menus

- **id**: Identificador único do menu.
- **parent_id**: Identificador do menu pai.
- **title**: Título do menu.
- **icon**: Ícone do menu.
- **route**: Rota do menu.
- **profiles**: Perfis associados ao menu.
- **order**: Ordem do menu.

### Payment Methods

- **id**: Identificador único do método de pagamento.
- **name**: Nome do método.
- **active**: Indica se o método está ativo.

### People Categories

- **id**: Identificador único da categoria de pessoas.
- **name**: Nome da categoria.
- **registration_type**: Tipo de registro.
- **created_by**: Usuário que criou.
- **created_at**: Data de criação.
- **updated_by**: Usuário que atualizou.
- **updated_at**: Data de atualização.
- **deleted_by**: Usuário que deletou.
- **deleted_at**: Data de deleção.

### Persons

- **id**: Identificador único da pessoa.
- **registration_type**: Tipo de registro.
- **name**: Nome da pessoa.
- **person_type**: Tipo de pessoa.
- **category_person_id**: Identificador da categoria da pessoa.
- **cpf_cnpj**: CPF ou CNPJ.
- **rg_ie**: RG ou Inscrição Estadual.
- **date_of_birth**: Data de nascimento.
- **email**: Endereço de email.
- **phone1**: Primeiro número de telefone.
- **phone2**: Segundo número de telefone.
- **zip_code**: CEP.
- **address**: Endereço.
- **number**: Número do endereço.
- **complement**: Complemento.
- **district**: Bairro.
- **city_id**: Identificador da cidade.
- **lat**: Latitude.
- **lng**: Longitude.
- **notes**: Notas.
- **active**: Indica se a pessoa está ativa.
- **created_by**: Usuário que criou.
- **created_at**: Data de criação.
- **updated_by**: Usuário que atualizou.
- **updated_at**: Data de atualização.
- **deleted_by**: Usuário que deletou.
- **deleted_at**: Data de deleção.

### Plans

- **id**: Identificador único do plano.
- **name**: Nome do plano.
- **description**: Descrição do plano.
- **price**: Preço do plano.
- **days_to_start_billing**: Dias para começar a cobrança.
- **radius_group**: Grupo de raio.
- **active**: Indica se o plano está ativo.
- **created_by**: Usuário que criou.
- **created_at**: Data de criação.
- **updated_by**: Usuário que atualizou.
- **updated_at**: Data de atualização.
- **deleted_by**: Usuário que deletou.
- **deleted_at**: Data de deleção.

### Profiles

- **id**: Identificador único do perfil.
- **name**: Nome do perfil.

### Users

- **id**: Identificador único do usuário.
- **name**: Nome do usuário.
- **email**: Email do usuário.
- **password**: Senha do usuário.
- **profile_id**: Identificador do perfil.
- **reset_password_fields**: Campos para redefinição de senha.
- **active**: Indica se o usuário está ativo.
- **created_by**: Usuário que criou.
- **created_at**: Data de criação.
- **updated_by**: Usuário que atualizou.
- **updated_at**: Data de atualização.

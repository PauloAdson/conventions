# Convenções de nomenclatura para banco de dados

## Geral

Os nomes das tabelas e colunas devem estar minúsculas e as palavras devem ser separadas por underscore, seguindo o padrão <ins>**snake case**</ins>. E todos os termos devem estar em <ins>**inglês**</ins>, exceto alguns termos que não há tradução apropriada para o inglês. Sempre prefira nomes descritivos, evitando ao máximo contrações.

## Tabelas

Os nomes das tabelas devem estar no plural.

**Exemplos:**

- **_Bom: `users`, `posts`, `roles`, `room_categories`._**
- **Ruim: ~~`user`~~, ~~`post`~~, ~~`grupos`~~, ~~`quarto_categoria`~~.**

## Colunas

Os nomes das colunas devem estar no singular.

**Exemplos:**

- **_Bom: `cpf`, `name`, `age`._**
- **Ruim: ~~`endereco`~~, ~~`posts`~~, ~~`idade`~~.**

## Foreign keys

Todas as **foreign keys** devem seguir o padrão **_`nome_da_tabela_no_singular_id`_**.

Por exemplo, caso a tabela **_`users`_** tenha um relacionameto com a tabela **_`roles`_**, o nome da coluna foreign key da tabela **_`users`_** deve ser **_`role_id`_**.

## Primary keys

A **primary key** de toda tabela deve ser uma <ins>coluna de inteiros com incremento automático</ins>, chamada **_`id`_**.

## DATETIME

- Toda tabela deve definir duas colunas para colocar os datetimes: **_`created_at`_** e **_`updated_at`_** do tipo **_`DATETIME(6)`_** "Tamanho 6". A coluna **_`created_at`_** recebe automaticamente o datetime do momento que o registro for criado. A coluna **_`updated_at`_** recebe automaticamente o datetime do momento que o registro for alterado.

- **_`created_at`_**: Armazena automaticamente o momento da criação do registro.

- **_`updated_at`_**: Armazena automaticamente o momento da última atualização do registro.

- Ao enviar, atualizar os registros do banco de dados, **_`created_at`_** e **_`updated_at`_** devem estar no **horário universal** **_`UTC +00:00`_**.

### Referência / Créditos

- https://gist.github.com/thiamsantos/654ec002f04c86d53611923a8b4c3a65#file-db-conventions-md

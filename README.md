# Time and Money

Uma API simples que processa vendas e cobra uma comissão pela operação financeira realizada. O objetivo é testar os problemas relacionados aos valores monetários e tipos de data e hora.

# Requisitos

Uma venda genérica é realizada. Essa venda contém os seguintes campos:
- Identificador do vendedor (UUID)
- Data e hora da venda no timezone do vendedor
- Valor da venda

Ao receber essa venda a API então aplica uma taxa de 5% no valor da venda e salva um registro informando o valor a ser retido e o valor a ser repassado para o vendedor (95%).
Inicialmente esse serviço vai ser oferecido apenas no Brasil, no estado de São Paulo.

A API faz sucesso e passa a ser vendida em todo o território nacional.

Com o sucesso, alguns requisitos novos passam a valer.
- A cobrança de 5% de comissão ocorre apenas até o dia 10, ao meio dia no timezone do vendedor.
- após o dia 10, até o dia 20, as comissões são de 4.5% nas vendas realizadas até às 18 horas e 4% nas vendas realizadas após às 18 horas.
- após o dia 20, as comissões são de 3% nas vendas realizadas até às 15 horas e 2,5% nas vendas realizadas após às 15 horas.

O site também passa a aceitar bitcoins como forma de pagamento.
Com isso um desconto de 10% na comissão deve ser dado a toda a venda recebida em bitcoin.


# Objetivo
O objetivo é conseguir descobrir problemas e propor soluções que envolvem data e hora, com timezone e uso de valores monetários e descobrir boas práticas para lidar com esses tipos de dados.

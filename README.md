# Bnaco-de-dados-II
Exercício prático

Uma empresa de vendas tem um banco de dados com informações sobre os seus produtos. Ela precisa criar um relatório que faça um levantamento diário da quantidade de produtos comprados por dia. Para ajudar a empresa, crie um procedure para agilizar esse processo.


DELIMITER //

CREATE PROCEDURE RelatorioProdutosComprados()
BEGIN
    SELECT DATE(data_compra) AS Data, COUNT(*) AS Quantidade
    FROM tabela_compras
    GROUP BY DATE(data_compra)
    ORDER BY DATE(data_compra) DESC;
END //

DELIMITER ;




Neste exemplo, supomos que a tabela de compras é chamada de "tabela_compras" e possui uma coluna "data_compra" que armazena a data da compra.

Ao chamar o procedure RelatorioProdutosComprados() , ele retornará um resultado que agrupa a quantidade de produtos comprados por cada dia, do mais recente ao mais antigo.

Você pode ajustar esse código de acordo com a estrutura real do seu banco de dados e a nomenclatura correta das tabelas e colunas.

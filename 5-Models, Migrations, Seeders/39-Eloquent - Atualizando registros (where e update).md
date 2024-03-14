Eloquent - Atualizando registros (where e update)

Como combinar o filtro de registro atraves da clausula update.


    Atraves do metodo update e um array associativo, o primeiro é a coluna e o segundo o valor a ser persistido no banco.

 Fornecedor::whereIn('id', [1,2])->update(['nome' => 'Fornecedor Teste']);
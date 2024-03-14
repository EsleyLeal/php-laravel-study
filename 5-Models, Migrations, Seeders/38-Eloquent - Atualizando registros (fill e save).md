Eloquent - Atualizando registros (fill e save)


fill - Preenchimento dos atributos para determinado objeto.

Forma mais pratica de atualizar os atributos do objeto, isso é atraves de um array associativo.


$fornecedores2->fill(['nome' => 'Fornecedor789', 'site' => 'fornecedor789.com.br', 'email' => 'contato789.com.br']);

= App\Models\Fornecedor {#5214

    id: 2,
    nome: "Fornecedor789",
    site: "fornecedor789.com.br",
    created_at: "2024-03-04 23:40:30",
    updated_at: "2024-03-04 23:40:30",
    uf: "SP",
    email: "contato789.com.br",
  }


  So consigo fazer essas alterações se a classe estiver configurada atraves do metodo fillabe 

  Ou seja , no meu arquivo Fornecedor.php 
            tenho isso aqui =>                  
                                            protected $fillable = ['nome', site', 'uf', 'email'];

                                    
Para persistir no banco de dados, chamamos a variavel e o metodo save();
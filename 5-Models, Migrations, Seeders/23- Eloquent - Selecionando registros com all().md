Como selecionar os registros no banco de dados -  Recuperar registro

Usamos o metodo estatico all que permite recuperar tudo em uma tabela.

exemplo

$fornecedores = \App\Models\Fornecedores::all();


ou assim

  use \App\Models\Fornecedor
> $for = Fornecedor::all();


O retorno de registro é dado atraves de um objeto chamado coleção que contem um array de objetos (Modelo)

Podemos tranforma o objeto em um array atraves do metodo

                    toArray();

print_r($for->toArray());


Podemos usar o 

    foreach($for as $f) {echo $f->nome; echo '-';}
teste1-Fornecedor ABC-⏎

pra visualizar melhor
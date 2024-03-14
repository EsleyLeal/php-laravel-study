Como remover registro - Remoção suave


Faz com que os registro nao sejam efetivamente excluidos da tabela.
Ele apenas adiciona uma nova coluna na tabela chamada delete_at
Excluir e ao mesmo tempo manter pra fins historicos
A tecnica de inclusao do softDelete dentro do nosso model é feito atraves do metodo chamado Trait
Basicamente Traits são pedaços de codigo que definem propriedades e metodos que podem ser utilizados dentro de uma classe como uma 
especie de include de CTRL + C E CTRL + V.


Primeiro para implementar o softDelete, precisamos passar ela no model

    use Illuminate\Database\Eloquent\SoftDeletes;

E dentro da class 

    use SoftDeletes;

Criar uma migration se torna interessante pra implementar essa nova coluna.

    Schema::table('fornecedores', function (Blueprint $table) {
            $table->softDeletes();
        });

         schema::table('fornecedores', function (Blueprint $table) {
            $table->dropSoftDeletes();
        });

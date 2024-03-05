                Estatico

Lembrando que metodo estatico ele nao depende da instancia do objeto e podemos apenas chamar os metodo passando 
apenas os parametros sem que haja uma instancia desse objeto antes.
    Usar metodo estatico dentro do framework laravel é bastante comum.

Na migrations por exemplos, usamos metodos estaticos. Quando utilizamos a classe schema ...


        protected $fillable = ['nome', 'site', 'uf', 'email'];

            php artisan tinker

\App\Models\Fornecedor::create(['nome'=>'Fornecedor ABC','site'=>'fornecedorabc.com.br','uf'=>'SP','email'=>'contato@fornecedorxyz.com.br']);



Principal diferença é que esse motodo nao vai precisar passar uma variavel(instancia)
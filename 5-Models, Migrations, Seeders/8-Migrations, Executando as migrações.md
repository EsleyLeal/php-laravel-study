Resolver erro 

Procedimento para correção:

    Editar o arquivo:- app\Providers\AppServiceProvider.php

Incluir a linha:

    use Illuminate\Support\Facades\Schema;

e dentro do

    public function boot(),
    
 adicionar o comando abaixo:

    public function boot()
    
    Schema::defaultStringLength(191);

Depois iniciar com 
    
        php artisan migrate


        Não precisa definir um tamanho para colunas do tipo integer e text !
php artisan migrate - Executa todos os metodos ups ( que nao foram executadas )

    Proposito do metodo Down 

Reverte tudo, desfaz tudo que o metodo up fez.

     public function down(): void
    {
        Schema::table('fornecedores', function (Blueprint $table) {
            //$table->dropColumn('uf');
            $table->dropColumn(['uf','email']);
        });
    }

Ou seja o metodo Schema se mantem junto com table, ou seja, passamos o metodo dropColumn com um array

    $table->dropColumn(['uf','email']);

Podemos ante disso verificar a existencia da tabela assim

    Schema::dropIfExists('fornecedores');
    
Ou a função drop que tenta remover sem fazer teste prévio

    $table->drop('fornecedores');






                                                Metodo de REVERSÃO

                                            php artisan migrate:rollback 

Para o metodo UP - É para a mais antiga para a mais atual

Para o metodo DOWN - É da mais atual para a mais antiga



                            Quantos passos quero retroceder nas migrations que foram executadas

php artisan migrate:rollback = Essa ele executa da ultima migration executada no banco
php artisan migrate:rollback --step=                                        








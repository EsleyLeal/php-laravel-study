            Status - Reset - Refresh - Fresh

Atalho de listagem das migrates que ja foi executada

    php artisan migrate:status

Reverter todas as migrações do banco - Atual para mais antiga ( metodo down )

    php artisan migrate:reset

Reverter todas as migrações executando metodo down, e depois executa o metodo migrate com o objetivo de recriar o banco de dados.

    php artisan migrate:refresh


Comando fresh é parecido com o refresh

Ao inves de exeuctar o metodo down de cada uma das migrates ele simplesmente dropa os objetos e depois executa o migrate.

    php artisan migrate:fresh
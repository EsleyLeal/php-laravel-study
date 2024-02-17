Configurar banco de dados local SQLite

---- Banco de dados SQL relacional imbutido e com  ele nao precisa realizar a instação de um SGBD, ou seja
de um Sistema Gerenciador de Banco de Dados.

Como por exemplo
        MYSQL, PostG ou SQLServer


SQLite é baseado em um arquivo de texto , cujo os dados são escritos dentro dele.
Pode ser usado em pequenos projetos, onde nao existe a necessidade de escalabilide ou segurança.

    Mas o ideal é usar apenas em desenvolvimento de testes



database.php ( Analisar esse arquivo ) = config raiz do projeto
    Guarda as conexões do banco de dados

    'sqlite' => [
            'driver' => 'sqlite',
            'url' => env('DATABASE_URL'),
            'database' => env('DB_DATABASE', database_path('database.sqlite')),
            'prefix' => '',
            'foreign_key_constraints' => env('DB_FOREIGN_KEYS', true),
        ],



        Metodo env 

        'database' => env('DB_DATABASE', database_path('database.sqlite')),

        Verifica a existencia das variaveis de ambiente e utiliza essas variaveis de ambiente na composição
        das string de conexão.
            E essas varivaies de ambiente são determinadas por suas vez dentro de 
                                                                                /.env ( environment )
                                                                                


database e .env tem que esta conectado ou seja , são interligados.

se apos a execução do 

    php artisan migrate
houver um erro..

no cmd digiteo comando php --ini , entre no caminho e procure por extension=pdo_sqlite
retire ";" da linha e execute novamente o comando 

    php artisan migrate

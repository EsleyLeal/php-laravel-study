1 Passo - Abrir arquivo de configurações de conexões. ( config / database.php )...

    criar tabela
create database sg

use sg


No arquivo .env temos isso 

    'options' => extension_loaded('pdo_mysql') ? array_filter([
                PDO::MYSQL_ATTR_SSL_CA => env('MYSQL_ATTR_SSL_CA'),
            ]) : [],

            Isso é um teste para ver se o pdo esta ou nao carregado, mas podemos fazer um teste na linha de comando.

    Verifica se a extensão em questao esta carregada e essa extensão é o pdo
php -r "var_dump(extension_loaded('pdo_mysql'));"

    Se for false , habilite no seu arquivo php.ini



CRIAR MODEL E MIGRATION  = 	php artisan make:model NomeProjeto -m     ( OBS; Nome sempre no singular )
FORMA ALTERNATIVA MODEL -	php artisan make:model NomeProjeto  ( Criou apenas o MODEL )
FORMA ALTERNATIVA MIGRATIONS - 	php artisan make:migrations create_nomedoprojeto_table

TESTE DE CONEXÃO = php -r "var_dump(extension_loaded('pdo_mysql'));"


RODAR MIGRATIONS = php artisan migrate ( Isso roda a migration adicionando as tabelas no nosso banco de dados )


COMO CRIAR NOVAS COLUNAS DENTRO DE TABELAS QUE JA FORAM CRIADAS NO BANCO DE DADOS 
A PARTIR DE UMA MIGRATION.

    CRIANDO MIGRATION 

php artisan make:migration alter_fornecedores_novas_colunas

    ADICIONAR NOVAS COLUNAS A UMA TABELA JA CRIADA

    Objeto que seleciona uma tabela ja no banco para a aplicação das instruções.
Schema::table('fornecedores', function (Blueprint $table) 
{
            $table->string('uf',2);
            $table->string('email', 150);   
});


CRIAR DATABASE
	create database

ENTRAR NA DATABASE 
	use ( nome do database )

LISTAR OS REGISTROS
	select * from migrations

MOSTRAR COLUNAS 
	describe fornecedores
Implementação da migration

Migration - Permite modelar o banco de dados da aplicação atraves do proprio PHP.
Não vamos precisar usar o SQL pra definição das tabelas das aplicações.

    Migrations fica dentro de database <<

                    Criado
2024_02_15_120405_create_site_contatos_table.php

    Na criação da migration temos isso

public function up(): void                                                      Metodo UP
    {
        Schema::create('site_contatos', function (Blueprint $table) {
            $table->id();
            $table->timestamps();
        });
    }


                            $table->timestamps();  Cria duas colunas, uma representa a data de criação do registro
                            a oura é uma instancia de atualização do registro.

1-Metodo UP
2-Remover tabela atraves do metodo down


    public function down(): void
    {
        Schema::dropIfExists('site_contatos');
    }

https://laravel.com/docs/10.x/migrations#creating-columns

Criação de colunas

    $table->string('nome', 50);
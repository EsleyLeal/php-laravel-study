    Relacionamento entre tabelas

Sem novidades, a ideia é que a chave primaria (id) da tabela viaje até a tabela que queremos guardar, ou seja, 
chave estrangeira.

por exemplo

                    produtos -->
                        id     -------------------------------------------
                                                    produtos_detalhes     |
                                                            id            |
                                                            produto_id    |     <--


Por convensao damos o nome da chave primaria no singular
                
                produto_id

Importante!!!

    A coluna da tabela que vai receber a chave estrangeira tenha o mesmo tipo da chave primaria.

    bigint unsigned
    $table->unsignedBigInteger('produto_id');



Constrant de integridade referencial indica que 
PRODUTO id da tabela produto_detalhes faz referencia para coluna id da tabela produtos.

        public function up(): void
    {
        Schema::create('produto_detalhes', function (Blueprint $table) {
            $table->id();
            $table->unsignedBigInteger('produto_id');
            $table->float('comprimento', 8,2);
            $table->float('largura', 8,2);
            $table->float('altura', 8,2);
            $table->timestamps();

            // constrant
            $table->foreign('produto_id')->references('id')->on('produtos');
            $table->unique('produto_id');  =================================== Garante que nao exista repetição
        });
    }

Foreign Keys -- Garante a interidade referencial !
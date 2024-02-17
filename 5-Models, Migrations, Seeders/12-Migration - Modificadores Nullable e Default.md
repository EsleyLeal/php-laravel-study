Como utilizar modificadores de coluna ? 

        Nullabe
Permite que colunas recebam valores vazios

        Default
Permite um valor padrão


                                                public function up(): void
    {
        Schema::create('produtos', function (Blueprint $table) {
            $table->id();
            $table->string('nome', 100);
            $table->text('descricao');
            $table->integer('peso');
            $table->float('preco_venda', 8, 2);
            $table->integer('estoque_minimo');
            $table->integer('estoque_maximo');
            $table->timestamps();
        });
    }

Supondo que na descrição eu nao queira passar nenhum valor, ou seja, vai ser nulo. 
Então preciso implementar isso, fica assim >>

        $table->text('descricao')->nullable();

No caso de um valor padrão, podemos usar assim >>

        $table->float('preco_venda', 8, 2)->default(0.01);
        $table->interger('estoque_minimo')->default(1);
        $table->interger('estoque_maximo')->default(1);
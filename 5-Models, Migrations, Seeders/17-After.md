After - Aprender a como usar o modificador de coluna.

Colocar as colunas em posição especifica da tabela..

Qual a posição que queremos incluir nossas colunas nas tabelas



          public function up(): void
    {
        Schema::table('fornecedores', function (Blueprint $table) {
            
            $table->string('site',150)->after('nome')->nullabe();
        });
    }
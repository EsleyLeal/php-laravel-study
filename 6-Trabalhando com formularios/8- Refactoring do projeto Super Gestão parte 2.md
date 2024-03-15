Relacionamento de tabelas

Refactoring do projeto Super Gestão parte 2


-- Criar a coluna motivo_contatos_id, migrar os dados de motivo_contato para motivo_contatos_id , aplicar a fk em motivo_contatos_id apontando para coluna id da tabela motivos_contatos e por fim remover a coluna motivo contato

    // Adicionando a coluna motivo_contatos_id
    
        Schema::table('site_contatos', function (Blueprint $table) {
            $table->unsignedBigInteger('motivo_contatos_id');
        });

  


    DB::statement('qualquer intrução sql') -> permite executar uma query no banco de dados


            Aqui pegamos os valores contidos em motivo_contato pra todos os registro contigo em site_contatos para motivo_contato_id

    DB::statement('update site_contatos set motivo_contato_id = motivo_contato');  
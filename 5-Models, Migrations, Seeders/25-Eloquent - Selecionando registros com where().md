Metodo Estatico

Um construtor que permite que diversos outros metrodos sejam utilizados em conjunto para construir a query adequada para seleção
de registros no banco.

A forma mais avançada... E vamos utilizar a forma mais simples utilizando operadores de comparação

Principais Operadores Logicos

            >
            >=
            <
            <=
            <>      -- Diferente
            like   - Com base em uma string , ele faz uma pesquisa em uma determinada coluna.


            > $contatos = SiteContato::where('nome_coluna','operador_comparacao','valor');
            > $contatos = SiteContato::where('id','>','1')->get();   --- Para retorno de uma collection acrescentamos o get

            $contatos = SiteContato::where('mensagem','like','%detalhes%')->get();

            usamos o operador % porcentagem atras da string , o operador curinga diz que podemos ter qualquer valor, que termine com a palavra detalhe
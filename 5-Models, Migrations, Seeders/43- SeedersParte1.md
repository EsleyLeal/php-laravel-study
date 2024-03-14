Responsavel por semear o banco de dados da aplicação, dados iniciais ou testes



php artisan make:seeder NomeSeeder

Temos que trazer o nosso model para o contexto da aplicação.

    use \App\Models\Fornecedor


            // instanciando o objeto
        $fornecedor = new Fornecedor();
        $fornecedor->nome = 'Fornecedor 100';
        $fornecedor->site = 'fornecedor100.com.br';
        $fornecedor->uf = 'CE';
        $fornecedor->email = 'contato@fornecedor100.com.br';
        $fornecedor->save();


        Temos o metodo create e para usar precisamos lembrar de passar no Models o protected fillable


            metodo create ( atenção para o atributo fillable da classe )
        Fornecedor::create([
            'nome' => 'Fornecedor 200',
            'site' => 'fornecedor200.com.br',
            'uf'   => 'RJ',
            'email'=>  'contato@fornecedor200.com.br'
        ]);


        // insert 


         DB::table('fornecedores')->insert([
            'nome' => 'Fornecedor 300',
            'site' => 'fornecedor300.com.br',
            'uf'   => 'PB',
            'email'=>  'contato@fornecedor300.com.br'
        ]);


Para processar seeders especificos


        php artisan db:seed --class=Fornecedor Seeder
Como trabalhar com uma factory.

1-Criar Facoty para alimentar tabela(Model) 

Factory permite , atraves de um seeder, semear em massa uma tabela no banco de dados

Utiliza uma biblioteca chamada Faker pra gerar os dados ficticios.

        php artisan make:factory SiteContatoFactory --model=SiteContato

Veja que passamos o nome da facoty que queremos popular e o modelo dela .


Eu havia criado o seed do SiteContato com esse comando

    php artisan db:seed --class=SiteContatoSeeder

Em seguida em dataBase seeder tenho isso 

        $this->call(SiteContatoSeeder::class);  É a chamada que permite executar

Em SiteContatoSeeder eu passo 

        \App\Models\SiteContato::factory()->count(100)->create();      Ele cria pra mim 100 registros


E isso so foi possivel devido a factory

        public function definition(): array
            {
                return [
                    

                    'nome' => fake()->name(),

                    'telefone' => fake()->cellphoneNumber(),

                    'email' => fake()->unique()->email(),

                    'motivo_contato' => fake()->numberBetween(1,3),

                    'mensagem' => fake()->sentence(4)
                ];
            }
        


        php artisan db:seed --class=SiteContatoSeeder   Comando de execução.




Exemplo Rapido - 

Factory - use \App\Models\SiteContato; E passamos no definition os nomes dos campos da tabela com a biblioteca faker.
Seeder - Chamo o comando de execução, chama o model e a factory junto  \App\Models\SiteContato::factory()->count(100)->create();
Em seguida no DatabaseSeeder.php e no metodo run , essa classe seeder precisa esta mapeada no metodo run. $this->call(SiteContatoSeeder::class);
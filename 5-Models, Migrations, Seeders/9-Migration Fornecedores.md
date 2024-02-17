Supondo que eu execute o comando 

    php artisan make:model Fornecedor

Sem o ( -m )

Nesse caso eu estou criando apenas o model sem a migration. Para criar a migration é preciso executar

    php artisan make:migration create_fornecedores_table



------

Detalhe = As migrations não serve apenas para criação de tabelas, toda ativida que faremos no banco de dados
serão feitas pela migration.

OBS:

TABELAS SÃO ESCRITAS NO PLURAL
MIGRATIONS SÃO ESCRITAS NO SINGULAR


                        
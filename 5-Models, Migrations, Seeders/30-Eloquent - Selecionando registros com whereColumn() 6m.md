Eloquent - Selecionando registros com whereColumn()

Quando passamos dois parametros no whereColumn ele entende que é por igualdade


    whereColumn('created_at', 'updated_at')


Suporta também 3 parametros . O segundo parametro é um operador


    whereColumn('created_at', '<>','updated_at')
Eloquent - Atualizando registros (save)

Como atualizar os registros que ja foram armazenados no banco de dados.


Primeiro - Recuperar esse registro

use App\Models\Fornecedor
> $fornecedor = Fornecedor::find(1);
= App\Models\Fornecedor {#5141
    id: 1,
    nome: "teste1",
    site: "teste1@gmail.com",
    created_at: "2024-03-04 23:24:43",
    updated_at: "2024-03-04 23:24:43",
    uf: "PB",
    email: "teste2@gmail.com",
  }

> $fornecedor->nome = 'Fornecedor123';
= "Fornecedor123"

> $fornecedor->site = 'Fornecedor123@gmail.com';
= "Fornecedor123@gmail.com"


        Atualizar

$fornecedor->save();
Unique - verifica Se ja existe uma informação em uma tabela no banco de dados.

                $request->validate([                AQUI
                'nome' => 'required|min:3|max:40|unique:site_contatos', 
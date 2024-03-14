 Eloquent - Selecionando e restaurando registros deletados com SoftDelete


 Metodo withTrashed()->get(); - Retorna um builder, registros e aqueles que foram removidos


 Fornecedores::withTrashed()->get(); - Retorna apenas o que foi removido


 $fornecedores[0]->restore();  Retira a informação delete_at e o registro passa a ser encontrado ( ativo )
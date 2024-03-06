Como utilizar os filtros =   

    whereBetween() e whereNotBetween()


Enquanto o whereIn() e o whereNotIn() realiza uma comparação de igualdade com array




whereBetween() e whereNotBetween() = A comparação é com base em intervalo.

$contato = SiteContato::whereBetween('id', [3,6])->get();  = Isso retorna 3,4,6

com o whereBetween() = É o inverso;
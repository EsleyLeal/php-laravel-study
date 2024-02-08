Array associativo

 Usando o Array associativo

         TesteController

class TesteController extends Controller
{
    public function teste(int $p1, int $p2) {
        return view('site.teste', ['p1' => $p1, 'p2' => $p2]);
    }
}


        Em teste.blade.php

P1 = {{ $p1 }}

<br>

P2 = {{ $p2 }}

<br>

A SOMA DE : P1 + P2 = {{ $p1 + $p2 }}
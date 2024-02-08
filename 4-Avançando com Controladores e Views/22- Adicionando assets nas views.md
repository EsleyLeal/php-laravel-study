Arquivos JavaScripts, CSS, imagens , videos, sons ... todos esses Assets, midias que acompanha o HTML
precisa esta publico, no diretorio Public.



utilizamos o help no blade ara conseguir visualizar o asset


exemplo de codigo

<div class="logo">
                <img src="img/logo.png">
</div>


Então utlizamos 


    <div class="logo">
                <img src="{{ asset('img/logo.png') }}"">
    </div>
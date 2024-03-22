    São recursos - Camadas de software implementadas entre aplicações destintas.

    Funciona como um intermediador de comunicação de entrada e saida entre aplicações destintas.

        Se popularizou nos anos 80 quando a necessidade de renovação de sistemas ligados se tornou um grande problema.
        Foram utilizados como uma forma de ligação entre os novos sistemas e sistemas legados.
        Isso permitia isolar bem as novas aplicações nos sistemas legados, permitia os programadores focar nas novas aplicações e não
        mais nos aspectos tecnicos dos sistemas legados.

        No contexto de aplicação web , os Middlewares atuam na interceptação de requisições http feitas pro browsers
        e  também na manipulação da resposta que é dada pela aplicação a esses mesmos browsers.


        A ideia é capturar as requisiçoes antes que ela chegue ao nucleo das aplicações.

        

        Geralmente manipulamos as response = resposta http para a padronização dos cabeçalhos quando estamos trabalhando com
        aplicações cors.


        CORS : Cross-origin Resource Sharing = Compartilhamento de recursos com origens diferentes

        CORS: APLICAÇÕES WEB QUE SE COMUNICAM COM DOMINIOS , PROTOCOLOS OU PORTAS DIFERENTES DA PROPRIA ORIGEM, ISSO É MUITO COMUM QUANDO
        NOSSA APLICAÇÃO EXPÕE APIS para aplicações externas, ou seja, quando a nossa aplicação fornece para outras aplicações
        acessos a determinadas rotas. Outras aplicações -> Outros dominios.
 

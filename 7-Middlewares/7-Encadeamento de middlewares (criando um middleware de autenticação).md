Encadeamento de middlewares (criando um middleware de autenticação)


Como as requisições formadas por clientes sao capturadas pelos middlewares de modo encadeados, sendo que essa requisição 
é transportadas de middlewares pra middlewares isso se houver o encadeamento, pra depois ser encaminhada para o nucleo da aplicação de modo que na sequencia a resposta dessa requisição faça o caminho inverso nesse encadeamento
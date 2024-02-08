Alternar entre versoes 

composer --version 
composer --help


pegar a versao e renomeiar o composer.phar
C:\ProgramData\ComposerSetup\bin\

curso 1.10.7  fazer o download da versao


Dica - Lidando com erros do Composer
Dicas importantes para a próxima aula enviadas por alunos do curso:



--

1) Dica do Bruno Martins: Ao iniciar novos projetos Laravel por meio do Composer, caso ocorra os erros:



Erro: Composer diagnose

Checking git settings: OK Checking http connectivity to packagist: WARNING [Composer\Downloader\TransportException] The "http://packagist.org/packages.json" file could not be downloaded: failed to open stream: No connection could be made because the target machine actively refused it.



ou



Erro: [Composer\Downloader\TransportException]                                                                                   

curl error 60 while downloading https://repo.packagist.org/packages.json: SSL certificate problem: self signed certificate



A dica para resolver é executar os comandos abaixo na linha de comandos do SO da seguinte forma:



1) Execute o comando: composer config -g repo.packagist composer https://repo.packagist.org

2) Execute o comando: composer self-update

3) Execute o comando: composer create-project --prefer-dist laravel/laravel projeto_lavavel_via_composer "7.0"



--

2) Dica do Pablo Batista: Ao iniciar novos projetos Laravel por meio do Composer, caso ocorra o erro:



Erro: [Composer\Exception\NoSslException]



A dica para resolver é acessar o arquivo php.ini e descomentar a linha com a instrução extension=openssl.
https://laravel.com/docs/10.x


C:\Users\esley.santana\Documents\Code



Configuração Global


composer config -g repo.packagist composer https://packagist.org
composer config -g github-protocols https ssh

Tive um erro na ciração do projeto, tive que entrar em C:\php-8.3.2\php.ini
e descomentar o extension=zip

e extension=fileinfo


composer create-project --prefer-dist laravel/laravel projeto_laravel_vi_composer "7.0"
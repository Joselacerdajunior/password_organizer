# Password Organizer

## 1. Requisitos
1. PHP-8.1.5
2. Composer-2.3.5
3. Laravel-9.X

## 2. Instalação (sequência)
### PHP
1. Baixe o PHP-8.1.5, [download link!](https://www.php.net/downloads)
2. Vá à raiz do sistema (C:) crie uma pasta com o nome "php-8.1.5" e extraia o arquivo ZIP baixado dentro dela.
3. Adicione o caminho "C:\php-8.1.5" às variáveis de ambiente do sistema.
4. Teste no console se o PHP foi instalado com sucesso.
    ``` 
    php --version
    ```

### COMPOSER
1. Baixe o Composer-2.3.5, [download link!](https://getcomposer.org/download)
2. Apenas avance durante a instalação. 
3. Configure o composer com os comandos:
    ```
    composer config -g repo.packagist composer https://packagist.org
    ```
    ```
    composer config -g github-protocols https ssh 
    ```

### LARAVEL
1. Crie o projeto com o comando:
    ```
    composer create-project --prefer-dist laravel/laravel password_organizer "9.x"
    ```
2. 
    Caso ocorra o erro:
    ```
    Updating dependencies
    Your requirements could not be resolved to an installable set of packages.

      Problem 1
        - laravel/framework[v8.40.0, ..., 8.x-dev] require league/flysystem ^1.1 -> satisfiable by league/flysystem[1.1.0, ..., 1.x-dev].
        - league/flysystem[1.1.0, ..., 1.x-dev] require ext-fileinfo * -> it is missing from your system. Install or enable PHP's fileinfo extension.
        - Root composer.json requires laravel/framework ^8.40 -> satisfiable by laravel/framework[v8.40.0, ..., 8.x-dev].

    To enable extensions, verify that they are enabled in your .ini files:
        - C:\php-8.0.8\php.ini
    You can also run `php --ini` inside terminal to see which files are used by PHP in CLI mode.
    ```
    Aplique a seguinte correção:
    ```
    No arquivo C:\php-8.1.5\php.ini procure pela extensão fileinfo (extension=fileinfo) sem parenteses e retire o ";" do início da instrução. Após fazer isso remova o projeto e tente criá-lo novamente.
    ```
3. Acesse a pasta do projeto pelo terminal do sistema e inicialize a aplicação com o comando:
 
    ```Observação: se você estiver clonando o projeto será necessário baixar as dependências, e para isso rxecute o comando "composer install"```

    ```
    php -S localhost:8000
    ```

## 3. Comandos
git init
git add .
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/Joselacerdajunior/password_organizer.git
git push -u origin main

…or push an existing repository from the command line
git remote add origin https://github.com/Joselacerdajunior/password_organizer.git
git branch -M main
git push -u origin main
# docker-laravel
Estructura base y configuraciones de docker para correr proyectos en Laravel

### En caso de presentar problemas con el instalador de Laravel en composer:
composer global config bin-dir ~/.composer/vendor/bin
composer global config bin-dir --absolute

touch ~/.bashrc
vi ~/.bashrc
export PATH=$PATH:/root/.composer/vendor/bin
source ~/.bashrc
composer global require laravel/installer
laravel --version


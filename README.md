# Website

## Setup
First you need to install [Composer](https://getcomposer.org/doc/00-intro.md) and [Node.JS and NPM](https://github.com/nvm-sh/nvm). Then install PHP mbstring and PHP xml (`sudo apt install php-mbstring php-xml`) and update the dependencies for both PHP and JS:
```shell
composer install
npm install
cp .env.example .env
php artisan key:generate
```

## Development
To start development, you need to run `php artisan serve`. It will output the link that leads to your website. You should also run `npm run watch` to dynamically rebuild changes you make to the Vue app. Both commands will attach to the shell you run them in. If you don't want to sustain multiple shells, use [nohup](https://linux.die.net/man/1/nohup) or a similar tool:
```shell
nohup npm run watch </dev/null &>/dev/null &
nohup php artisan serve &
```
This creates a `nohup.out` file. The output from `npm run watch` usually is not important and will be ommited, but you will find the IP and logs from `php artisan serve` in this file.
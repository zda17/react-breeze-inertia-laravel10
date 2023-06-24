(React + Tailwind) && (Inertia + Laravel) Starter Kit

## GETTING STARTED

Clone this repo and then:

```bash
touch .env
```

<br>

### Install Composer (if you've worked with Laravel before, skip this step)
Paste this in your terminal:
```bash
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');" <br>
php -r "if (hash_file('sha384', 'composer-setup.php') === '756890a4488ce9024fc62c56153228907f1545c228516cbf63f885e036d37e9a59d27d63f46af1d4d07ee0f76181c7d3') {     echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"
```
Run the following in your terminal to move composer into your $PATH
```bash
sudo mv composer.phar /usr/local/bin/composer
```
If you run into any trouble, you can go here and read more: https://getcomposer.org/download/

### Install NPM packages

```bash
npm install
```

### Install composer packages

```bash
composer install
```

### Install Sail (Laravel's built-in Docker config
```bash
php artisan sail:install
```
then type 0 for msyql, press enter <br>

then:
```bash
php artisan key:generate
```

then just to double check run:
```bash
composer update
```

Add sail to your $path (so you can just use 'sail' in future terminal commands):
```bash
alias sail='bash vendor/bin/sail'
```
If you get a "sail command not found" then just re-run this anytime.

## Open Docker Destkop

If you don't have Docker Desktop, you can download it here: https://www.docker.com/products/docker-desktop

Once it's open, run this in your terminal:
```bash
sail up
```
This will start the docker container(s)( If you get a "sail command not found" then you can run -- otherwise skip to the next step): 
```bash
./vendor/bin/sail up
``` 

If you run into any trouble, the Sail documentation is here: https://laravel.com/docs/8.x/sail#introduction

<br>

Open a new tab in the terminal and run:

```bash
sail artisan migrate
```

Or if you're still getting the "sail command not found", run this:

```bash
./vendor/bin/sail artisan migrate
```

For a list of commands you can run, run:
```bash
./vendor/bin/sail artisan
```

Migrations need to be run using 'sail' instead of 'php' so that they are run inside the docker container

Now run:

```bash
npm run dev
```
## Launch 🚀
Main page is here:
```bash
localhost
```

<br>
You'll need a DB client. I like to use TablePlus. <br>
You can download it here: https://tableplus.com/. <br>
<br>
Once you have that downloaded, open it up and click "create a new connection". <br>
Your info should look something like the image below (click "Test" for the boxes to turn green), and then click "Connect":

<img width="504" alt="Screen Shot 2021-05-19 at 10 04 43 PM" src="https://user-images.githubusercontent.com/52245667/118920263-b2bd8900-b8fb-11eb-9db1-8763a66f0d8f.png">

If you have trouble connecting to DB, see: https://laracasts.com/discuss/channels/servers/laravel-sail-no-dbdb-user-created

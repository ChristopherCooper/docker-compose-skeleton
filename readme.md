
1. Download Composer 
https://getcomposer.org/download/

php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('SHA384', 'composer-setup.php') === '544e09ee996cdf60ece3804abc52599c22b1f40f4323403c44d44fdfdd586475ca9813a858088ffbc1f233e9b180f061') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"

Check composer is installed, type composer in terminal.

2. Download Homebrew 
https://brew.sh/

/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

Wait for downloads to complete.

3. Install Docker CE
https://store.docker.com/editions/community/docker-ce-desktop-mac
Create a Docker CE account in order to download docker. Once your registered you should see the login to download docker change to download docker.
Wait for docker to download, go make a cup of tea it is 350+ MB.

Install and run docker, login using your username and password created above.

4. Intall Laravel.
https://laravel.com/docs/5.6
In terminal cd into the directory you want to install Larvel into.

cd PhpstormProjects/
composer create-project --prefer-dist laravel/laravel DevelopmentSite

4.1 Dockerise the Laravel installation.
Get local copy of Coopers skeleton builder.
Download zip to Documents - https://github.com/ChristopherCooper/docker-compose-skeleton.git
Copy the contents of the unzipped contents to your DevelopmentSite folder which should now be located at "/Users/nameofuser/PhpstormProjects/DevelopmentSite"
Close PHP storm open it again
Go to Preferences, Search for Docker, Click + symbol, Add Docker, Click Apply, Click Ok
Click Play on the Docker toolbar thats now appeared.
Right click on the docker-compose.yml shown under the project view and click run docker-compose.yml
You should now see output such as "c2f679898ade: Pulling fs layer" leave this to complete. You will see it starts to download loads of images

Open the .env file in your "DevelopmentSite" for laravel in the project folder.
Change the DB_HOST to the below.
DB_HOST=mysql

You are now done! go have a happy meal. http://localhost/





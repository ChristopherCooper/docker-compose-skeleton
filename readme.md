# Docker compose skeleton install

#### 1 Download Composer
  - Run the following in terminal
  
    ``` php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
    php -r "if (hash_file('SHA384', 'composer-setup.php') === '544e09ee996cdf60ece3804abc52599c22b1f40f4323403c44d44fdfdd586475ca9813a858088ffbc1f233e9b180f061') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
    php composer-setup.php
    php -r "unlink('composer-setup.php');"
 
Check Composer is installed by typing "composer" in terminal.

#### 2 Download Homebrew - https://brew.sh/
   - Type the following into terminal.
   ``` /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"```

Wait for the downloads to complete.

#### 3 Install Docker CE - https://store.docker.com/editions/community/docker-ce-desktop-mac

 - Create a Docker CE account in order to download docker. Once you have registered you should see the login to download docker change in order you to download it.
 - Wait for docker to download, go make a cuppa if your on the wifi.
 - Install and run docker, login using your username and password created above.

#### Install Laravel - https://laravel.com/docs/5.6

- In terminal cd into the directory you want to install laravel into. In my case this was the following.
 ``` cd PhpstormProjects/ ```
 ``` composer create-project --prefer-dist laravel/laravel DevelopmentSite ```

##### Dockerise the Laravel Installation
- Get local copy of Cooper skeleton builder - Download zip to Documents - https://github.com/ChristopherCooper/docker-compose-skeleton.git
- Copy the contents of unzipped contents to your DevelopmentSite folder. The folder should be located somewhere like. ```/Users/nameofuser/PhpstormProjects/DevelopmentSite```
- Close PHP storm completely.
- Open PHP Storm go to preferences, Search for Docker, Click (+) symbol, Add Docker, Click Apply, Click Ok.
- Click play on the Docker toolbar that has now appeared.
- Right click on the docker-compose.yml shown under the project view in PHP storm. Click run docker-compose-yml.
- You should now see output such as ```Pulling fs layer``` leave this to complete. You will see it starts to download lots of images.
- Once complete, open the .env file in your project window in the "DevelopmentSite" for Laravel in the project folder.
- Change the ```DB_HOST``` within the .env file ```to DB_HOST=mysql```

## Congratulations you are now done, head on over to localhost to see your new DevelopmentSite project.

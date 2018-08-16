# Hello and welcome!
## This project is an exploration of USER EXPERIENCE CENTERED web design. 
## The objective is to showcase the work of 'The New Dukes', a Sheffield (UK) based Sketch Comedy Troupe.

### The client has requested the following features for their web:

#### - A gallery for photos and videos
#### - Contact form so they can be booked for gigs
#### - Show their past shows
#### - Social media links

##### This project uses HTML/5 CSS/3 Bootstrap JavaScript jQuery and more!
### Thank you for your visit.

#### "Howdy weary traveller. Welcome to the home of The New Dukes, sketch trio extraordinaire! Here you can find info on shows to come, photos and clips of shows past, and anything that happens in between. So take a tour through our digital home and get to grips with the inner workings of Luke, Marcus and Damian's brains"


The space utils in this CSS section have been creaated from the information in https://getbootstrap.com/docs/4.1/utilities/spacing/

# Deployment of proyect
## This proyect was deployed through the following steps

- Creation of a server in Digital Ocean.
- Configured Nginx to serve static pages on the domain www.thenewdukes.com.
- Pulled the code down into the static serve folder from git repository https://github.com/Mgsignorelli/the-new-dukes.
- Restarted Nginx to pick up the configuration and codebase.
- The request from the booking form was set up to use a Php script to send an email to The New Dukes.
- The Nginx configuration used was the following:

server {
    listen 80 default_server;

    root /var/www/hosting/thenewdukes.com;

    index index.html index.htm;

    server_name thenewdukes.com www.thenewdukes.com;

    location / {
        try_files $uri $uri/;
    }
    location ~ \.php$ {
        include snippets/fastcgi-php.conf;
        fastcgi_pass unix:/var/run/php/php7.2-fpm.sock;
    }
}

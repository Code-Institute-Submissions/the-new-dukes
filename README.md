# USER EXPERIENCE CENTERED DESIGN

### This is the Milestone Project for the Experience Centered Design Unit of the Full Stack Web Developer Course of Code Institute, credit-rated by Edinburgh Napier University

### The objective of this project is to design and execute a Responsive, User Experience Centered, static page to showcase the work of 'The New Dukes', a Sheffield (UK) based Sketch Comedy Troupe.


### The client has requested the following features for their web:

#### - A gallery for photos and videos
#### - Contact form so they can be booked for gigs
#### - Showcase their work, their past performances and diffusion of upcoming shows.
#### - Include Social media links

This site is thought primarily for comedy fans and potential bookers and festival organisers. The client would like their users to be able to see their past work and future work, and be contacted for more performance oportunities. They also expressed they were interested in a colour palet resembling the red seats widely used in the clubs they have performed in. <p>With this in mind, a <a href='https://github.com/Mgsignorelli/the-new-dukes/blob/master/mockups.jpg'> Mockup </a> was sketched and approved by the client. </p>
<img src='https://i.pinimg.com/originals/37/55/ad/3755adc94c251f259a57aaac155fa64c.png' alt='Red Seats Leeds Show' class='img-responsive'></img> 

The website can be found in www.thenewdukes.com. 

                                                        
## Features

#### - Requested colour palet in the range of Dark Red to Salmon, for highlights and neutral grays for contrasting. 
#### - The website was optimized for accessibility and responsiveness for all different sizes of screens. 
#### - Navigation is aided by a Navigation Bar, with links to the Shows information, Contact Form, Gallery and Home page. In responsive mode, this Navbar is collapsed and a Dropdown Menu is used for comfort. 
#### - The Home page features an Image Header within a Jumbotron. This is designed to capture the attention of the web user and to give an immidiate visual example of the comedic value of the Trio via the chosen photograph and its edition. It features as well an introductory text that disappears in responsive mode for further comfort.
#### - The shows site has information of past shows with links to the events for further connection with, and within, the South Yorkshire Comedy Scene. 
#### - Contact form is fully functional and uses a Php script to send emails to The New Dukes.
#### - Gallery showcases media through the use of Modals. Available are both past shows registry and current photographs, as well as a Video made by The New Dukes exclusively for this website. 
#### - Social Media links are present at the footer of the webpage via clear and styled icons.

<img src='https://i.pinimg.com/originals/13/04/25/13042505d497e82b3d17da3541d38b99.png' alt='Red Seats Leeds Show' class='img-responsive'></img> 

## Technologies Used

#### - HMTL language for writting of the webpage layout
#### - CSS was used to customize the webpage design
#### - Bootstrap Framework was used to organize the webpage and uniform the layout throughout. Also, the spacing utils section has been creaated from the information in https://getbootstrap.com/docs/4.1/utilities/spacing/
#### - Media Queries were used to control the responsive adjustments for smallest screens of the Jumbotron, Navbar and Footer. 





## Testing
#### - This project was designed on a Mac laptop, therefore, it was actively tested in Windows platforms to avoid incompatibilities.
#### - Extensive testing in different browsers was performed in Mac and Windows machines.





## Deployment of proyect
### This proyect was deployed through the following steps

- Creation of a server in Digital Ocean.
- Configured Nginx to serve static pages on the domain www.thenewdukes.com.
- Pulled the code down into the static serve folder from git repository https://github.com/Mgsignorelli/the-new-dukes.
- Restarted Nginx to pick up the configuration and codebase.
- The request from the booking form was set up to use a Php script to send an email to The New Dukes.
- The Nginx configuration used was the following:

```
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
```




## Difficulties 
#### Especially at the beginning of the project, I had a problem using the fourth version of Bootstrap with instructions for the grid design of the course, meant for version 3.3.7. Eventually, following advice given by my first mentor, I decided to start over, using version 3.3.7. 
#### This proved difficult in the last stages of the project, when the Jumbotron Navbar and Footer were not responding as intended in smallest screens. This was eventually solved through the use of Media Queries, but I wish to keep working on this project and completely redo it with Bootstrap 4 and make sure the responsiveness does not get out of hand. 



## Content
 - All content was provided by Marcus Newman, member of The New Dukes.
 - The New Dukes is not a for profit organization. 

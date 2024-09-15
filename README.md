# GourmetPlace - Restaurant Website

Welcome to the GourmetPlace repository, a simple yet engaging restaurant website created with PHP, HTML, and CSS. The website offers an enhanced online dining experience with core features for easy navigation. As my first web development project, it focuses on essential functionalities and clean design.

![Restaurant Homepage](https://github.com/Chaimaa-zaghloul/GourmetPlace/blob/main/GourmetPlace/img/1.png)  
*Screenshot of the GourmetPlace homepage*

## Features

- **Home**: Welcomes visitors with a brief introduction to the restaurant.
- **Reservations**: Allows guests to reserve tables online with options for date, time, and special requests.
- **Menu**: Displays our dishes with descriptions and images.
- **Events**: Lists upcoming events and special occasions hosted at the restaurant.
- **About Us**: Tells the restaurant's story, mission, and introduces the team.
- **Config**: Backend page for managing site settings (restricted access).

## Getting Started

Follow these steps to run the project locally for development or testing purposes.

### Requirements

- PHP 7.4 or higher
- Apache or Nginx web server
- Optional: MySQL or another SQL database for storing reservations and menu items

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/GourmetPlace.git
   cd GourmetPlace

2. **Web Server Configuration**

   **For Apache Users:**
   Create a virtual host entry like below:
   ```apacheconf
   <VirtualHost *:80>
       ServerName gourmetplace.local
       DocumentRoot "/path/to/GourmetPlace"
       <Directory "/path/to/GourmetPlace">
           AllowOverride All
           Require all granted
       </Directory>
   </VirtualHost>
   ```

   **For Nginx Users:**
   Set up a server block:
   ```nginx
   server {
       listen 80;
       server_name gourmetplace.local;
       root /path/to/GourmetPlace;
       index index.php;
       location / {
           try_files $uri $uri/ =404;
       }
       location ~ \.php$ {
           include snippets/fastcgi-php.conf;
           fastcgi_pass unix:/var/run/php/php7.4-fpm.sock;
       }
   }
   ```

3. **Start your web server** and visit `http://gourmetplace.local` in your browser to view the site.

## Technologies Used

- **HTML**  for page structure
- **CSS** for styling
- **PHP** for server-side logic

## Authors

- **NOUIH Omar** - *Initial work* - [OmarNouih](https://github.com/OmarNouih)
- **ZAGHLOUL Chaimaa** - *Initial work* - [Chaimaa-zaghloul](https://github.com/Chaimaa-zaghloul)

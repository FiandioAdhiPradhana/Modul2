# MODUL 2 SAS
------
## Fiandio Adhi Pradhana (1202192034)/IT 02-01
## Reksa Aldian Rahmandy (1202192048)/IT 02-01
------
1. 

   * Cek lxc dengan menggunakan 

   ```markdown
    lxc-ls -f
   ```

   * Hapus ubuntu landing dengan menggunakan  command seperti dibawah ini, dan buat ubuntu focal baru dengan lxc-create

   ```markdown
    lxc-destroy ubuntu_landing
   ```

   <p align="center">
         		<img src= https://user-images.githubusercontent.com/93086665/144601260-54894407-7af5-400f-a023-2d72c51b6466.png>
   </p>
   
   <p align="center">
         	<img src= https://user-images.githubusercontent.com/93086665/144601656-6aa8d79d-f0ce-4759-a83d-c9ff11a84770.png>
   </p>
   
   

​		

- Setelah membuat baru, gunakan command lxc-start untuk memulai ubuntu_landing dan gunakan command lxc-attach untuk membuka ubuntu_landing. Lalu gunakan install nano untuk mengedit config.

  <p align="center">
        	<img src= https://user-images.githubusercontent.com/93086665/144602009-a33c3aa2-fcfd-4385-9d8e-328cb1a3366f.png>
   </p>
  </p>			

- Atur IP ubuntu_landing
          
  <p align="center">
        	<img src= https://user-images.githubusercontent.com/93086665/144602099-d4fd9a74-c21d-43c0-8ca9-e1b3949ddcd8.png>
  </p>			

  

  ```markdown
  sudo lxc-start -n ubuntu_landing
  sudo lxc-attach  -n ubuntu_landing
  nano /etc/netplan/10-lxc.yaml
  netplan apply
  
  ```

  <p align="center">
        	<img src= https://user-images.githubusercontent.com/93086665/144602555-dce4ed3e-15e3-4b79-97d9-843f4d842a3d.png>
  </p>			

  

  - atur autostart lxc, seperti dibawah ini :

    <p align="center">
          	<img src= https://user-images.githubusercontent.com/93086665/144602713-97e39a75-1197-4716-a42e-84d8e7cd6fbe.png>
    </p>			

  

  

  - install ssh 

    <p align="center">
          <img src=	https://user-images.githubusercontent.com/93086665/144602938-c530bdba-8d86-4bc4-bea9-c093253208c1.png>
    </p>			

    

    ```markdown
    PermitRootLogin yes
    RSAAuthentication yes
    service sshd restart
    
    ```

    <p align="center">
           <img src= https://user-images.githubusercontent.com/93086665/144603043-b65ae722-6cc2-4f49-948f-a2894b2b85f3.png>
    </p>			

    

  - cek ssh apakah sudah berjalan atau belum

    <p align="center">
          <img src=	https://user-images.githubusercontent.com/93086665/144603227-70556869-dd05-4d69-b3e0-40633122999e.png>
    </p>			





2. 

   - Cek lxc dengan menggunakan 

   ```markdown
    lxc-ls -f
   ```

   * Hapus ubuntu landing dengan menggunakan  command seperti dibawah ini, dan buat ubuntu_php7.4 baru dengan menggunakan command lxc-create

   ```markdown
    lxc-destroy ubuntu_php7.4
   ```

   <p align="center">
         <img src=	https://user-images.githubusercontent.com/93086665/144603396-0da56a75-0543-481c-884f-8c251ab4ce3a.png>
   </p>			

   <p align="center">
         	<img src= https://user-images.githubusercontent.com/93086665/144603558-ae49d84a-d900-4de8-8336-59cf9903f17f.png>
   </p>		

   

   - Setelah membuat baru, gunakan command lxc-start untuk memulai ubuntu_7.4 dan gunakan command lxc-attach untuk membuka ubuntu_7.4. Lalu gunakan install nano untuk mengedit config.

     <p align="center">
           	<img src= https://user-images.githubusercontent.com/93086665/144603708-e4dda3c4-c9bd-4463-af89-402d2dcd5721.png>
     </p>		

     
   
   - Atur IP ubuntu_php7.4
   
     <p align="center">
           	<img src= https://user-images.githubusercontent.com/93086665/144603814-bd8d9e8b-42a9-4389-8e7d-f58f293bf8b7.png>
     </p>		

     Dengan Menggunakan

     ```markdown
     sudo lxc-start -n ubuntu_php7.4
     sudo lxc-attach  -n ubuntu_php7.4
     nano /etc/netplan/10-lxc.yaml
     netplan apply
     
     ```

     <p align="center">
           	<img src= https://user-images.githubusercontent.com/93086665/144603962-78b6f1bb-a9af-4f82-8e3a-77f7ff48e012.png>
     </p>		

     
   
   - Hentikan ubuntu_php7.4 dengan menggunakan command

     ```markdown
     lxc-stop ubuntu_php7.4
     ```

     <p align="center">
           	<img src= https://user-images.githubusercontent.com/93086665/144604054-a5086697-0e9a-4702-8b1d-14faee3d6e0b.png>
     </p>		
     
     

   - Cek lxc dengan menggunakan 

   ```markdown
    lxc-ls -f
   ```
   
   <p align="center">
         	<img src= https://user-images.githubusercontent.com/93086665/144604139-31ff4a03-26eb-44bf-8d16-bee917c4b870.png>
   </p>		
   
   
   
   - install ssh
   
     <p align="center">
           	<img src= https://user-images.githubusercontent.com/93086665/144604184-59dbb3bf-498e-4912-8990-179632cc0375.png>
     </p>		
   
     
   
   - Atur password baru
   
     <p align="center">
          <img src= https://user-images.githubusercontent.com/93086665/144604300-c8b83a1e-3b25-41f9-8832-e7542cb454c4.png>
     </p>
     
   
   - cek ssh apakah sudah berjalan atau belum
   
     <p align="center">
           	<img src= https://user-images.githubusercontent.com/93086665/144604442-1889d49c-b08c-41d0-a4b6-6222f02d1687.png
     </p>		
     

3. vm.local/

- Langkah pertama yang harus dilakukan yakni menginstall laravel  menggunakan ansible. Setelah menginstall, masuk ke ansible tersebut dan buatlah folder laravel

  <p align="center">
        	<img src= https://user-images.githubusercontent.com/93086665/144604661-af031c49-b3fc-45d1-9bd8-37fe8235cd58.png>
  </p>		

  

- Selanjutnya, buat host untuk lxc yang nanti akan di otomasi

  <p align="center">       
    
    <img src= https://user-images.githubusercontent.com/93086665/144604720-6f9b6881-2d92-4960-8918-4e0d99a296a9.png>
                                 
    </p>   

   

  ```markdown
  [landing]
  ubuntu_landing ansible_host=lxc_landing.dev ansible_ssh_user=root ansible_become_pass=sepasi
  
  ```

  * Buatlah directory serta apapun yang akan digunakan untuk menjalankan folder php dan lakukan instalasi

    <p align="center">
          	<img src= https://user-images.githubusercontent.com/93086665/144604819-23d8fd50-58d1-4190-82dd-d010075730de.png>
    
  ```
  ---
  - hosts: all
    become : yes
    tasks:
      - name: install nginx nginx extras
        apt:
         pkg:
           - nginx
           - nginx-extras
         state: latest
      - name: start nginx
        service:
         name: nginx
         state: started
      - name: menginstall tools
        apt:
         pkg:
           - curl
           - software-properties-common
           - unzip
         state: latest
      - name: "Repo PHP 7.4"
        apt_repository:
          repo="ppa:ondrej/php"
      - name: "Updating the repo"
        apt: update_cache=yes
      - name: Installation PHP 7.4
        apt: name=php7.4 state=present
      - name: install php untuk laravel
        apt:
         pkg:
            - php7.4-fpm
            - php7.4-mysql
            - php7.4-mbstring
            - php7.4-xml
            - php7.4-bcmath
            - php7.4-json
            - php7.4-zip
            - php7.4-common
         state: present
  ```
  - Jika instalasi telah selesai dilakukan, buat folder installcomposer.yml

    <p align="center">
          	gambar belum
    </p>

  ```
  ---
   -hosts: all
    become : yes
    tasks:
     - name: Download and install Composer
       shell: curl -sS https://getcomposer.org/installer | php
       args:
        chdir: /usr/src/
        creates: /usr/local/bin/composer
        warn: false
     - name: Add Composer to global path
       copy:
        dest: /usr/local/bin/composer
        group: root
        mode: '0755'
        owner: root
        src: /usr/src/composer.phar
        remote_src: yes
     - name: Composer create project
       become_user: root
       composer:
        command: create-project
        arguments: laravel/laravel landing 
        working_dir: /var/www/html
        prefer_dist: yes
       environment:
          COMPOSER_NO_INTERACTION: "1"
     - name: mengkopi file .env.example jadi .env
       copy:
        dest: /var/www/html/landing/.env.example
        src: /var/www/html/landing/.env
        remote_src: yes
     - name: mengganti konfigurasi .env
       lineinfile:
        path: /var/www/html/landing/.env
        regexp: "{{ item.regexp }}"
        line: "{{ item.line }}"
        backrefs: yes
       loop:
        - { regexp: '^(.*)DB_HOST(.*)$', line: 'DB_HOST=10.0.3.200' }
        - { regexp: '^(.*)DB_DATABASE(.*)$', line: 'DB_DATABASE=landing' }
        - { regexp: '^(.*)DB_USERNAME(.*)$', line: 'DB_USERNAME=admin' }
        - { regexp: '^(.*)DB_PASSWORD(.*)$', line: 'DB_PASSWORD= ' }
        - { regexp: '^(.*)APP_URL(.*)$', line: 'APP_URL=http://vm.local' }
        - { regexp: '^(.*)APP_NAME=(.*)$', line: 'APP_NAME=landing' }
     - name: Composer install ke landing
       composer:
         command: install
         working_dir: /var/www/html/landing
       environment:
         COMPOSER_NO_INTERACTION: "1"
     - name: generate php artisan
       args:
        chdir: /var/www/html/landing
       shell: php artisan key:generate
     - name: mengganti permission storage
       file:
        path: /var/www/html/landing/storage
        mode: 0777
        recurse: yes
  
  ```

  - Lakukan instalasi kembali

    <p align="center">
          	gambar belum
    </p>

  - Buatlah file lxc_landing.dev

    <p align="center">
          	<img src= https://user-images.githubusercontent.com/93086665/144605170-69684284-0ba0-49e0-a50f-16f366c7f6cd.png>
    </p>

    ```
    
    server {
            listen 80;
    
            root /var/www/html/landing/public;
            index index.php index.html index.htm;
            server_name lxc_landing.dev;
    
            error_log /var/log/nginx/landing_error.log;
            access_log /var/log/nginx/landing_access.log;
    
            client_max_body_size 100M;
            location / {
                    try_files $uri $uri/ /index.php$args;
            }
            location ~\.php$ {
                    include snippets/fastcgi-php.conf;
                    fastcgi_pass unix:run/php/php7.4-fpm.sock;
                    fastcgi_param SCRIPTFILENAME $document_root$fastcgi_script_name;
            }
    }
    ```

    

  - Buatlah file config.yml

    <p align="center">       
          <img src= https://user-images.githubusercontent.com/93086665/144605309-85e62f58-c772-4441-a5fe-a30f927ac7d2.png>
    ```
    ---
    - hosts: all
      become : yes
      vars:
        domain: 'lxc_landing.dev'
      tasks:
       - name: stop apache2
         service:
          name: apache2
          state: stopped
          enabled: no
       - name: Write {{ domain }} to /etc/hosts
         lineinfile:
          dest: /etc/hosts
          regexp: '.*{{ domain }}$'
          line: "127.0.0.1 {{ domain }}"
          state: present
       - name: ensure nginx is at the latest version
         apt: name=nginx state=latest
       - name: start nginx
         service:
          name: nginx
          state: started
       - name: copy the nginx config file 
         copy:
          src: ~/ansible/laravel/lxc_landing.dev
          dest: /etc/nginx/sites-available/lxc_landing.dev
       - name: Symlink lxc_landing.dev
         command: ln -sfn /etc/nginx/sites-available/lxc_landing.dev /etc/nginx/sites-enabled/lxc_landing.dev
         args:
          warn: false
       - name: restart nginx
         service:
          name: nginx
          state: restarted
       - name: restart php7
         service:
          name: php7.4-fpm
          state: restarted
       - name: curl web
         command: curl -i http://lxc_landing.dev
         args:
          warn: false
    ```

    

  - Lakukan instalasi

    <p align="center">        gambar belum

    

    

  - Cek dengan cara membuka vm.local. Jika sukses, maka tampilannya akan seperti berikut ini :

    <p align="center">        
    	          <img src= https://user-images.githubusercontent.com/93086665/144605578-ed506a51-3c40-4d20-8f02-c1878f2928ae.png>
    



4. vm.local/blog

   - Seperti pada nomor sebelumnya, langkah pertama dimulai dengan masuk pada folder ansible

     <p align="center">
           	<img src= https://user-images.githubusercontent.com/93086665/144605665-e1dc89c8-399d-4d79-a659-7c55424082df.png>
     </p>

     

   - Buat host untuk lxc yang nanti akan di otomasi

     <p align="center">
           	<img src= https://user-images.githubusercontent.com/93086665/144605710-1a948dc2-62ac-4e11-8987-f16e6827ba19.png>
     </p>

   ```
   [blog]
   ubuntu_php7.4 ansible_host=lxc_php7.dev ansible_ssh_user=root ansible_become_pass=sepasi
   ```
   
   
   
   - Buat direktori untuk tasks,templates dan handlers di folder wordpress. Lalu, masuk ke dalam folder tasks untuk menginstall paket
   
     <p align="center">
           	<img src= https://user-images.githubusercontent.com/93086665/144605935-de4f54fa-f8e5-47ed-bed1-8c2ca2c13704.png>
     </p>
   
   ```
   ---
   - hosts: all
     vars:
       domain: 'lxc_php7.dev'
     tasks:
      - name: delete apt chache
        become: yes
        become_user: root
        become_method: su
        command: rm -vf /var/lib/apt/lists/*
   
      - name: install requirement
        become: yes
        become_user: root
        become_method: su
        apt: name={{ item }} state=latest update_cache=true
        with_items:
         - nginx
         - nginx-extras
         - curl
         - wget
         - php7.4
         - php7.4-fpm
         - php7.4-curl
         - php7.4-xml
         - php7.4-gd
         - php7.4-opcache
         - php7.4-mbstring
         - php7.4-zip
         - php7.4-json
         - php7.4-cli
         - php7.4-mysqlnd
         - php7.4-xmlrpc
         - php7.4-curl
   
      - name: wget wordpress
        shell: wget -c http://wordpress.org/latest.tar.gz
   
      - name: tar latest.tar.gz
        shell: tar -xvzf latest.tar.gz
   
      - name: copy folder wordpress
        shell: cp -R wordpress /var/www/html/blog
   
      - name: chmod
        become: yes
        become_user: root
        become_method: su
        command: chmod 775 -R /var/www/html/blog/
   
      - name: copy .wp-config.conf
        copy:
         src=~/ansible/wordpress/wp.conf
         dest=/var/www/html/blog/wp-config.php
   
      - name: copy wordpress.conf
        copy:
         src=~/ansible/wordpress/wordpress.conf
         dest=/etc/nginx/sites-available/{{ domain }}
        vars:
         servername: '{{ domain }}'
   
      - name: Symlink wordpress.conf
        command: ln -sfn /etc/nginx/sites-available/{{ domain }} /etc/nginx/sites-enabled/{{ domain }}
      
      - name: restart nginx
        become: yes
        become_user: root
        become_method: su
        action: service name=nginx state=restarted
   
      - name: Write {{ domain }} to /etc/hosts
        lineinfile:
         dest: /etc/hosts
         regexp: '.*{{ domain }}$'
         line: "127.0.0.1 {{ domain }}"
         state: present
   
      - name: enable module php mbstring
        command: phpenmod mbstring
   
      - name: restart php
        become: yes
        become_user: root
        become_method: su
        action: service name=php7.4-fpm state=restarted
   
      - name: restart nginx
        become: yes
        become_user: root
        become_method: su
        action: service name=nginx state=restarted
   ```
   
   
   
   - Kemudian, masuk ke dalam templates wp.conf yang merupakan tempat configuration pada wordpress
   
     <p align="center">
           	<img src= https://user-images.githubusercontent.com/93086665/144606086-325d0abb-ba20-43d5-82e3-63f71f2d9cf8.png>
     </p>
   
      
   
     ```
     <?php
     /**
      * The base configuration for WordPress
      *
      * The wp-config.php creation script uses this file during the installation.
      * You don't have to use the web site, you can copy this file to "wp-config.php"
      * and fill in the values.
      *
      * This file contains the following configurations:
      *
      * * MySQL settings
      * * Secret keys
      * * Database table prefix
      * * ABSPATH
      *
      * @link https://wordpress.org/support/article/editing-wp-config-php/
      *
      * @package WordPress
      */
     
     define( 'WP_HOME', 'http://vm.local/blog' );
     define( 'WP_SITEURL', 'http://vm.local/blog' );
     
     // ** MySQL settings - You can get this info from your web host ** //
     /** The name of the database for WordPress */
     define( 'DB_NAME', 'blog' );
     
     /** MySQL database username */
     define( 'DB_USER', 'admin' );
     
     /** MySQL database password */
     define( 'DB_PASSWORD', 'SysAdminSas0102' );
     
     /** MySQL hostname */
     define( 'DB_HOST', '10.0.3.200:3306' );
     
     /** Database charset to use in creating database tables. */
     define( 'DB_CHARSET', 'utf8' );
     
     /** The database collate type. Don't change this if in doubt. */
     define( 'DB_COLLATE', '' );
     
     /**#@+
      * Authentication unique keys and salts.
      *
      * Change these to different unique phrases! You can generate these using
      * the {@link https://api.wordpress.org/secret-key/1.1/salt/ WordPress.org secret-key service}.
      *
      * You can change these at any point in time to invalidate all existing cookies.
      * This will force all users to have to log in again.
      *
      * @since 2.6.0
      */
     define( 'AUTH_KEY',         'put your unique phrase here' );
     define( 'SECURE_AUTH_KEY',  'put your unique phrase here' );
     define( 'LOGGED_IN_KEY',    'put your unique phrase here' );
     define( 'NONCE_KEY',        'put your unique phrase here' );
     define( 'AUTH_SALT',        'put your unique phrase here' );
     define( 'SECURE_AUTH_SALT', 'put your unique phrase here' );
     define( 'LOGGED_IN_SALT',   'put your unique phrase here' );
     define( 'NONCE_SALT',       'put your unique phrase here' );
     
     /**#@-*/
     
     /**
      * WordPress database table prefix.
      *
      * You can have multiple installations in one database if you give each
      * a unique prefix. Only numbers, letters, and underscores please!
      */
     $table_prefix = 'wp_';
     
     /**
      * For developers: WordPress debugging mode.
      *
      * Change this to true to enable the display of notices during development.
      * It is strongly recommended that plugin and theme developers use WP_DEBUG
      * in their development environments.
      *
      * For information on other constants that can be used for debugging,
      * visit the documentation.
      *
      * @link https://wordpress.org/support/article/debugging-in-wordpress/
      */
     define( 'WP_DEBUG', false );
     
     /* Add any custom values between this line and the "stop editing" line. */
     
     
     
     /* That's all, stop editing! Happy publishing. */
     
     /** Absolute path to the WordPress directory. */
     if ( ! defined( 'ABSPATH' ) ) {
             define( 'ABSPATH', __DIR__ . '/' );
     }
     
     /** Sets up WordPress vars and included files. */
     require_once ABSPATH . 'wp-settings.php';
     
     ```
   
     
   
   - Masuk ke dalam templates wordpress.conf
   
     <p align="center">
           	<img src= https://user-images.githubusercontent.com/93086665/144606228-192b4362-1d54-4ba9-a461-c5819837bd00.png>
     </p>
   
     ```
     server {
          listen 80;
          listen [::]:80;
     
          # Log files for Debugging
          access_log /var/log/nginx/wordpress-access.log;
          error_log /var/log/nginx/wordpress-error.log;
     
          # Webroot Directory for Laravel project
          root /var/www/html/blog;
          index index.php index.html index.htm;
     
          # Your  Name
          server_name lxc_php7.dev;
     
          location / {
                  try_files $uri $uri/ /index.php?$query_string;
          }
     
          # PHP-FPM Configuration Nginx
          location ~ \.php$ {
                  try_files $uri =404;
                  fastcgi_split_path_info ^(.+\.php)(/.+)$;
                  fastcgi_pass unix:/run/php/php7.4-fpm.sock;
                  fastcgi_index index.php;
                  fastcgi_param SCRIPT_FILENAME $document_root$fastcgi_script_name;
                  include fastcgi_params;
          }
     }
     ```
   
     
   
     - Jalankan ansible kembali untuk menginstall
   
       <p align="center">
             	<img src= https://user-images.githubusercontent.com/93086665/144606363-5b8201dd-cb07-4985-8cc4-e407234f1ffb.png>
       </p>
   
     
   
   - Buka vm.local/blog/ untuk melakukan checking apakah wordpressnya sudah dapat dijalankan atau belum. Jika sudah dapat dijalankan, maka tampilannya akan berubah menjadi berikut :
   
     <p align="center">
           	<img src= https://user-images.githubusercontent.com/93086665/144606455-a41b4b89-1104-4a48-8ef8-2bda6972e7d8.jpeg>
     </p>
   
DONE :)

## Download RAILS
https://gorails.com/setup/windows/11
## RAILS
In WSL (Run as adminstater):
gem install rails -v 7.0.6
rails -v
for rails app creation;
rails new hello-rails -d postgresql OR rails new .
## POSTGRESQL
In WSL (Run as adminstater):
sudo apt install postgresql libpq-dev
=> set password: root
In VS Code Teminal (WSL-Ubuntu Shell):
1. Start Postgre Server:
sudo service postgresql start

 3. Connect to the PostgreSQL Server:
 sudo -u postgres psql

 5. Create User:
  CREATE ROLE masuma LOGIN PASSWORD 'your_password';

 4.Grant Necessary Privileges:
   ALTER USER masuma CREATEDB;
 
 5.Exit from terminal 
  \q

 6.Use createuser as the PostgreSQL Superuser:
  createuser -U postgres masuma

 7.Verify User Privileges:
  sudo -u postgres psql
 => within psql shell
    \du masuma
 
 8.If the "masuma" user doesn't have the CREATEDB privilege, you can grant it explicitly:
  ALTER USER masuma CREATEDB;
  
 9.Creating the Rails Database:
  rails db:create

 10. Start Server
  rails server (rails s)

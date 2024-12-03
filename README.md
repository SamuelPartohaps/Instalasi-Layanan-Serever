# Instalasi-Layanan-Serever
    Menggunakan UbuntuServer
# Updagrade System
    sudo apt upgrade

#  Install Nginx
    sudo apt update
    sudo apt install nginx -y
    sudo systemctl enable nginx
    sudo systemctl start nginx

#  Install MySQL
    sudo apt install mysql-server -y
    sudo systemctl enable mysql
    sudo systemctl start mysql

# Konfigurasi MySQL
    sudo mysql_secure_installation

# Install PHP
    sudo apt install php-fpm php-mysql -y
    sudo systemctl enable php7.4-fpm  # Ubah versi sesuai yang terinstal
    sudo systemctl start php7.4-fpm

#  Install Redis
    sudo apt install redis-server -y
    sudo systemctl enable redis
    sudo systemctl start redis

# Install FTP Server (vsftpd)
    sudo apt install vsftpd -y
    sudo systemctl enable vsftpd
    sudo systemctl start vsftpd

# Edit file konfigurasi
    sudo nano /etc/vsftpd.conf
    Tambahkan :
    local_enable=YES
    write_enable=YES
    (anonymous_enable=NO)

# Restart Layanan
    sudo systemctl restart vsftpd

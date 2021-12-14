<h3>Hướng dẫn sử dung laravel + docker = LARADOCK</h3>
<hr>
<p>Bài viết được tham khảo bởi <a href="https://kipalog.com/posts/Trien-khai-du-an-laravel-voi-laradock--p-1">Link ở đây</a></p>
<b>Các bước thực hiện</b>
<ul>
<li>B1: Tạo thư mục source để chứa các soure code</li>
<li>B2: Chỉnh sửa .env</li>
PHP_VERSION=7.2
MARIADB_DATABASE=default
MARIADB_USER=default
MARIADB_PASSWORD=secret
MARIADB_PORT=3306
MARIADB_ROOT_PASSWORD=root
MARIADB_ENTRYPOINT_INITDB=./mariadb/docker-entrypoint-initdb.d

<li>B3: Tạo file config nginx. Copy file example rồi thay đổi domain local</li>
<li>B4: Chạy lệnh docker-compose build -d nginx mariadb adminer workspace để build các image cho docker</li>
<li>B5: Chạy lệnh docker-compose up -d nginx mariadb adminer workspace để build các image cho docker</li>
<li>B6: Chạy file ssh.sh để vào wordpace project</li>
</ul>

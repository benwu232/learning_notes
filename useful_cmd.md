### docker
docker stop $(docker ps -q)

docker rm $(docker ps -aq)

docker run --rm -it --name docker-stacks docker/stacks:latest /bin/bash

### jupyter

jupyter lab --ip 0.0.0.0 --port 8888

jupyter nbconvert --to script bigtable.ipynb 

### sql

mysql -u growth_hacker -p -h 10.10.33.43

use test_db;

show tables;

drop table err_log;

describe err_log;

SELECT * FROM err_log;

select count(*) from rounds28;

select * from rounds28 order by started_at desc limit 1;

ALTER TABLE abc ROW_FORMAT=COMPRESSED;

ALTER TABLE abc KEY_BLOCK_SIZE=4;

chown -R mysql:mysql /var/lib/mysql/

create user 'abc'@'localhost' identified by '*Abcd1234';

GRANT ALL PRIVILEGES ON *.* TO 'abc'@'%'IDENTIFIED BY '*Abcd1234' WITH GRANT OPTION;

GRANT ALL PRIVILEGES ON *.* TO 'abc'@'localhost' IDENTIFIED BY '*Abcd1234' WITH GRANT OPTION;

FLUSH privileges;

get table size:

`SELECT 
    table_name AS `Table`, 
    round(((data_length + index_length) / 1024 / 1024), 2) `Size in MB` 
FROM information_schema.TABLES 
WHERE table_schema = "test_db"
    AND table_name = "abc";
`
systemctl start mariadb #启动MariaDB
systemctl stop mariadb #停止MariaDB
systemctl restart mariadb #重启MariaDB
systemctl enable mariadb #设置开机启动

### youtube-dl

youtube-dl -f 137+251 https://www.youtube.com/playlist?list=PLiRrp7UEG13bjai3mwraHEqjxBfoRJadd

下載並合併格式，需要ffmpeg

youtube-dl -f best https://www.youtube.com/playlist?list=PLiRrp7UEG13bjai3mwraHEqjxBfoRJadd

You can merge the video and audio of two formats into a single file using -f <video-format>+<audio-format> (requires ffmpeg or avconv installed), for example -f bestvideo+bestaudio will download the best video-only format, the best audio-only format and mux them together with ffmpeg/avconv.

youtube-dl https://www.youtube.com/playlist?list=PLRvtZpAxKyorZNp291m0DlOL1q5Qj0ZX- -4 -F (--list-format)

列出所有格式，強制使用Ipv4

https://github.com/ytdl-org/youtube-dl

### kill a process by port

#### win

netstat -ano | findstr :8051

taskkill /f /pid 2772

### VIM

%s#\(new\|keep\)_players#month_\1_players#gc

replace with backreference

/\d\+ 查找数字

\r 换行

### Configure pyspark in pycharm

File - Settings - Project structure - Add Content Root (/opt/spark/python/lib/ pyspark.zip, py4j*src.zip)

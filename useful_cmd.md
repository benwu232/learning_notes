#### docker
docker stop $(docker ps -q)

docker rm $(docker ps -aq)

docker run --rm -it --name docker-stacks docker/stacks:latest /bin/bash

#### jupyter

jupyter lab --ip 0.0.0.0 --port 8888

jupyter nbconvert --to script bigtable.ipynb 

#### sql

mysql -u growth_hacker -p -h 10.10.33.43

use test_db;

show tables;

drop table err_log;

describe err_log;

SELECT * FROM err_log;

select count(*) from rounds28;

select * from rounds28 order by started_at desc limit 1;


#### youtube-dl

youtube-dl -f 137+251 https://www.youtube.com/playlist?list=PLiRrp7UEG13bjai3mwraHEqjxBfoRJadd

下載並合併格式，需要ffmpeg

youtube-dl https://www.youtube.com/playlist?list=PLRvtZpAxKyorZNp291m0DlOL1q5Qj0ZX- -4 -F (--list-format)

列出所有格式，強制使用Ipv4

https://github.com/ytdl-org/youtube-dl



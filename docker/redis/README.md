确保conf下面有redis配置文件
确保data下面有dump.rdb文件（提前准备好，私募缓存文件）

./docker-build.sh 生成images

docker run -p 6379:6379 --name portal-redis -d portal-redis redis-server --requirepass 'Cscs@31$2016#'

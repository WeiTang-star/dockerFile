# 记录一些dockerFile
1. 需要创建NetWork：
docker network create --driver bridge --subnet 172.23.0.0/25 --gateway 172.23.0.1  tang_network
2. 容器内的数据保存在 dockerFileData 中

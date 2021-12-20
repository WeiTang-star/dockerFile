# 记录一些dockerFile
1. 需要创建NetWork：
docker network create --driver bridge --subnet 172.23.0.0/25 --gateway 172.23.0.1  tang_network
2. 容器内的数据保存在 dockerFileData 中
3. 启动命令 
docker-compose -f docker-compose.yml up -d
4. 删除当前所有容器
   docker rm -f $(docker ps -a | awk '{print $1}' | sed -n '2,10'p)
5. 解除network关联
   docker network disconnect -f tang_network zookeeper_2

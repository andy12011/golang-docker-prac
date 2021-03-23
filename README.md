# golang-docker-prac

<li>FROM: 指定base image
<li>WORKDIR: 指定docker執行起來時候的預設目錄位置
<li>EXPOSE: 指定所有發布的port
<li>CMD: 指定Instance啟動後所要執行的指令
<li>ENTRYPOINT: 指令Instance啟動後，程式的進入點
語法筆記

<a>https://blog.gtwang.org/linux/docker-commands-and-container-management-tutorial/</a>


docker build -t andy:gotest .

#container-port:local-port

docker run --rm -p 7000:7000 -d andy

docker run --rm -p 7000:7000 -d andy:gotest

docker ps //顯示containerId

docker stop d491a189f632 //停止

docker images //顯示所有映像檔

docker tag {imageId} {accountName}/imageName:{version} //先做版本印象檔
docker push {accountName}/imageName:{version} //推上

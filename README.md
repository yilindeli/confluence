# confluence
一键安装基于端口访问的 Confluence


## install docker and docker-compose

## fit your port 8090 or ...

## docker-compose up and check "========= agent working ==========="

## visit 127.0.0.1:8090 install

## get license key by 
    > 设置产品类型：-p conf， 详情可执行：java -jar atlassian-agent.jar 
    docker-compose exec app java -jar /opt/atlassian/confluence/atlassian-agent.jar -d -m test@test.com -n BAT -p conf -o TAB -s BBES-DK9H-RX5Z-9SDS

    如果上个页面中也选择了安装团队日程表，则可执行下面的命令获得授权码：
    docker-compose exec app java -jar /opt/atlassian/confluence/atlassian-agent.jar -p tc -m test@test.com -n my_name -o https://zhile.io -s BBES-DK9H-RX5Z-9SDS

    如果上个页面中也选择了Confluence Questions表，则可执行下面的命令获得授权码：
    docker-compose exec app java -jar /opt/atlassian/confluence/atlassian-agent.jar -p questions -m test@test.com -n my_name -o https://zhile.io -s BBES-DK9H-RX5Z-9SDS
## 安装时选择 Standalone => postgresql 
    by connection string 中，把localhost替换成db即可。
    Setup type : By connection string
    Database URL: dbc:postgresql://db:5432/confluence
    Username:  confluence
    Password: confluence
    
## Hello confluence
    Confluence Base URL Should Match But Does Not
        https://confluence.atlassian.com/conf73/configuring-the-server-base-url-991928713.html
        https://confluence.atlassian.com/confkb/your-url-doesn-t-match-warning-in-confluence-6-1-or-later-881545925.html
    https://confluence.atlassian.com/confkb/can-t-check-base-url-warning-in-confluence-6-6-or-later-939718433.html

## https://confluence.atlassian.com/doc/make-a-space-public-829076202.html
## 说明

- 1. Confluence 对 mysql要求苛刻，故使用 postgres:9.6，详见 https://confluence.atlassian.com/doc/supported-platforms-207488198.html
- 2. Confluence 对 系统要求较高，MAC 虚拟机2核2G安装时并不够用，而且老卡
- 3. 我们推荐你手工备份Confluence数据库、home目录及附件. 更多信息请查看 我们的在线文档。https://confluence.atlassian.com/doc/configuring-backups-138348.html
- 4. APP https://confluence.atlassian.com/doc/invite-your-team-to-use-the-app-947159481.html
    Download the app for:

    Android: https://play.google.com/store/apps/details?id=com.atlassian.confluence.server
    iOS (Apple) https://itunes.apple.com/us/app/id1288365159?mt=8.

## confluence使用
    详细信息请参考: 官方中文文档

## 参考链接
    - https://gitee.com/pengzhile/atlassian-agent
        https://zhile.io/2018/12/20/atlassian-license-crack.html
    - 安装及破解confluence插件 https://www.qinjj.tech/2019/01/04/confluence%20install/
    - https://blog.csdn.net/ked/article/details/77297506
    - 如果卡的话，参考设置最大堆内存设置 https://www.cnblogs.com/rslai/p/8845777.html
    - https://github.com/jgrodziski/docker-confluence
    - https://www.runoob.com/manual/PostgreSQL/index.html
        https://www.runoob.com/postgresql/postgresql-tutorial.html
    - https://www.jianshu.com/p/b95ceabd3e9d 通过Docker安装JIRA和Confluence（破解版）

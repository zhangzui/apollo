#模块的内容
1.adminservice:admin服务
2.assembly:一个启动main函数类：
3.biz
4.buildtools:构建工具；自动化部署脚本
5.client：客户端
6.common：公共资源RestController
7.configservice：配置服务
8.core：核心组件
9.demo：客户端连接apollo的示例
10.portal:门户和管理端
#本地启动

1.先启动构建脚本，将启动参数，数据库配置信息，打包构建;
2.启动：config_service,admin_service,最后启动portal
    启动先后顺序：1.config_service：配置服务，端口8080，Eureka 服务注册
            2.admain_service：8090一些restAPI
            3.管理端：8070

    a.target目录下进行启动：jar文件
        ./apollo-configservice-0.11.0-SNAPSHOT.jar
        ./apollo-amdinservice-0.11.0-SNAPSHOT.jar
        ./apollo-portal-0.11.0-SNAPSHOT.jar
    b.采用启动脚本
    c.main 函数：ApolloApplication启动，带上参数--configservice --adminservice
        注意：需要将数据库配置信息，进行手打填充，或者自行配置
    d.官网下载部署包:然后启动demo.sh脚本，需要修改数据库参数
3.eura


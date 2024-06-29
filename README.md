



## maven下载和配置
- 下载
   - https://maven.apache.org/download.cgi
- 配置环境变量
   - MAVEN_HOME
   - PATH



## 目录说明
1. maventest1  （手动创建相应的文件）
2. maventest2   (mvn 运用架构自动配置框架项目)  详情搜索 7768xnxn
mvn archetype:generate -DgroupId=com.hfbhfb -DartifactId=maventest2 -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false


## maven基础概念

- 仓库
   - 本地仓库，远程仓库（中央仓库，私服）
- 坐标
   - https://repo1.maven.org/maven2/
- groupId: 定义当前Maven项目隶属组织
- artifactId: maven项目名称
- version: 定义当前项目版本号


## 配置mvn默认行为 查看git提交日志 `修改本地仓库路径`  `配置ali镜像服务器proxy`
cd /d/work2/apache-maven-3.9.8
code .



## 基本操作
```sh
mvn compile # 编译

mvn clean # 清理

mvn test # 测试

mvn package # 打包

mvn install # 安装到本地仓库

```



#### maven阿里源
https://developer.aliyun.com/mvn/guide

#### maven华为源 **推荐**
https://mirrors.huaweicloud.com/mirrorDetail/5ea0025f2ab89b484a4dd5ce?mirrorName=maven&catalog=language






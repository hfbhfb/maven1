

## 基本操作
```sh
mvn compile # 编译

mvn clean # 清理

mvn test # 测试

mvn package # 打包

mvn install # 安装到本地仓库

```


## 手动准备 所有maven的文件

``` sh
mkdir -p ./src
mkdir -p ./src/main
mkdir -p ./src/main/java
mkdir -p ./src/main/resources
mkdir -p ./src/test
mkdir -p ./src/test/java
mkdir -p ./src/test/resources

mkdir -p ./src/main/java/com/testaa/
mkdir -p ./src/test/java/com/testaa/

cat > ./src/main/java/com/testaa/Demo.java <<EOF
package com.testaa;

public class Demo {

    public String say(String name) {
        System.out.println("hello " + name);
        return "hello " + name;
    }

    public static void main(String[] args) {
        System.out.println("hello ");
    }
}

EOF

cat > ./src/test/java/com/testaa/DemoTest.java <<EOF
package com.testaa;

import org.junit.Test;
import org.junit.Assert;

public class DemoTest {

    @Test
    public void testSay() {
        Demo d = new Demo();
        String ret = d.say("maven");
        Assert.assertEquals("hello maven", ret);
    }
}
EOF



cat > pom.xml <<EOF
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/maven-v4_0_0.xsd">
  <modelVersion>4.0.0</modelVersion>

  <groupId>com.testaa</groupId>
  <artifactId>my-maven-test1</artifactId>
  <version>0.1</version>
  <name>my-maven-test1</name>
  <inceptionYear>2002</inceptionYear>

  <dependencies>
    <dependency>
      <groupId>junit</groupId>
      <artifactId>junit</artifactId>
      <version>4.12</version>
    </dependency>
  </dependencies>

</project>

EOF




```



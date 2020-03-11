# 找不到mapper对应的xml

![avatar](https://github.com/sanwancoder/tech_study/blob/master/problem&solution/images/20200312010649.4840e4327532bd92408db11edcb7f61f.png?raw=true)

### 工程目录如上，server是主类，打包后无法启动


## 解决办法
```
  <build>
    <resources>
      <resource>
        <!-- 指定resources插件处理哪个目录下的资源文件 -->
        <directory>src/main/resources</directory>
        <!--注意此次必须要放在此目录下才能被访问到 必须注释掉才OK -->
<!--        <targetPath>BOOT-INF</targetPath>-->
        <includes>
          <include>**/**</include>
        </includes>
      </resource>
    </resources>
  </build>
```


![avatar](https://github.com/sanwancoder/tech_study/blob/master/problem&solution/images/20200312005828.0d7ad9325a3cd7ff9ffc17bd6ffb09f3.png?raw=true)



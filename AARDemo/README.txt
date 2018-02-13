第一步：
项目根目录的build.gradle下添加
        classpath 'com.github.dcendents:android-maven-gradle-plugin:2.0'
        classpath 'com.jfrog.bintray.gradle:gradle-bintray-plugin:1.7.3'
        classpath "org.jfrog.buildinfo:build-info-extractor-gradle:4.5.4"

第二步：
module的gradle.properties下添加
        PROJ_GROUP=com.lxm.aar
        PROJ_VERSION=1.0.0
        PROJ_NAME=aarTest
        PROJ_WEBSITEURL=https://github.com/lixiaoming0314/AARLibrary
        PROJ_ISSUETRACKERURL=https://github.com/ls1110924/AARLibrary/issues
        PROJ_VCSURL=https://github.com/lixiaoming0314/AARLibrary.git
        PROJ_DESCRIPTION=A Test Lib
        PROJ_ARTIFACTID=aarLib
        LICENSE_NAME='The Apache Software License, Version 2.0'
        LICENSE_URL='http://www.apache.org/licenses/LICENSE-2.0.txt'
        DEVELOPER_ID=lixiaoming
        DEVELOPER_NAME=aman
        DEVELOPER_EMAIL=287907160@qq.com

第三步：
module的build.gradle下添加
        apply from: './bintray.gradle'

第四步：
module下新建bintray.gradle

第五步：
在terminal下执行
    ./gradlew clean build bintrayUpload

第六步：
    打开https://bintray.com/aman/maven/aarTest，添加 add to jcenter

.. title: Android Studio 使用国内源
.. slug: android-studio-shi-yong-guo-nei-yuan
.. date: 2020-05-02 02:03:08 UTC+08:00
.. tags: Android
.. category: Android
.. link: 
.. description: 
.. type: text

修改项目的build.gradle文件, 把

.. code-block :: javascript
    :linenos:
    
    buildscript {
    
        repositories {
            google()
            jcenter()
            
        }
        dependencies {
            classpath 'com.android.tools.build:gradle:3.6.3'
            

            // NOTE: Do not place your application dependencies here; they belong
            // in the individual module build.gradle files
        }
    }

    allprojects {
        repositories {
            google()
            jcenter()
            
        }
    }

    task clean(type: Delete) {
        delete rootProject.buildDir
    }

修改成

.. code-block :: javascript
    :linenos:
    
    buildscript {
    
        repositories {

            maven{ url 'https://maven.aliyun.com/nexus/content/groups/public/' }
            maven{ url 'https://maven.aliyun.com/repository/google'}
            maven{ url 'https://maven.aliyun.com/repository/gradle-plugin'}
            maven{ url 'https://maven.aliyun.com/repository/public'}
            maven{ url 'https://maven.aliyun.com/repository/jcenter'}
            
        }
        dependencies {
            classpath 'com.android.tools.build:gradle:3.6.3'
            

            // NOTE: Do not place your application dependencies here; they belong
            // in the individual module build.gradle files
        }
    }

    allprojects {
        repositories {

            maven{ url 'https://maven.aliyun.com/nexus/content/groups/public/' }
            maven{ url 'https://maven.aliyun.com/repository/google'}
            maven{ url 'https://maven.aliyun.com/repository/gradle-plugin'}
            maven{ url 'https://maven.aliyun.com/repository/public'}
            maven{ url 'https://maven.aliyun.com/repository/jcenter'}
            
        }
    }

    task clean(type: Delete) {
        delete rootProject.buildDir
    }

    
    

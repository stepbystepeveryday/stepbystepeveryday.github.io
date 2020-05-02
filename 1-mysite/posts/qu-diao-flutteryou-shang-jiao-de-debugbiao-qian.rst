.. title: 去掉Flutter右上角的debug标签
.. slug: qu-diao-flutteryou-shang-jiao-de-debugbiao-qian
.. date: 2020-05-02 14:28:34 UTC+08:00
.. tags: Flutter
.. category: Flutter
.. link: 
.. description: 
.. type: text

.. code-block :: dart
    :linenos:

    class MyApp extends StatelessWidget {
        @override
        Widget build(BuildContext context) {
            return MaterialApp(
                title: '测试程序',
                debugShowCheckedModeBanner: false, // 去掉右上角的debug标签
                theme: ThemeData(
                primarySwatch: Colors.blue,
                ),
            home: MyHomePage(title: "测试程序"),
            );
        }
    }

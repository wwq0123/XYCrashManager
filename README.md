# XYCrashManager
* swift crash manager是一个可在swift上捕获crash的demo，已经集成捕获，存储，读取，删除crash信息等功能。
* 本Demo在第二次打开APP时将你上次崩溃的信息显示在屏幕上以方便你观察。SlideAdressTool.h及SlideAdressTool.m用来调用C方法获取SlideAdress
* 如果不想关心具体实现，可将CrashManager直接拖到你的工程中并将`SlideAdressTool.h`添加到你的桥接文件中，然后在AppDelegate中的如下方法中添加代码即可使用，具体实现可以了解[实现文档](http://www.jianshu.com/p/d2b7a2eb36ba)

        func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplicationLaunchOptionsKey: Any]?) -> Bool {
        // Override point for customization after application launch.
        
        //crash捕获
        crashHandle { (crashInfoArr) in
            
            for info in crashInfoArr{
                //这里添加对每一条crash信息的操作
            }
        }
        
        return true
        }

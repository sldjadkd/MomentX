# 关于动态Dex加载
**注意：这是一个实验性功能，我不保证该功能的可用性。**


对于每个Dex，你需要编写如以下形式的入口类：


其中类名和入口方法可自定义。


Java版本：
```java
package com.sb114514.moment.dex;

import android.content.Context;
import androidx.annotation.NonNull;

public static class EntryClass {
    /**
     * @param context 源自[android.app.Application.attachBaseContext]
     * */
    public static void entryMethod(@NonNull Context context) {
        // 你的代码...
    }
}
```
Kotlin版本：
```kotlin
package com.sb114514.moment.dex

import android.content.Context

class EntryClass {
    companion object {
        /**
         * @param context 源自[android.app.Application.attachBaseContext]
         * */
        @JvmStatic // 务必添加此注解。模块依靠反射来invoke入口方法。
        fun entryMethod(context: Context) {
            // 你的代码...
        }
    }
}
```
或
```kotlin
package com.sb114514.moment.dex

import android.content.Context

object EntryObject {
    /**
     * @param context 源自[android.app.Application.attachBaseContext]
     * */
    @JvmStatic // 务必添加此注解。模块依靠反射来invoke入口方法。
    fun entryMethod(context: Context) {
        // 你的代码...
    }
}
```


然后这个功能能干啥哩？我也不知道。


~~此功能源自于[某人](https://github.com/ReChoilles)的建议~~
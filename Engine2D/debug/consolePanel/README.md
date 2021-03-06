在桌面端我们能够方便的使用 `console` 提供的诸多方法输出日志，然后使用浏览器提供的开发者工具查看。

但是在移动端这个方式收到了限制，大多数的浏览器没有方便的方法来查看日志。
因此 Egret 集成了向屏幕输出日志的功能，方便移动设备调试。

![显示日志](575e991fdd5f8.png)

## 打开日志显示开关

在 template/index.html 中能够很方便的控制日志的显示状态。

```
    <div style="margin: auto;width: 100%;height: 100%;" class="egret-player"
         data-entry-class="Main"
         data-orientation="auto"
         data-scale-mode="noScale"
         data-frame-rate="30"
         data-content-width="480"
         data-content-height="800"
         data-show-paint-rect="false"
         data-multi-fingered="2"
         data-show-fps="true" data-show-log="false"
         data-log-color="#b0b0b0"> 
     </div>
```

* data-show-log： 设置是否在屏幕中显示日志。 true 显示，false 不显示。

## 输出日志

在代码中可以直接调用 `egret.log(message?:any, ...optionalParams:any[])` 来输出日志。
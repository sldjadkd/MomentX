## 准备步骤
首先，在`子模块设置`内启用`HTTPS解密`

## 如何查看解密数据
将手表连上电脑，输入以下命令
```bash
adb logcat -s MomentHttpsDbg
```
或
```bash
adb shell logcat -s MomentHttpsDbg
```
或使用[Android Studio](https://developer.android.google.cn/studio?hl=zh-cn)，打开任意项目在左侧工具栏选择`Logcat`图标（不推荐）

然后你就能看到如下面的输出：

> [!IMPORTANT]
> **注：`滚木滚木`均为手动打码部分，请注意个人信息安全**

```text
--------- beginning of crash
--------- beginning of main
--------- beginning of system
08-28 18:00:22.991  4646  4689 I MomentHttpsDbg: 请求：[POST] https://api.watch.okii.com/social-service/violation/initViolationInfo
08-28 18:00:23.496  4646  4689 I MomentHttpsDbg: - uuid: 滚木滚木
08-28 18:00:23.698  4646  4689 I MomentHttpsDbg: 明文请求：
08-28 18:00:23.698  4646  4689 I MomentHttpsDbg: eebbkKey=滚木滚木
08-28 18:00:23.698  4646  4689 I MomentHttpsDbg: aesKey=滚木滚木
08-28 18:00:23.698  4646  4689 I MomentHttpsDbg: body={"informSource":3,"watchId":"滚木滚木"}
08-28 18:00:23.724  4646  4692 I MomentHttpsDbg: 请求：[GET] https://api.watch.okii.com/social-service/prerogative/getResource
08-28 18:00:23.799  4646  4695 I MomentHttpsDbg: 请求：[POST] https://moment.watch.okii.com/moment/search
08-28 18:00:25.255  4646  4692 I MomentHttpsDbg: - uuid: 滚木滚木
08-28 18:00:25.446  4646  4681 I MomentHttpsDbg: 请求：[GET] https://api.watch.okii.com/watch-game-service/treasureHunt/getVersionNumber
08-28 18:00:25.508  4646  4682 I MomentHttpsDbg: 请求：[POST] https://api.watch.okii.com/watch-game-service/talentshow/getVersion
08-28 18:00:25.712  4646  4695 I MomentHttpsDbg: - uuid: 滚木滚木
08-28 18:00:25.786  4646  4695 I MomentHttpsDbg: 明文请求：
08-28 18:00:25.786  4646  4695 I MomentHttpsDbg: eebbkKey=滚木滚木
08-28 18:00:25.786  4646  4695 I MomentHttpsDbg: aesKey=滚木滚木
08-28 18:00:25.786  4646  4695 I MomentHttpsDbg: body={"begin":0,"commentPageSize":5,"currentWatchId":"滚木滚木","end":1787911222122,"firstQuery":true,"friend":1,"from":0,"lastLikeTime":1787911222134,"searchPermission":1,"size":10,"watchId":"滚木滚木"}
08-28 18:00:26.134  4646  4692 I MomentHttpsDbg: 明文响应：
08-28 18:00:26.134  4646  4692 I MomentHttpsDbg: body={"code":"000007","desc":"request parameter is invalid."}
08-28 18:00:26.321  4646  4682 I MomentHttpsDbg: - uuid: 滚木滚木
08-28 18:00:26.337  4646  4681 I MomentHttpsDbg: - uuid: 滚木滚木
08-28 18:00:26.344  4646  4695 I MomentHttpsDbg: 明文响应：
08-28 18:00:26.344  4646  4695 I MomentHttpsDbg: body={"code":"000007","desc":"request parameter is invalid."}
08-28 18:00:26.356  4646  4682 I MomentHttpsDbg: 明文请求：
08-28 18:00:26.356  4646  4682 I MomentHttpsDbg: eebbkKey=滚木滚木
08-28 18:00:26.356  4646  4682 I MomentHttpsDbg: aesKey=滚木滚木
08-28 18:00:26.356  4646  4682 I MomentHttpsDbg: body={"openId":"滚木滚木"}
08-28 18:00:26.538  4646  4681 I MomentHttpsDbg: 明文响应：
08-28 18:00:26.538  4646  4681 I MomentHttpsDbg: body={"code":"000007","desc":"request parameter is invalid."}
```

> [!NOTE]
> ~~功能还不是很完善~~

> [!TIP]
> 配合[Reqable](https://reqable.com/zh-CN/download/)使用效果更佳
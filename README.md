# fas-rs-extension-offset
一个fas-rs插件。通过设置offset以减少空转优化fas效果，推荐搭配asoulopt使用。若fas-rs版本低于3.1.0，推荐开启controll_min_freq开关。
## SoC及游戏的适配
### 已适配SoC
- SM7475
- SM7675
- SM8450
- SM8475
- SM8550
### SM7475
- 原神
- Genshin Impact
- 王者荣耀
- Honor of Kings
- 永劫无间
- 和平精英
- 绝区零
- 英雄联盟手游
- 穿越火线
- 崩坏：星穹铁道
- 使命召唤
- 王牌竞速
- 金铲铲之战
### SM7675
- 原神
- Genshin Impact
- 崩坏：星穹铁道
- 鸣潮
- 绝区零
- 永劫无间
- 火影忍者
- 王者荣耀
- Honor of Kings
- 英雄联盟手游
- QQ飞车
- 和平精英
- PUBGMobile
- 暗区突围
- 光遇
- 金铲铲之战
- 战双帕弥什
- 穿越火线
- 荒野乱斗
### SM8450&SM8475
- 原神
- Genshin Impact
- 王者荣耀
- Honor of Kings
- 我的世界
- Minecraft PE
- 绝区零
- Zenless Zone Zero
- 元气骑士
- Soul Knight
- 和平精英
- 英雄联盟手游
- 穿越火线-枪战王者
- 永劫无间
- 巅峰极速
- 极品飞车: 集结
- 鸣潮
- 明日方舟
- 光遇
- 金铲铲之战
- QQ飞车
- 火影忍者
- 逆水寒手游
### SM8550
- 原神
- Genshin Impact
- 崩坏：星穹铁道
- 鸣潮
- 绝区零
- 永劫无间
- 火影忍者
- 王者荣耀
- Honor of Kings
- 英雄联盟手游
- QQ飞车
- 和平精英
- PUBGMobile
- 暗区突围
- 光遇
- 金铲铲之战
- 战双帕弥什
- 穿越火线
- 荒野乱斗
# fas-rs-extension-schedhorizon
一个fas-rs插件。游戏时由fas-rs接管CPU调度，fas-rs取消接管后回到schedhorizon调度。
## schedhorizon
schedhorizon是schedutil的修改版，它引入两个可优化参数efficient_freq和up_delay，它会将CPU频率压制在efficient_freq以下，以免CPU频繁运行在高频下。当请求的频率超过efficient_freq的时间超过 up_delay，将解除CPU频率限制，以应对重负载。频率限制会在应用冷启动和高内存压力内存重新分配时短时解除。使用schedhorizon不可以使用其他CPU调度程序。
## SoC及游戏的适配
### 已适配SoC
- SM7475
- SM7675
- SM8450
- SM8475
- SM8550

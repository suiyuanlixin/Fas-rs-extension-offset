# Fas-rs-extension
一个Fas-rs的插件整合。为Fas-rs提供频率偏移、Schedhorizon日用调度、CPU限制器等功能。
## Fas-rs-extension-offset
一个Fas-rs插件。通过设置offset以减少空转优化Fas效果，推荐搭配Asoulopt使用。若Fas-rs版本低于3.1.0，推荐开启controll_min_freq开关。
## Offset已适配的SoC
- SM7475
- SM7675
- SM8250
- SM8350
- SM8450
- SM8475
- SM8550
- SM8635
- SM8650
- MT6895
- MT6896
- MT6983
- MT6985
- MT6989
## Offset已适配的游戏
### SM8650
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
- 英雄联盟手游
- 逆水寒
- 崩坏：星穹铁道
- 来自星尘
- 尘白禁区
- 火影忍者
- 永劫无间
- 和平精英
### SM8635
- 王者荣耀
- Honor of Kings
### SM8550/SM7675
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
### SM8450/SM8475
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
### SM8350
- 原神
- Genshin Impact
- 王者荣耀
- Honor of Kings
- 永劫无间
- 和平精英
- 光遇
- 金铲铲之战
- 鸣潮
- 绝区零
- QQ飞车
### SM8250
- 和平精英
- PUBGMobile
### MT6895/MT6896
- 原神
- Genshin Impact
- 王者荣耀
- Honor of Kings
- 绝区零
- 我的世界
- Minecraft PE
- 元气骑士
- Soul Knight
- 和平精英
- 英雄联盟手游
- 穿越火线
- 永劫无间
- 巅峰极速
- 极品飞车: 集结
### MT6983
- 王者荣耀
- Honor of Kings
- 穿越火线
- 和平精英
- 英雄联盟手游
- 使命召唤
- 第五人格
### MT6985
- 王者荣耀
- Honor of Kings
- 英雄联盟手游
### MT6989
- 王者荣耀
- Honor of Kings
- 光遇
- 崩坏：星穹铁道
# Fas-rs-extension-schedhorizon
一个Fas-rs插件。游戏时由Fas-rs接管CPU调度，Fas-rs取消接管后回到Schedhorizon调度。
## Schedhorizon
Schedhorizon是Schedutil的修改版，它引入两个可优化参数efficient_freq和up_delay，它会将CPU频率压制在efficient_freq以下，以免CPU频繁运行在高频下。当请求的频率超过efficient_freq的时间超过 up_delay，将解除CPU频率限制，以应对重负载。频率限制会在应用冷启动和高内存压力内存重新分配时短时解除。使用Schedhorizon不可以使用其他CPU调度程序。
## Schedhorizon已适配的SoC
- SM7475
- SM7675
- SM8450/SM8475
- SM8550
- MT6895/MT6896
- MT6983
# Fas-rs-extension
一个Fas-rs的插件整合。为Fas-rs提供频率偏移、Schedhorizon日用调度、CPU限制器等功能。
# Fas-rs-extension-offset
一个Fas-rs插件。通过设置offset以减少空转优化Fas效果，推荐搭配Asoulopt使用。若Fas-rs版本低于3.1.0，推荐开启controll_min_freq开关。
## 已适配的SoC
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
# Fas-rs-extension-schedhorizon
一个 fas-rs 插件。游戏时由Fas-rs接管CPU调度，Fas-rs取消接管后回到Schedhorizon调度。
## Schedhorizon
Schedhorizon是Schedutil的修改版，它引入两个可优化参数efficient_freq和up_delay，它会将CPU频率压制在efficient_freq以下，以免CPU频繁运行在高频下。当请求的频率超过efficient_freq的时间超过 up_delay，将解除CPU频率限制，以应对重负载。频率限制会在应用冷启动和高内存压力内存重新分配时短时解除。使用Schedhorizon不可以使用其他CPU调度程序。模块设置了我认为适用于大部分处理器的efficient_freq和up_delay日用参数，你可以自己调整适应其他需求。
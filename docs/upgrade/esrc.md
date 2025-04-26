---
title: (初阶)安装无缝
nav_order: 2
parent: 萌新进阶之路
---

<details open markdown="block">
  <summary>
    目录
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

---

# 视频教程

[无缝联机教程(含正版学习版，存档继承)](https://www.bilibili.com/video/BV1bKdDYTERP/){:target="_blank"}

---

# 图文教程

## 下载最新版无缝联机mod

- [无缝联机mod N网地址](https://www.nexusmods.com/darksoulsremastered/mods/899){:target="_blank"}
- [无缝联机mod Github地址](https://github.com/LukeYui/DarkSouls3SeamlessCoopRelease/releases){:target="_blank"}

N网地址会有mod详细介绍及说明，看不懂英文的话可以翻译着看

- [无缝联机mod简体中文补丁 N网地址](https://www.nexusmods.com/darksoulsremastered/mods/928){:target="_blank"}


## 无缝联机mod目录结构说明

```yaml
├─ ds1sc_launcher.exe #无缝自带启动器
└─ SeamlessCoop/
    ├─ ds1sc.dll #无缝的代码逻辑核心文件
    ├─ ds1sc_settings.ini #无缝的配置文件
    ├─ crashpad/
    │    └─ crashpad_handler.exe #无缝崩溃时dump内存的
    └─ locale/ #这个文件夹内是各国语言翻译
         └─ english.json #英文
```

把简体中文补丁放到SeamlessCoop/locale文件夹下

```yaml
├─ ds1sc_launcher.exe
└─ SeamlessCoop/
    ├─ ds1sc.dll
    ├─ ds1sc_settings.ini
    ├─ crashpad/
    │    └─ crashpad_handler.exe
    └─ locale/
         ├─ english.json
         └─ schinese.json #刚刚放进来的简体中文补丁
```

## 安装无缝联机mod

拖进游戏目录即可，注意文件夹层级结构如下图

![无缝拖进游戏目录.png](/assets/images/无缝拖进游戏目录.png)


## 无缝联机mod配置文件`SeamlessCoop/ds1sc_settings.ini`说明

可根据自己喜好自行修改，关于缩放的部分请谨慎修改，可能会影响游戏体验

{: .note }
密码`cooppassword`和语言`mod_language_override`是默认为空的，下方为了举例才填写了一个案例

```ini
[GAMEPLAY]
; 是否允许被入侵，1允许 0不允许 不想被入侵就改成0
allow_invaders = 1
; 是否有死亡惩罚，1有 0没有 开启状态下死亡会获得猩红诅咒花 坐火消除
death_debuffs = 1
; 多人游戏时是否允许召唤骨灰，1允许 0不允许
allow_summons = 1
; 队友头顶显示的信息 0显示“勾指主人” 1显示延迟 2显示人物等级 3显示死亡次数 4显示人物等级和延迟
overhead_player_display = 1
; Serverless features involve mechanics triggered by player's not related to your game seession. 0 = OFF 1 = ON
serverless_features = 1
[SCALING]
; 敌人的生命值缩放（%）（默认值：每增加一位玩家会使敌方生命值增加75%）
enemy_health_scaling = 75
; 敌人的伤害值缩放（%） （默认值：每增加一位玩家会使敌方伤害增加0%）
enemy_damage_scaling = 0
; 敌人的韧性值缩放（%）（默认值：每增加一位玩家会使敌方韧性增加30%）
enemy_posture_scaling = 30
; boss的生命值缩放（%）（默认值：每增加一位玩家会使boss生命值增加200%）
boss_health_scaling = 200
; boss的伤害值缩放（%） （默认值：每增加一位玩家会使boss伤害增加0%）
boss_damage_scaling = 0
; boss的韧性值缩放（%）（默认值：每增加一位玩家会使boss韧性增加60%）
boss_posture_scaling = 60
[PASSWORD]
; 房间密码(会话密码) 默认是空的，必须填写才能进入游戏，注意等于号后面有个空格（大家都默认的），就算密码一样，有空格和没空格也会加入不到一起
cooppassword = 123456
[SAVE]
; 存档的扩展名 (原版游戏的扩展名是.sl2). 可以使用任何字母数字字符，最大长度120
save_file_extension = co2
[LANGUAGE]
; mod的语言，留空的话就是你启动游戏时游戏的语言，如果想强制简体中文的话就填schinese，但前提是你locale文件夹内有对应的schinese.json文件，其他语言也是一样
mod_language_override = schinese
```

{: .warning }
必须填写密码才能正常进入游戏，否则会有错误提示

{: .warning }
修改配置文件后记得保存，且重启游戏才能生效(如果在开着游戏的情况下修改的话)

## 如果你是学习版，需要额外打一个联机补丁

如果你想变成学习版，**和学习版的小伙伴一起联机**，也需要打上这个补丁**变成学习版**
> 如果你有正版的话，建议复制出来一份再打这个补丁，这样的话正版和学习版是分开的，想玩哪个版本就找对应的目录启动就好了


夸克网盘：[DARKSOULSREMASTERED_Fix_Repair_Steam_Generic.zip](https://pan.quark.cn/s/e6cb2ed8c39f){:target="_blank"}


![学习版steam联机补丁.png](/assets/images/学习版steam联机补丁.png)

拖到游戏目录里

![学习版steam联机游戏目录.png](/assets/images/学习版steam联机游戏目录.png)


# 大功告成 🎉🎉🎉

> 开始游戏之前使用加速器加速一下steam，如果你不跟人联机，那不用加速

可以双击`ds1sc_launcher.exe`启动游戏了

你可能需要：[常见问题]({{site.baseurl}}/docs/common_problem/)

# 如何确定我是不是安装成功了

启动游戏之后，标题页面左上角如果显示无缝联机mod的版本号，就是安装成功了

![标题页面无缝版本号.png](/assets/images/标题页面无缝版本号.png)

# mod道具说明

进入游戏后**坐火**可以获得mod道具

![圣化眼眸宝珠.png](/assets/images/圣化眼眸宝珠.png) 开启房间的道具，房主使用

![结晶眼眸宝珠.png](/assets/images/结晶眼眸宝珠.png) 加入房间的道具，非房主玩家使用

![混沌眼眸宝珠.png](/assets/images/混沌眼眸宝珠.png) 入侵道具，入侵别的无缝联机玩家

![深渊眼眸宝珠.png](/assets/images/深渊眼眸宝珠.png) 房主使用的话是关闭房间，非房主玩家使用的话是离开房间

![禁忌典籍.png](/assets/images/禁忌典籍.png) 修改玩家之前的规则的道具，可以开友伤来PVP，也可以分队伍PVP

![干枯手指.png](/assets/images/干枯手指.png) 吸引更多的入侵者入侵你

![受咒坠饰.png](/assets/images/受咒坠饰.png) 给自己放墓灾，更多红灵

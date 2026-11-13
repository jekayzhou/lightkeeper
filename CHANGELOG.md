# 更新记录

每次发布新版本：

1. 改 `js/core/base.js` 里的 `VERSION`（游戏设置页底部会显示这个版本号）。
2. 在本文件最上面加一节，写清楚这一版的改动。
3. 运行 `python3 tools/build.py`，上传新的 zip。

每一版都附一段英文，可以直接贴到 itch.io 的 Devlog 或 Game Jolt 的动态里。

版本号规则：
- 第三位：修 bug、小调整（1.0.1 → 1.0.2）
- 第二位：新玩法、新内容（1.0 → 1.1）
- 第一位：大改版

---

## 1.0.2 · 2026-11-12

**修复**
- **画面边缘被裁掉**：画面四周原来有一圈约 8 像素的空隙，底部和右边各被裁掉一条。itch.io、Game Jolt、Poki、CrazyGames 的版本都有这个问题，现在画面铺满整个区域。
- **窄手机上面板超出屏幕**：弹出面板现在按外框计算宽度，不会再超出屏幕。

**优化**
- **电脑上的菜单改成左右两栏**：左边是标题、说明和守灯人等级，右边是全部玩法和今日任务。在 itch.io 默认的 960×640 嵌入框里，打开就能看到所有玩法按钮，不用先往下滚。手机上保持原来的上下排列。
- **菜单不再压住按钮**：菜单不会压住右下角的全屏和声音按钮。
- **显示版本号**：设置页底部会显示当前版本号。

> **Devlog（English）**
> **v1.0.2 — Layout fixes**
> - Fixed an 8px gap around the game that cut off the bottom and right edges in the embedded player.
> - The main menu now uses two columns on desktop, so every game mode is visible in the default 960×640 window without scrolling.
> - Panels no longer overflow on very narrow phones.
> - The version number is now shown at the bottom of Settings.

---

## 1.0.1 · 2026-11-12

**优化（来自玩家反馈）**

有玩家在 itch.io 评论里问：第一夜到底该常关灯省油，还是因为两面夹击只能一直开着？这说明有两条规则开局时没讲清楚：引航成功会回一点油；船潮从第几夜开始。现在补上了：

- **菜单说明**：补充了"每引航一艘船回一点油，空闲时熄灯回得更快。第 2 夜起会有船潮，第 3 夜起可能两面夹击"。
- **开局操作提示**：补充了"引航成功也会回一点油"。
- 中文、英文、日文同步更新。

> **Devlog（English）**
> **v1.0.1 — Clearer rules up front**
> Thanks to a player question in the comments, the intro now explains two things that were easy to miss:
> - Every ship you guide gives a little oil back, and switching the lamp off in quiet moments refills it faster.
> - Surges start on night 2, and from night 3 they can come from two sides at once.

---

## 1.0.0 · 2026-11-12 · 首次发布

在 itch.io 首次公开发布。

**核心玩法**
- 转动灯塔的光照住来船，光环转满，船就会改道绕开暗礁。
- 灯亮着烧油，熄灯回油；引航成功也会回一点油。
- 船潮从第 2 夜开始，第 3 夜起可能两面夹击。

**玩法模式**
- 经典：每到天亮选一项升级。
- 无尽、双灯（两人同屏）、禅模式。
- 每日一夜：所有人同一片海。
- 每周风浪：每周一换一组变数，有 0–5 级风浪等级、奖章，连续几周守到天亮还有奖励。
- 航海日志：12 章，每章最多 3 星。

**收集与成长**
- 漂流瓶惊喜、藏宝图碎片与寻宝、礁石钓鱼。
- 世界灯塔图：26 座真实灯塔，37 条航线，6 条可集齐的航线。
- 守灯人等级 30 级，解锁新的灯光颜色和灯塔涂装。
- 成就、航海日记、统计、排行榜。在 claude.ai 上是在线排行榜，其他平台记录在本机。

**天气与船只**
- 天气：雾、风暴、大潮、漩涡、流冰、满月、流星雨。
- 船只：渔船、货船、快艇、救生艇、走私船、海盗船、补给船、旗舰、幽灵船、王室游艇。

**其他**
- 灯全灭时每局可以续一盏灯：在 Poki、CrazyGames 上看激励广告，或者花 2 份灯火。
- 支持简体中文、English、日本語。
- 鼠标、触屏、键盘、手柄都能玩。
- 字体已嵌入游戏，离线和中国大陆都能正常显示。
- 存档备份码：可以把进度导出，在别的设备或平台导入。

> **Devlog（English）**
> **v1.0 — Lightkeeper is out!**
> Turn the beam, hold it on each ship until its ring fills, and guide them past the reefs until dawn. Classic nights with upgrades, Endless, a shared Daily Night, a Weekly Squall with five difficulty levels, two-player Duo, Zen, and a 12-chapter Logbook. Fish bottles out of the sea, hunt for treasure, catch fish, light 26 real lighthouses on a world map, and level up your keeper. Plays in English, 简体中文 and 日本語, on desktop and mobile.

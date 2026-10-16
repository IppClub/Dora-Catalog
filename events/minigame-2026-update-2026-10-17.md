# 2026-10-17 活动新增作品与原生分发清理

活动接口已完整读取全部 5 页，共 140 个当前作品。对比 2026-10-02 的 106 个作品 ID，新增 36 个；2 个旧作品不再出现在当前活动列表，已有目录条目保留。因此目录累计包含 142 个活动作品。

36 个新增仓库均递归检查完整文件树，并已提供原生 `init.lua`。全部带有浏览器发布归档，已在 Dora Minigame 2026 组织创建 fork、删除确认的浏览器包、添加 DORA_NATIVE.md 出处记录并提交上游 PR。所有保留文件的 Git SHA 与文件模式逐项校验一致；未执行完整游戏流程测试。

另以公开地址对《木头人》的清理 fork 做了 depth 1 浅克隆：38 个保留文件的 Git SHA 与上游基线一致，浏览器 ZIP 不在当前树中。

`stacked_chess.zip` 为原生源码包，保留。`RaccoonHeist-HTTP.zip` 经检查含 index.html、runtime.json、浏览器 wasm/data 及哈希资源目录，确认为浏览器发布包并移除。

| 作品 | 原项目 | 原生分发 fork | PR | 移除的发布包 |
| --- | --- | --- | --- | --- |
| 木头人 | [作者仓库](https://atomgit.com/code_2007/dora-Statues) | [fork](https://gitcode.com/dora-minigame-2026/code_2007-dora-Statues) | [PR #1](https://gitcode.com/code_2007/dora-Statues/merge_requests/1) | `木头人-web-html.zip` |
| 形意棋：残影 | [作者仓库](https://atomgit.com/code_2007/dora-Onitama) | [fork](https://gitcode.com/dora-minigame-2026/code_2007-dora-Onitama) | [PR #1](https://gitcode.com/code_2007/dora-Onitama/merge_requests/1) | `形意棋：残影-web-html.zip` |
| 上海堡垒 | [作者仓库](https://atomgit.com/code_2007/dora-ShanghaiFortress) | [fork](https://gitcode.com/dora-minigame-2026/code_2007-dora-ShanghaiFortress) | [PR #1](https://gitcode.com/code_2007/dora-ShanghaiFortress/merge_requests/1) | `项目15_上海堡垒-web-html.zip` |
| 光影切换 | [作者仓库](https://atomgit.com/haiyangxing4521/thelightandshadow) | [fork](https://gitcode.com/dora-minigame-2026/haiyangxing4521-thelightandshadow) | [PR #1](https://gitcode.com/haiyangxing4521/thelightandshadow/merge_requests/1) | `光影切換-web-html.zip` |
| 鬼才抓得到 | [作者仓库](https://atomgit.com/Ice_eat/ghost) | [fork](https://gitcode.com/dora-minigame-2026/Ice_eat-ghost) | [PR #1](https://gitcode.com/Ice_eat/ghost/merge_requests/1) | `ghost-web.zip` |
| 爱反射的光 | [作者仓库](https://atomgit.com/code_2007/dora-ReflectionLight) | [fork](https://gitcode.com/dora-minigame-2026/code_2007-dora-ReflectionLight) | [PR #1](https://gitcode.com/code_2007/dora-ReflectionLight/merge_requests/1) | `爱反射的光-web-html.zip` |
| 弯道漂移 | [作者仓库](https://atomgit.com/code_2007/dora-DriftLane) | [fork](https://gitcode.com/dora-minigame-2026/code_2007-dora-DriftLane) | [PR #1](https://gitcode.com/code_2007/dora-DriftLane/merge_requests/1) | `弯道漂移-web-html.zip` |
| 单程 | [作者仓库](https://atomgit.com/Dragon_Zhi/escape-velocity) | [fork](https://gitcode.com/dora-minigame-2026/Dragon_Zhi-escape-velocity) | [PR #1](https://gitcode.com/Dragon_Zhi/escape-velocity/merge_requests/1) | `escape-velocity-web-html.zip` |
| 黑白小怪兽 | [作者仓库](https://atomgit.com/YuFireee/-) | [fork](https://gitcode.com/dora-minigame-2026/YuFireee--) | [PR #1](https://gitcode.com/YuFireee/-/merge_requests/1) | `黑白小怪兽-web-html.zip` |
| 暗室 | [作者仓库](https://atomgit.com/kkkkkklsyk/DarkRoom) | [fork](https://gitcode.com/dora-minigame-2026/kkkkkklsyk-DarkRoom) | [PR #1](https://gitcode.com/kkkkkklsyk/DarkRoom/merge_requests/1) | `DarkRoom-web.zip` |
| 观鸟俱乐部 | [作者仓库](https://atomgit.com/EthanFU/BirdingClub) | [fork](https://gitcode.com/dora-minigame-2026/EthanFU-BirdingClub) | [PR #1](https://gitcode.com/EthanFU/BirdingClub/merge_requests/1) | `BirdingClub-web.zip` |
| 叠起来的国际象棋 | [作者仓库](https://atomgit.com/DandelionTides/stacked_chess) | [fork](https://gitcode.com/dora-minigame-2026/DandelionTides-stacked_chess) | [PR #1](https://gitcode.com/DandelionTides/stacked_chess/merge_requests/1) | `stacked_chess-web-html.zip` |
| 飞翔的纸飞机 | [作者仓库](https://atomgit.com/cakecaker/feiji) | [fork](https://gitcode.com/dora-minigame-2026/cakecaker-feiji) | [PR #1](https://gitcode.com/cakecaker/feiji/merge_requests/1) | `飞翔的纸飞机-H5.zip` |
| 折序 | [作者仓库](https://atomgit.com/Koikokokokoro/Fold) | [fork](https://gitcode.com/dora-minigame-2026/Koikokokokoro-Fold) | [PR #1](https://gitcode.com/Koikokokokoro/Fold/merge_requests/1) | `Fold-web-html.zip` |
| 将军棋 | [作者仓库](https://atomgit.com/code_2007/Dora-GeneralChess) | [fork](https://gitcode.com/dora-minigame-2026/code_2007-Dora-GeneralChess) | [PR #1](https://gitcode.com/code_2007/Dora-GeneralChess/merge_requests/1) | `将军棋-web-html.zip` |
| 《浣熊夜盗》 | [作者仓库](https://atomgit.com/captainczt/Raccoon_Heist) | [fork](https://gitcode.com/dora-minigame-2026/captainczt-Raccoon_Heist) | [PR #1](https://gitcode.com/captainczt/Raccoon_Heist/merge_requests/1) | `RaccoonHeist-HTML.zip`, `RaccoonHeist-HTTP.zip` |
| 齿轮狂飙 | [作者仓库](https://atomgit.com/yyr444/Dora-GearRush) | [fork](https://gitcode.com/dora-minigame-2026/yyr444-Dora-GearRush) | [PR #1](https://gitcode.com/yyr444/Dora-GearRush/merge_requests/1) | `齿轮狂飙-web-html.zip` |
| 新宿决战 | [作者仓库](https://atomgit.com/RtCt/Shinjuku_Showdown) | [fork](https://gitcode.com/dora-minigame-2026/RtCt-Shinjuku_Showdown) | [PR #1](https://gitcode.com/RtCt/Shinjuku_Showdown/merge_requests/1) | `新宿之战-web-html.zip` |
| 一个萝卜一个坑 | [作者仓库](https://atomgit.com/Koikokokokoro/FindCarrots) | [fork](https://gitcode.com/dora-minigame-2026/Koikokokokoro-FindCarrots) | [PR #1](https://gitcode.com/Koikokokokoro/FindCarrots/merge_requests/1) | `FindCarrots-web-html.zip` |
| 星空之声 | [作者仓库](https://atomgit.com/DandelionTides/voice_of_the_starry_sky) | [fork](https://gitcode.com/dora-minigame-2026/DandelionTides-voice_of_the_starry_sky) | [PR #1](https://gitcode.com/DandelionTides/voice_of_the_starry_sky/merge_requests/1) | `voice_of_the_starry_sky-web-html.zip` |
| 反2048 | [作者仓库](https://atomgit.com/DandelionTides/anti_2048) | [fork](https://gitcode.com/dora-minigame-2026/DandelionTides-anti_2048) | [PR #1](https://gitcode.com/DandelionTides/anti_2048/merge_requests/1) | `anti_2048_html.zip` |
| 夏日养蚕计 | [作者仓库](https://atomgit.com/2401_88209890/SummerSilkwormPlan) | [fork](https://gitcode.com/dora-minigame-2026/2401_88209890-SummerSilkwormPlan) | [PR #1](https://gitcode.com/2401_88209890/SummerSilkwormPlan/merge_requests/1) | `夏日养蚕记-web-html.zip` |
| 松鼠藏坚果 | [作者仓库](https://atomgit.com/yyr444/Dora-SquirrelNutStash) | [fork](https://gitcode.com/dora-minigame-2026/yyr444-Dora-SquirrelNutStash) | [PR #1](https://gitcode.com/yyr444/Dora-SquirrelNutStash/merge_requests/1) | `松鼠藏坚果-web-html.zip` |
| 不一样的围棋 | [作者仓库](https://atomgit.com/code_2007/dora_DifferentGO) | [fork](https://gitcode.com/dora-minigame-2026/code_2007-dora_DifferentGO) | [PR #1](https://gitcode.com/code_2007/dora_DifferentGO/merge_requests/1) | `不一样的围棋-web-html.zip` |
| 魔物餐厅 | [作者仓库](https://atomgit.com/EthanFU/MonsterDiner) | [fork](https://gitcode.com/dora-minigame-2026/EthanFU-MonsterDiner) | [PR #1](https://gitcode.com/EthanFU/MonsterDiner/merge_requests/1) | `MonsterDiner-web.zip` |
| 罗马建城记 | [作者仓库](https://atomgit.com/EthanFU/GloryToRome) | [fork](https://gitcode.com/dora-minigame-2026/EthanFU-GloryToRome) | [PR #1](https://gitcode.com/EthanFU/GloryToRome/merge_requests/1) | `GloryToRome-web.zip` |
| 忍者攀爬 | [作者仓库](https://atomgit.com/dust112345/Ninja-Climb) | [fork](https://gitcode.com/dora-minigame-2026/dust112345-Ninja-Climb) | [PR #1](https://gitcode.com/dust112345/Ninja-Climb/merge_requests/1) | `Ninja-Climb-web.zip` |
| 骰子吃鸡 | [作者仓库](https://atomgit.com/EthanFU/DiceRoyale) | [fork](https://gitcode.com/dora-minigame-2026/EthanFU-DiceRoyale) | [PR #1](https://gitcode.com/EthanFU/DiceRoyale/merge_requests/1) | `DiceRoyale-web.zip` |
| 一梭成画 | [作者仓库](https://atomgit.com/wangyue789/weft-painting) | [fork](https://gitcode.com/dora-minigame-2026/wangyue789-weft-painting) | [PR #1](https://gitcode.com/wangyue789/weft-painting/merge_requests/1) | `weft-painting-web.zip` |
| 黑店账本 | [作者仓库](https://atomgit.com/EthanFU/InnLedger) | [fork](https://gitcode.com/dora-minigame-2026/EthanFU-InnLedger) | [PR #1](https://gitcode.com/EthanFU/InnLedger/merge_requests/1) | `InnLedger-web.zip` |
| 引力矿工 | [作者仓库](https://atomgit.com/dust112345/Space-Miner) | [fork](https://gitcode.com/dora-minigame-2026/dust112345-Space-Miner) | [PR #1](https://gitcode.com/dust112345/Space-Miner/merge_requests/1) | `Space-Miner-web.zip` |
| 放猫咪 | [作者仓库](https://atomgit.com/EthanFU/CatDrop) | [fork](https://gitcode.com/dora-minigame-2026/EthanFU-CatDrop) | [PR #1](https://gitcode.com/EthanFU/CatDrop/merge_requests/1) | `CatDrop-web.zip` |
| 破空者 | [作者仓库](https://atomgit.com/codenoobsad/SkyBreaker) | [fork](https://gitcode.com/dora-minigame-2026/codenoobsad-SkyBreaker) | [PR #1](https://gitcode.com/codenoobsad/SkyBreaker/merge_requests/1) | `SkyBreaker-web-html.zip` |
| 影偶剧场 | [作者仓库](https://atomgit.com/wangyue789/shadow-puppet-theatre) | [fork](https://gitcode.com/dora-minigame-2026/wangyue789-shadow-puppet-theatre) | [PR #1](https://gitcode.com/wangyue789/shadow-puppet-theatre/merge_requests/1) | `shadow-web.zip` |
| 深空远航 | [作者仓库](https://atomgit.com/code_2007/dora-PlutoArrive) | [fork](https://gitcode.com/dora-minigame-2026/code_2007-dora-PlutoArrive) | [PR #1](https://gitcode.com/code_2007/dora-PlutoArrive/merge_requests/1) | `深空远航-web-html.zip` |
| 红灯街区 | [作者仓库](https://atomgit.com/gcw_UmSNPx2Y/red-light-ferry) | [fork](https://gitcode.com/dora-minigame-2026/gcw_UmSNPx2Y-red-light-ferry) | [PR #1](https://gitcode.com/gcw_UmSNPx2Y/red-light-ferry/merge_requests/1) | `dist/red-light-ferry-html.zip`, `red-light-ferry-web-html.zip` |

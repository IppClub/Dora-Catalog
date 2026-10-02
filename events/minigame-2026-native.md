# Dora Minigame 2026 原生分发清理

组织：[Dora Minigame 2026](https://gitcode.com/dora-minigame-2026)。处理日期：2026-10-02（Asia/Shanghai）。

已为全部 106 个作品建立 fork，共移除 109 个浏览器发布 ZIP。使用正常删除提交保留 Git 历史，下载器通过 `--depth 1` 避免下载旧提交中的 ZIP。每个仓库保留作者 README、许可证、源码及资源，并添加 `DORA_NATIVE.md` 记录出处。

检查了额外 ZIP 的目录内容：`BlackPowder-HTTP.zip`、`Tank Duel.zip`、`hollow-report-controls-prototype.zip` 含浏览器运行时和 index.html，已移除。源码 ZIP 及四个原生项目 ZIP 保留。`LastPirateDora-v0.13.2-Network.zip` 同时包含服务器源码、部署脚本及浏览器运行时，其 README 将它作为联机项目包使用，保留此混合用途归档。

通过比较基线提交和清理后根目录中的文件/子树 Git SHA，验证除清单文件及移除 ZIP 外的内容一致。该校验涵盖子树内容，不代表每个游戏均做过实际运行测试。

验证：全部 180 个 resource.json 通过 schema 校验；真实 Catalog.lua 解析并筛选出 106 个活动 feed 条目（96 原生、10 在线试玩）。本次仅修改下载来源，名称、介绍、封面、运行入口和试玩链接均与先前提交一致。未重复执行全部游戏或真机 QA。

匿名 HTTP 浅克隆样例：默片拟音局 Git pack 从 25,170 KiB 减到 5,249 KiB（约减少 79%）。对新 fork 禁用 credential helper 并以 depth 1 成功下载，当前树不存在 Web ZIP。坦克大战的 Git pack 从 20,825 KiB 减到 1,111 KiB（减少 94.7%），源码保留，仍按在线试玩条目展示。

| 作品 | 原作者仓库 | 原生分发 fork | 基线提交 | 移除 ZIP |
| --- | --- | --- | --- | --- |
| 默片拟音局 | [上游](https://atomgit.com/wangyue789/silent-foley-studio) | [fork](https://gitcode.com/dora-minigame-2026/wangyue789-silent-foley-studio) | `31a2a037b6804a56ad6dfdd74eca116f454d4a8d` | `foley-web.zip` |
| 切割与设置 | [上游](https://atomgit.com/DandelionTides/cut_and_settings) | [fork](https://gitcode.com/dora-minigame-2026/DandelionTides-cut_and_settings) | `ca6d4f038eb9d870d7062f8d4e432225a6c6c45b` | `cut_and_settings-web-html.zip` |
| 生命程序员 | [上游](https://atomgit.com/DandelionTides/Life_Programmer) | [fork](https://gitcode.com/dora-minigame-2026/DandelionTides-Life_Programmer) | `49a099664f0ecfcae516f42ddf0142667b87194d` | `LifeProgrammer-web-html.zip` |
| 《黑火药！》 | [上游](https://atomgit.com/captainczt/Black_Powder) | [fork](https://gitcode.com/dora-minigame-2026/captainczt-Black_Powder) | `e1cb40b70ac33f76287ef828fdd7e85b9ede8032` | `BlackPowder-HTML.zip`<br>`BlackPowder-HTTP.zip` |
| 战翼：红蓝脉冲 | [上游](https://atomgit.com/gcw_S7zWMos9/RedBlue) | [fork](https://gitcode.com/dora-minigame-2026/gcw_S7zWMos9-RedBlue) | `dfa3b9ae76fc74e5e7a8fee654c7968d4428c2ca` | `Red&Blue-web-html.zip` |
| 残影位移 | [上游](https://atomgit.com/haiyangxing4521/shadowdisplacement) | [fork](https://gitcode.com/dora-minigame-2026/haiyangxing4521-shadowdisplacement) | `e7cd85644d2291dbc50711f8f966c1a14739766e` | `shadow displacement-web-html.zip` |
| 调香师 | [上游](https://atomgit.com/Koikokokokoro/The-Perfumer) | [fork](https://gitcode.com/dora-minigame-2026/Koikokokokoro-The-Perfumer) | `8f1157e23df4ac7a74409d54a0c8ae286d55f7b4` | `The Perfumer-web-html.zip` |
| 雪球大作战 | [上游](https://atomgit.com/code_2007/dora-SnowballBlitz) | [fork](https://gitcode.com/dora-minigame-2026/code_2007-dora-SnowballBlitz) | `da44ba6948c4a5bcd6c5c5d9c35bb02d167e1853` | `雪球大作战-web-html.zip` |
| 除夕大作战 | [上游](https://atomgit.com/code_2007/dora-NiansEve) | [fork](https://gitcode.com/dora-minigame-2026/code_2007-dora-NiansEve) | `76e7b00e8ac0def139ec30f338dff8241ddd84e6` | `除夕大作战-web-html.zip` |
| 牌途 | [上游](https://atomgit.com/code_2007/dora-Handscape) | [fork](https://gitcode.com/dora-minigame-2026/code_2007-dora-Handscape) | `d036f0aab51ea52f552cee88775f119f2f9fd5f6` | `牌途-web-html.zip` |
| 深海捕食者 | [上游](https://atomgit.com/codenoobsad/Deep_Devour) | [fork](https://gitcode.com/dora-minigame-2026/codenoobsad-Deep_Devour) | `97d5d1c71fea57ad7420b64808627a977e0704db` | `Deep_Devour-web-html.zip` |
| 万物皆可乒乓 | [上游](https://atomgit.com/2401_88209890/Ping-PongEverything) | [fork](https://gitcode.com/dora-minigame-2026/2401_88209890-Ping-PongEverything) | `c87f622be609f539d4ea374dc937d8e1020261b4` | `万物皆可乒乓-web-html.zip` |
| 投壶 | [上游](https://atomgit.com/2401_88209890/Touhu) | [fork](https://gitcode.com/dora-minigame-2026/2401_88209890-Touhu) | `cccd57de21511963c5b0b1fff355f39289ae139e` | `投壶-web-html.zip` |
| 烦人的知了 | [上游](https://atomgit.com/2401_88209890/AnnoyingCicada) | [fork](https://gitcode.com/dora-minigame-2026/2401_88209890-AnnoyingCicada) | `da5f82b10ca98b1556e71fc03b267b811533f3e3` | `烦人的知了-web-html.zip` |
| 哈气方程 | [上游](https://atomgit.com/2401_88209890/HissEquation) | [fork](https://gitcode.com/dora-minigame-2026/2401_88209890-HissEquation) | `03d5b716f6d649678a6bea14ff4e2bc80839523f` | `哈气方程-web-html.zip` |
| 摸鱼模拟器 | [上游](https://atomgit.com/losdeam/just_goof_off) | [fork](https://gitcode.com/dora-minigame-2026/losdeam-just_goof_off) | `1244deafb951b875965d6e3775c0e8bbad960bdd` | `just_goof_off-web-html.zip` |
| 暗房追光 | [上游](https://atomgit.com/wangyue789/darkroom-chase) | [fork](https://gitcode.com/dora-minigame-2026/wangyue789-darkroom-chase) | `01fadf9029b7fce79593dd1b72ef345eb015e356` | `darkroom-web.zip` |
| 极光节拍 | [上游](https://atomgit.com/wangyue789/aurora-beat) | [fork](https://gitcode.com/dora-minigame-2026/wangyue789-aurora-beat) | `7cb117fa4bb9ae5184c11f6929f25e64d74e3228` | `aurora-beat-web.zip` |
| 甩甩绳子 | [上游](https://atomgit.com/zzh31/Sling) | [fork](https://gitcode.com/dora-minigame-2026/zzh31-Sling) | `499db3e0ff6801b73b869078f7d5845365bbe5f0` | `Sling-web-html.zip` |
| 《折痕秘径》 | [上游](https://atomgit.com/yyr444/Dora-11) | [fork](https://gitcode.com/dora-minigame-2026/yyr444-Dora-11) | `e29f177ad71115ef0c70d9766a7a053f242321ba` | `01-折痕秘径-web-html.zip` |
| Ratchet | [上游](https://atomgit.com/Koikokokokoro/Ratchet) | [fork](https://gitcode.com/dora-minigame-2026/Koikokokokoro-Ratchet) | `fc506655cce2a94bd59d70b25571b4969411557c` | `Ratchet-web-html.zip` |
| 引力井 | [上游](https://atomgit.com/Koikokokokoro/GravityWell) | [fork](https://gitcode.com/dora-minigame-2026/Koikokokokoro-GravityWell) | `022632c79a5ce059ed9e780ee573c911428fd1a4` | `GravityWell-web-html.zip` |
| 躲猫猫 | [上游](https://atomgit.com/EthanFU/CatHide) | [fork](https://gitcode.com/dora-minigame-2026/EthanFU-CatHide) | `ad19ffad98583a05c806664e6aa401a624337dfd` | `CatHide-web.zip` |
| 电量告急：广告大作战 | [上游](https://atomgit.com/2401_88209890/LowBattery) | [fork](https://gitcode.com/dora-minigame-2026/2401_88209890-LowBattery) | `fe8cef9daffc467742e08b188a25637ad65edc09` | `电量告急：广告大作战-web-html.zip` |
| 鹈鹕快跑 | [上游](https://atomgit.com/u-uu/run-pelican-run) | [fork](https://gitcode.com/dora-minigame-2026/u-uu-run-pelican-run) | `15c62c7e2e6bf30006ec23e3aa3704ed0181dab8` | `run-pelican-run-web-html.zip` |
| Build by Layers | [上游](https://atomgit.com/darkskyx15/build-by-layers) | [fork](https://gitcode.com/dora-minigame-2026/darkskyx15-build-by-layers) | `73daff697787189672b26d78e04a19d042e0641e` | `build-by-layers-web-html.zip` |
| 高尔夫高手 | [上游](https://atomgit.com/code_2007/dora-GolfMaster) | [fork](https://gitcode.com/dora-minigame-2026/code_2007-dora-GolfMaster) | `3f1d7d02ba1acbab7f5b94924ed2e5d4587fd617` | `高尔夫高手-web-html.zip` |
| GoldTrader | [上游](https://atomgit.com/Koikokokokoro/Goldtrader) | [fork](https://gitcode.com/dora-minigame-2026/Koikokokokoro-Goldtrader) | `ff358e194f9ab80cc98d2d4e70d07b7a132677f8` | `goldtrader-web-html.zip` |
| 空中篮球 | [上游](https://atomgit.com/zzh31/Air_Dunk) | [fork](https://gitcode.com/dora-minigame-2026/zzh31-Air_Dunk) | `348defbff8236fd7c635369814635dd6649c02a2` | `Air Dunk-web-html.zip` |
| 蒸汽小发明家 | [上游](https://atomgit.com/EthanFU/SteamInventor) | [fork](https://gitcode.com/dora-minigame-2026/EthanFU-SteamInventor) | `11906372029b13abb53f534c79e18d9325d5b568` | `SteamInventor-web.zip` |
| 幻轨弹球 | [上游](https://atomgit.com/code_2007/dora-PhasmaBall) | [fork](https://gitcode.com/dora-minigame-2026/code_2007-dora-PhasmaBall) | `8654cca2cfe02ff7f46cc78502d408296e463bb8` | `幻轨弹球-web-html.zip` |
| 抓猫咪 | [上游](https://atomgit.com/EthanFU/CatSlap) | [fork](https://gitcode.com/dora-minigame-2026/EthanFU-CatSlap) | `b1c138c8a9967c0fb9622a20bfcc62a76495b42f` | `CatSlap-web.zip` |
| 诈唬森林 | [上游](https://atomgit.com/EthanFU/BluffForest) | [fork](https://gitcode.com/dora-minigame-2026/EthanFU-BluffForest) | `136d78001e7f43475351e94e3d7a1b28ac1a7dab` | `BluffForest-web.zip` |
| 丢出那张牌 | [上游](https://atomgit.com/DandelionTides/throw_the_card) | [fork](https://gitcode.com/dora-minigame-2026/DandelionTides-throw_the_card) | `2a6b03fae0374cc0181d157e4108af3568aab982` | `throw_the_card-web-html.zip` |
| 别迟到 | [上游](https://atomgit.com/DandelionTides/Dont_be_late) | [fork](https://gitcode.com/dora-minigame-2026/DandelionTides-Dont_be_late) | `3d9c523ddad7f25c4570616b4d28030d72aa4635` | `Dont_be_late-web-html.zip` |
| The Binder Clip | [上游](https://atomgit.com/Koikokokokoro/The-Binder-Clip) | [fork](https://gitcode.com/dora-minigame-2026/Koikokokokoro-The-Binder-Clip) | `2c1aa6feff861161ea6508a17e7d5501cf0b778e` | `The Binder Clip-web-html.zip` |
| 课间十分钟 | [上游](https://atomgit.com/Koikokokokoro/ClassJump) | [fork](https://gitcode.com/dora-minigame-2026/Koikokokokoro-ClassJump) | `e1b1f5fc9ddeba648927a6e0e1d2ded831d7945b` | `classjump-web-html.zip` |
| 灵术牌MysticDeck | [上游](https://atomgit.com/spadellllll/MysticDeck) | [fork](https://gitcode.com/dora-minigame-2026/spadellllll-MysticDeck) | `f006ac7c8945adcca56dee8a8129854b871c28f7` | `灵术牌-web-html.zip` |
| 乒乓高手 | [上游](https://atomgit.com/code_2007/dora-PingpongMaster) | [fork](https://gitcode.com/dora-minigame-2026/code_2007-dora-PingpongMaster) | `d36fdd1731e3760fcb6961a092ccb4f86e44b6ab` | `乒乓高手-web-html.zip` |
| 熬夜 vs 早起 | [上游](https://atomgit.com/2401_88209890/WakeUpShowdown) | [fork](https://gitcode.com/dora-minigame-2026/2401_88209890-WakeUpShowdown) | `00d5df6e448aa95dff0df561a4ee39ed5a08ab74` | `熬夜 vs 早起-web-html.zip` |
| 纸箱猫 | [上游](https://atomgit.com/gcw_S7zWMos9/BoxCat) | [fork](https://gitcode.com/dora-minigame-2026/gcw_S7zWMos9-BoxCat) | `b62611e33c5620a9909efb5c96d08fa76569807d` | `BoxCat-web-html.zip` |
| 床下有人 | [上游](https://atomgit.com/meiweipanini/UnderTheBed) | [fork](https://gitcode.com/dora-minigame-2026/meiweipanini-UnderTheBed) | `9517320755ce593aa77adfcc245bb6e80c891641` | `UnderTheBed-web.zip` |
| 鸡中之王 | [上游](https://atomgit.com/2401_88209890/KingofChickens) | [fork](https://gitcode.com/dora-minigame-2026/2401_88209890-KingofChickens) | `d4b881c5482a75af12b3d4e50af918139f1e55de` | `鸡中之王-web-html.zip` |
| 磁暴拾荒者 | [上游](https://atomgit.com/wangyue789/magnetic-scavenger) | [fork](https://gitcode.com/dora-minigame-2026/wangyue789-magnetic-scavenger) | `bd78c638e3d30efc5a0fc1fbf315c0da721407ed` | `magnetic-web.zip` |
| 云顶温室 | [上游](https://atomgit.com/wangyue789/sky-greenhouse) | [fork](https://gitcode.com/dora-minigame-2026/wangyue789-sky-greenhouse) | `bf81fbb21bb58bc73522b79c06821d465d8cd18e` | `sky-greenhouse-web.zip` |
| 电梯塞满了 | [上游](https://atomgit.com/2401_88209890/ElevatorFull) | [fork](https://gitcode.com/dora-minigame-2026/2401_88209890-ElevatorFull) | `3d5bd9f9a8378329013cdca345ce3c72cde7c8f8` | `电梯塞满了-web-html.zip` |
| 桌面大扫除 | [上游](https://atomgit.com/2401_88209890/DesktopCleanup) | [fork](https://gitcode.com/dora-minigame-2026/2401_88209890-DesktopCleanup) | `3a86c122fbd6154845fc234b090f7c089bd8c176` | `桌面大扫除-web-html.zip` |
| 看客 | [上游](https://atomgit.com/u-uu/kankyaku) | [fork](https://gitcode.com/dora-minigame-2026/u-uu-kankyaku) | `e2f8d81ae745fc9a3ca64294e8a57077e077f177` | `kankyaku-web-html.zip` |
| 月饼对对碰 | [上游](https://atomgit.com/2401_88209890/MooncakeMatch) | [fork](https://gitcode.com/dora-minigame-2026/2401_88209890-MooncakeMatch) | `3f46fb1c7353bc85c8d02d390c8ac0cb1919b58d` | `月饼对对碰-web-html.zip` |
| 苦无跃迁 | [上游](https://atomgit.com/zzh31/Kunai_Leap) | [fork](https://gitcode.com/dora-minigame-2026/zzh31-Kunai_Leap) | `89c00c44d983f52d0f728ac72b7dd0b563cba8bf` | `Kunai Leap-web-html.zip` |
| 棱镜巡检 | [上游](https://atomgit.com/Amiya_desi/prism-patrol) | [fork](https://gitcode.com/dora-minigame-2026/Amiya_desi-prism-patrol) | `c74e00188dc43f6bdaeda67bb04319101dba6cc7` | `prism-patrol-web-html.zip` |
| One last pirate | [上游](https://atomgit.com/captainczt/One_Last_Pirate) | [fork](https://gitcode.com/dora-minigame-2026/captainczt-One_Last_Pirate) | `e9e99ad8b778356bdaa98bb5d46efc182d46342c` | `LastPirateDora-HTML.zip`<br>`LastPirateDora-v0.13.2-HTML.zip` |
| 布朗运动 | [上游](https://atomgit.com/PingGuoLiZiJvZi/brownian-motion) | [fork](https://gitcode.com/dora-minigame-2026/PingGuoLiZiJvZi-brownian-motion) | `0a9f514d2d54c77e621f1286b56cb6fb06c1abb6` | `brownian-motion-web.zip` |
| 灌篮高手 | [上游](https://atomgit.com/code_2007/dora-SlamDunk) | [fork](https://gitcode.com/dora-minigame-2026/code_2007-dora-SlamDunk) | `bbf192821f9d9917bb781b5c8879f170c389f149` | `灌篮高手-web-html.zip` |
| 猛蹬 | [上游](https://atomgit.com/2401_88209890/Mengdeng) | [fork](https://gitcode.com/dora-minigame-2026/2401_88209890-Mengdeng) | `c0fb400c764e35a4deacfdf49b5e1721a4a9c19b` | `猛蹬-web-html.zip` |
| 雾境远征 | [上游](https://atomgit.com/starwishxnyx/mistfall-extraction) | [fork](https://gitcode.com/dora-minigame-2026/starwishxnyx-mistfall-extraction) | `5a74ee0e586fcca87f4a36a92d9c4c3a683cf63a` | `MistfallExtraction-web-html.zip` |
| 重力小子 | [上游](https://atomgit.com/zzh31/Gravity_Hero) | [fork](https://gitcode.com/dora-minigame-2026/zzh31-Gravity_Hero) | `23e0da5899c917f31acc7c24a1a7ea31dec41534` | `Gravity Hero-web-html.zip` |
| 重力泡泡龙 | [上游](https://atomgit.com/starwishxnyx/gravity-bubbles) | [fork](https://gitcode.com/dora-minigame-2026/starwishxnyx-gravity-bubbles) | `970b750a32e29eea7dd296105f24abe43aaf16c7` | `gravity-bubbles-web-html.zip` |
| 七分满 | [上游](https://atomgit.com/2401_88209890/Qifenman) | [fork](https://gitcode.com/dora-minigame-2026/2401_88209890-Qifenman) | `3f5ef6f2532daae2faa319fb35378b1b9c77dfd5` | `七分满-web-html.zip` |
| 炼丹配料台 | [上游](https://atomgit.com/wangyue789/liandan-peiliaotai) | [fork](https://gitcode.com/dora-minigame-2026/wangyue789-liandan-peiliaotai) | `733368e2fcbe69cdd4d89145810676ba4af310f6` | `liandan-web-html.zip` |
| TANK DUEL | [上游](https://atomgit.com/Uyv12/D) | [fork](https://gitcode.com/dora-minigame-2026/Uyv12-D) | `22d8ef7d4fd3556081b1a1f3cb6448f981fe8ecd` | `Tank Duel.zip` |
| 摇落 | [上游](https://atomgit.com/2401_88209890/Yaolou) | [fork](https://gitcode.com/dora-minigame-2026/2401_88209890-Yaolou) | `2a8489819d1f8fa139588761dd45ff45c9219235` | `摇落-web-html.zip` |
| 迷宫坦克 | [上游](https://atomgit.com/dust112345/MazeTank) | [fork](https://gitcode.com/dora-minigame-2026/dust112345-MazeTank) | `a7f58e0f5717b4d0f466d558d21d43e1dfe3aa0d` | `MazeTank-web.zip` |
| 水果忍者：但你是忍者 | [上游](https://atomgit.com/code_2007/dora-FruitNinja) | [fork](https://gitcode.com/dora-minigame-2026/code_2007-dora-FruitNinja) | `fc241e0ffb4efcaf951318e8a341bb13d6fa11bc` | `项目11_水果忍者：但你是忍者-web-html.zip` |
| 捞金鱼 | [上游](https://atomgit.com/2401_88209890/Laojinyu) | [fork](https://gitcode.com/dora-minigame-2026/2401_88209890-Laojinyu) | `23ee6a18ed50fb5bf4792ffaa651ddec35ee2e3a` | `捞金鱼-web-html.zip` |
| 古宅惊魂：归灯 | [上游](https://atomgit.com/dfer/gu_zhai_jing_hun.dora) | [fork](https://gitcode.com/dora-minigame-2026/dfer-gu_zhai_jing_hun.dora) | `a6677ff86595fa3a1157fc76613c2142ee76ac2d` | `古宅惊魂-web-html.zip` |
| 吞噬酷跑 | [上游](https://atomgit.com/gcw_r5pPU1ky/Eat-And-Run) | [fork](https://gitcode.com/dora-minigame-2026/gcw_r5pPU1ky-Eat-And-Run) | `d909f4b2d907273cf0e60df1f97e72f13762248a` | `Eat-and-Run-web-html.zip` |
| Takt | [上游](https://atomgit.com/Koikokokokoro/Takt) | [fork](https://gitcode.com/dora-minigame-2026/Koikokokokoro-Takt) | `5cd111026ee0505769dbe71d8b2d45e688c90ed6` | `Takt-web-html.zip` |
| 裂隙突围 | [上游](https://atomgit.com/code_2007/dora-RiftBreaker) | [fork](https://gitcode.com/dora-minigame-2026/code_2007-dora-RiftBreaker) | `fb534e535662b45d26af463f740297e7c6e97516` | `裂隙突围-web-html.zip` |
| 魔线 | [上游](https://atomgit.com/losdeam/magic_line) | [fork](https://gitcode.com/dora-minigame-2026/losdeam-magic_line) | `0f98984444192c926ecea4b5bcf708d844f2f896` | `magic_line-web-html.zip` |
| 赶海 | [上游](https://atomgit.com/2401_88209890/Ganhai) | [fork](https://gitcode.com/dora-minigame-2026/2401_88209890-Ganhai) | `565ead2d35248624a7102137e5d7d967b1e25c0c` | `赶海-web-html.zip` |
| 荡索 | [上游](https://atomgit.com/2401_88209890/Dangsuo) | [fork](https://gitcode.com/dora-minigame-2026/2401_88209890-Dangsuo) | `5bcfe90e01fade26ba2bf5220a85fd4e979c1b81` | `荡索-web-html.zip` |
| 掘地爆破 | [上游](https://atomgit.com/code_2007/dora-Mineblast) | [fork](https://gitcode.com/dora-minigame-2026/code_2007-dora-Mineblast) | `d4fd27ec407b9f518a230fd25fce1825cc48b8fe` | `掘地爆破-web-html.zip` |
| 封江 | [上游](https://atomgit.com/2401_88209890/Fengjiang) | [fork](https://gitcode.com/dora-minigame-2026/2401_88209890-Fengjiang) | `416fbd3e52b4c21c1cc9a1ae3919449e9e8b6ef9` | `fengjiang-web-html.zip` |
| 月光收集站 | [上游](https://atomgit.com/codenoobsad/moonlight-station) | [fork](https://gitcode.com/dora-minigame-2026/codenoobsad-moonlight-station) | `a52384673f2cfb8fe6ba4d6c28a33e9921a99be1` | `moonlight-station-web-html.zip` |
| 一石千浪 | [上游](https://atomgit.com/2401_88209890/one-stone-thousand-waves) | [fork](https://gitcode.com/dora-minigame-2026/2401_88209890-one-stone-thousand-waves) | `e2eb6ff5ae67ec2aa63f41e53749f05d557d9982` | `一石千浪-web-html.zip` |
| 三色围棋 | [上游](https://atomgit.com/DandelionTides/small_color_go) | [fork](https://gitcode.com/dora-minigame-2026/DandelionTides-small_color_go) | `4d3039c2600f692ad238eb8c2cf1c15d7da5c8ce` | `three_color_go-web-html.zip` |
| 风铃邮差 | [上游](https://atomgit.com/starwishxnyx/wind-chime-postman) | [fork](https://gitcode.com/dora-minigame-2026/starwishxnyx-wind-chime-postman) | `98d04f0d4f122f47829a027c846d1116d0231be0` | `wind-chime-postman-web-html.zip` |
| Unshape | [上游](https://atomgit.com/Koikokokokoro/Unshape) | [fork](https://gitcode.com/dora-minigame-2026/Koikokokokoro-Unshape) | `f08a8526c1453611ff4198f5626661bd1d0688f4` | `Unshape-web-html.zip` |
| 我要吃奶酪 | [上游](https://atomgit.com/zzh31/Eat_Cheese) | [fork](https://gitcode.com/dora-minigame-2026/zzh31-Eat_Cheese) | `e38c7cf7caeeb54a04b5a3689318decff547d004` | `Eat Cheese-web-html.zip` |
| 别让公鸡打鸣 | [上游](https://atomgit.com/2401_88209890/dont-let-rooster-crow) | [fork](https://gitcode.com/dora-minigame-2026/2401_88209890-dont-let-rooster-crow) | `f5625cfc711770f795049e69e62ade8106771f94` | `别让公鸡打鸣-web-html.zip` |
| 彩块跃迁 | [上游](https://atomgit.com/code_2007/dora-BlockLeap) | [fork](https://gitcode.com/dora-minigame-2026/code_2007-dora-BlockLeap) | `172c9905e86f11d1adee943d74cd2701a12dc022` | `彩块跃迁-web-html.zip` |
| 溜球大作战 | [上游](https://atomgit.com/2401_88209890/liuqiu-big-battle) | [fork](https://gitcode.com/dora-minigame-2026/2401_88209890-liuqiu-big-battle) | `b0d3d08d7cb89414a4374abc45cbf76696cfc9ca` | `溜球大作战-web-html.zip` |
| 大肥鱼与白饭工厂 | [上游](https://atomgit.com/PingGuoLiZiJvZi/big-fish-rice-factory) | [fork](https://gitcode.com/dora-minigame-2026/PingGuoLiZiJvZi-big-fish-rice-factory) | `811d3fd3d52066ba87f110815d996fb06fc6d2b4` | `big-fish-rice-factory-web.zip` |
| 重力爆破 | [上游](https://atomgit.com/code_2007/dora-GravityBlast) | [fork](https://gitcode.com/dora-minigame-2026/code_2007-dora-GravityBlast) | `9dfacc9c6ffa04ce746cec288622f3def9bc17d8` | `重力爆破-web-html.zip` |
| 空响 | [上游](https://atomgit.com/PingGuoLiZiJvZi/hollow-report) | [fork](https://gitcode.com/dora-minigame-2026/PingGuoLiZiJvZi-hollow-report) | `da2d4939b6bb85e8639ffd5a8afa9d1c2e9c4351` | `hollow-report-controls-prototype.zip`<br>`hollow-report-web-html.zip` |
| 夷陵剑仙：夜幕斩妖 | [上游](https://atomgit.com/dfer/yi_ling_jian_xian) | [fork](https://gitcode.com/dora-minigame-2026/dfer-yi_ling_jian_xian) | `5661f10ba8cdc99efeac1c6cbb8bab4e4f887804` | `夷陵剑仙-web-html.zip` |
| 捏一下！ | [上游](https://atomgit.com/zzh31/Squish_it) | [fork](https://gitcode.com/dora-minigame-2026/zzh31-Squish_it) | `84823c06202ce3e9a4f722558a06f92dfe349607` | `Squish it-web-html.zip` |
| 子弹回收站 | [上游](https://atomgit.com/Amiya_desi/bullet-recycler) | [fork](https://gitcode.com/dora-minigame-2026/Amiya_desi-bullet-recycler) | `cfaafb69a1e513b7b95881b8eddf336d8c2a7e35` | `bullet-recycler-web-html.zip` |
| 愤怒的小鸟：飞天猪的逆袭 | [上游](https://atomgit.com/code_2007/Angry_Birds_Pig_Revolt) | [fork](https://gitcode.com/dora-minigame-2026/code_2007-Angry_Birds_Pig_Revolt) | `1302196e5eb1c956dd961dbfc0ec995c3990687d` | `愤怒的小鸟：飞天猪的逆袭-web-html.zip` |
| 捣蛋鬼我来捣蛋 | [上游](https://atomgit.com/zzh31/Do_not_Look_Back) | [fork](https://gitcode.com/dora-minigame-2026/zzh31-Do_not_Look_Back) | `b1b7e895b0511c83c6ba276f8eb78b88c61df0e2` | `Don’t Look Back-web-html.zip` |
| 叠影 | [上游](https://atomgit.com/2401_88209890/DieYing) | [fork](https://gitcode.com/dora-minigame-2026/2401_88209890-DieYing) | `0c52e098b7ccb2dbb759a91fd8a0be3b21e037bb` | `叠影-web-html.zip` |
| 推箱的蛇 | [上游](https://atomgit.com/code_2007/dora-BoxSnake) | [fork](https://gitcode.com/dora-minigame-2026/code_2007-dora-BoxSnake) | `f398d56bce1bc7b3f0aa00e53bfaa08f296404d9` | `推箱的蛇-web-html.zip` |
| 纸翼 | [上游](https://atomgit.com/PingGuoLiZiJvZi/paper-wings) | [fork](https://gitcode.com/dora-minigame-2026/PingGuoLiZiJvZi-paper-wings) | `83cff4ff85b3519b0d09bf809a74bcb101a75698` | `paper-wings-web-html.zip` |
| 撕碎0分试卷 | [上游](https://atomgit.com/zzh31/rip_the_zero) | [fork](https://gitcode.com/dora-minigame-2026/zzh31-rip_the_zero) | `87058a19485a00e425d31a1b495f7bfdee6d8d9e` | `Rip the Zero!-web-html.zip` |
| 时钟树 | [上游](https://atomgit.com/PingGuoLiZiJvZi/clock-tree) | [fork](https://gitcode.com/dora-minigame-2026/PingGuoLiZiJvZi-clock-tree) | `fea7b0c29fd1a42a4586351a48dbb9de243ed24d` | `clock-tree-web-html.zip` |
| 俄罗斯消消块 | [上游](https://atomgit.com/code_2007/dora-BlockMatch) | [fork](https://gitcode.com/dora-minigame-2026/code_2007-dora-BlockMatch) | `970db1e4db395c08df7e32efe7cfb76aad7bfe7e` | `俄罗斯消消块-web.zip` |
| 镜反 | [上游](https://atomgit.com/2401_88209890/JingFan) | [fork](https://gitcode.com/dora-minigame-2026/2401_88209890-JingFan) | `f2dd12e2b4e92422cbf3eba41ce599e760a889e5` | `镜反-web-html.zip` |
| 音跃落痕 | [上游](https://atomgit.com/haiyangxing4521/melody-fade) | [fork](https://gitcode.com/dora-minigame-2026/haiyangxing4521-melody-fade) | `68eedb1533cd4de3e0399f2d5fc8feadef0288db` | `音跃落痕-web-html.zip` |
| 围城 | [上游](https://atomgit.com/code_2007/dora-siege) | [fork](https://gitcode.com/dora-minigame-2026/code_2007-dora-siege) | `bcc75e851a8042c1bc8cfc2bb6e88462260a76cd` | `围城-web.zip` |
| 引力禁区 | [上游](https://atomgit.com/zzh31/AVOID_THE_BLACK_CORE) | [fork](https://gitcode.com/dora-minigame-2026/zzh31-AVOID_THE_BLACK_CORE) | `7037cbb86a9822f864e696f8a54ede3a976d15c9` | `Away-The-Black-web-html.zip` |
| 纳维-斯托克斯台球 | [上游](https://atomgit.com/u-uu/ns-billiard) | [fork](https://gitcode.com/dora-minigame-2026/u-uu-ns-billiard) | `0c5f6f01960d5819597238df4bc73c03642fccf9` | `ns-billiard-web-html.zip` |
| 火车RUN | [上游](https://atomgit.com/EthanFU/TrainRun) | [fork](https://gitcode.com/dora-minigame-2026/EthanFU-TrainRun) | `d063848ea0788cc0b1db3b2dc688c6249fa205c4` | `TrainRun-web.zip` |
| 奇怪的贪吃蛇 | [上游](https://atomgit.com/starwishxnyx/strange-snake) | [fork](https://gitcode.com/dora-minigame-2026/starwishxnyx-strange-snake) | `4614b3aca4a3918d55fa7bd0e198b6d9e8abd239` | `Strange Snake-web-html.zip` |
| 云际巡航 | [上游](https://atomgit.com/starwishxnyx/cloud-cruise) | [fork](https://gitcode.com/dora-minigame-2026/starwishxnyx-cloud-cruise) | `a2a3bdadcacd8bdb5eb4dc2455a2757a49495daf` | `云际巡航-H5.zip` |
| 点墨 | [上游](https://atomgit.com/mtdw/dianmo-dora) | [fork](https://gitcode.com/dora-minigame-2026/mtdw-dianmo-dora) | `3597d893082b7d8c163fcf0a924ef575fd7eb00b` | `dianmo-web-html.zip` |

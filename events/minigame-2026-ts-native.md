# 仅 TypeScript 作品的原生构建验证

日期：2026-10-02（Asia/Shanghai）。使用本地 Dora SSR 1.9.3.11、官方 TypeScript API 和引擎 Web IDE 编译服务生成 Lua。全部 10 个作品以 init.lua 在真实本地引擎启动，0.5 秒及 3 秒截图均正常显示游戏界面。9 个作品自带的规则测试在引擎 Lua 环境全部通过。

坦克大战原仓库缺少 Audio/TankAudio、UI/AudioSettings、Music/TankBgm 等依赖；从作者原始 Tank Duel.zip 内的 html-assets 取回其 TypeScript 模块及音频，并验证内嵌 SHA-256。保留 init.ts 原文，补齐 Audio、Music、UI 后重新编译通过。源码包不再被整体放回仓库。

提交包含生成 Lua 和必要的作者依赖，不包含本地 API 安装目录、tsconfig、.agent 截图或编译缓存。各仓库提交已推送并核对远程默认分支。Catalog 将这 10 个条目设为 runnable: true、entrypoints: init；原始在线试玩链接保留。全部 180 个条目通过 schema，真实 Catalog.lua 筛选到 108 个原生 feed 条目（活动作品 106 个）。

验证范围：编译、原生启动画面和作者规则测试；未逐个通关、执行全流程交互测试或真机测试。已安装的旧工作树需要自行 Git pull 或重新安装，Catalog 更新本身不会改动用户项目。

| 作品 | 分发仓库提交 | 生成 Lua 数 | 作者规则测试 |
| --- | --- | --- | --- |
| 摇落 | [6db4a3aa](https://gitcode.com/dora-minigame-2026/2401_88209890-Yaolou/commit/6db4a3aacbf476e34f9b978ca6f8d6c8de0cf092) | 18 | === RULE CHECKS BEGIN ===<br>passed — 67 passed, 0 failed<br>=== RULE CHECKS END === |
| TANK DUEL | [b4efef15](https://gitcode.com/dora-minigame-2026/Uyv12-D/commit/b4efef150f2f7381e176830d40292cd4de1feb89) | 6 | 未提供独立测试入口；启动画面验证通过 |
| 愤怒的小鸟：飞天猪的逆袭 | [f24e89f5](https://gitcode.com/dora-minigame-2026/code_2007-Angry_Birds_Pig_Revolt/commit/f24e89f5a4de150da775e4eb9cbbaa80968caac7) | 10 | passed 88 checks<br>ANGRY_BIRD_TESTS_PASSED |
| 彩块跃迁 | [ddee426b](https://gitcode.com/dora-minigame-2026/code_2007-dora-BlockLeap/commit/ddee426b128ec051861110fd2fbc4ea354e5f88d) | 10 | passed 112 checks<br>COLOR_LEAP_TESTS_PASSED |
| 推箱的蛇 | [aecd1e24](https://gitcode.com/dora-minigame-2026/code_2007-dora-BoxSnake/commit/aecd1e24bc6719c833857d08feafab700be7f5cc) | 11 | passed 79 checks<br>PUZZLE_SNAKE_TESTS_PASSED |
| 水果忍者：但你是忍者 | [89cc13fe](https://gitcode.com/dora-minigame-2026/code_2007-dora-FruitNinja/commit/89cc13fee3ab854874020fa2766403a2e75cc076) | 11 | [test] 配置表<br>[test] 忍者物理<br>[test] 蓄力冲刺斩击<br>[test] 水果行为<br>[test] 连击与计分<br>[test] 三分钟倒计时<br>[test] 教学模式<br>[test] 手机端技能脚本<br>[test] 压测<br>passed 215 checks<br>SANDBOX_TESTS_PASSED<br>ui checks: 52, failed: 0<br>SANDBOX_UI_PASSED |
| 重力爆破 | [2687e0d3](https://gitcode.com/dora-minigame-2026/code_2007-dora-GravityBlast/commit/2687e0d33016fc59ecb4f2872d7cd1cbf455e8c7) | 10 | passed 63 checks<br>GRAVITY_BLAST_TESTS_PASSED |
| 掘地爆破 | [2dba82c7](https://gitcode.com/dora-minigame-2026/code_2007-dora-Mineblast/commit/2dba82c7acabbcf85ef237e447016f05b6ba8ac3) | 10 | passed 115 checks<br>MINEBLAST_TESTS_PASSED |
| 裂隙突围 | [9a87a310](https://gitcode.com/dora-minigame-2026/code_2007-dora-RiftBreaker/commit/9a87a31035e5c3f293f8137e82f3d2d2347ed334) | 11 | passed 11165 checks<br>RIFT_TESTS_PASSED |
| 围城 | [17f6e755](https://gitcode.com/dora-minigame-2026/code_2007-dora-siege/commit/17f6e755f55429ca9868f51fd2bb94a23a234936) | 9 | passed 21 checks<br>SIEGE_TESTS_PASSED |

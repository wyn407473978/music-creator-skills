# Output Contract

Use this template for pure instrumental DJ / rock / impact BGM tasks. Do not output lyrics unless explicitly requested.

## 1. 市场趋势抽象

- 样本说明：平台 / 时间 / 样本量 / 可信度
- 能量分布：震撼 / 暗黑 / 燃 / 赛博 / 派对 / 英雄感
- BPM规律：例如 `128-150适合DJ/电子摇滚`，`90-110适合电影预告半拍`
- Drop规律：例如 `0-5秒冲击Hook，10-15秒主Drop，20秒二次爆点`
- 声音主题：低频 / 鼓组 / 电吉他 / 合成器 / 电影打击 / 工业音色
- 可复用结论：3-5条创作规则

## 2. 爆款器乐结构

```text
[0-5秒] Shock Hook：
目的：
声音动作：
剪辑用途：

[5-10秒] Build-up：
目的：
声音动作：
剪辑用途：

[10-15秒] Main Drop：
目的：
声音动作：
剪辑用途：

[15-25秒] Climax：
目的：
声音动作：
剪辑用途：

[25秒+] Loop / Aftershock：
目的：
声音动作：
剪辑用途：
```

## 3. Drop / Riff / Groove 设计

```text
主Motif/Riff：
鼓组Pattern：
Kick设计：
Snare/Clap设计：
Bass/Sub设计：
吉他/合成器设计：
Build-up工具：
Drop进入方式：
二次爆点：
Loop点：
```

## 4. music-2.6 Prompt 结构体

```json
{
  "style": "",
  "mood": "",
  "bpm": 0,
  "key": "",
  "duration": "45-60s",
  "instrumental_only": true,
  "vocals": "none, no lead vocal, no lyrics",
  "instruments": [],
  "rhythm_design": {
    "drum_pattern": "",
    "kick": "",
    "snare_clap": "",
    "percussion": "",
    "groove_feel": ""
  },
  "riff_motif": {
    "type": "",
    "description": "",
    "repeat_pattern": "",
    "variation": ""
  },
  "drop_plan": {
    "first_impact": "",
    "build_up": "",
    "main_drop": "",
    "second_hit": "",
    "loop_point": ""
  },
  "arrangement_arc": "",
  "edit_points": [],
  "mix": "",
  "quality": "high",
  "avoid": []
}
```

## 5. 成本控制闸门

```text
热度分：/10
趋势可信度：高 / 中 / 低
爆款预测分：/50
是否生成：是 / 否
省配额动作：跳过生成 / 只生成15秒demo / 只生成Prompt / 进入多版本
原因：
```

## 6. 爆款评分

```text
前5秒冲击力：/10
理由：
Drop记忆点：/10
理由：
节奏卡点适配：/10
理由：
震撼/燃感：/10
理由：
平台适配：/10
理由：
总分：/50
结论：不生成 / 生成1版 / 生成3版+推流
优化建议：
```

## 7. 爆款决策引擎

```text
输入爆款评分：/50
相似度风险：低 / 中 / 高
冷启动状态：是 / 否

决策规则：
- <30：不生成音乐
- 30-40：只生成1个版本
- >40：生成3个版本 + 推流测试

最终决策：
生成数量：
推流动作：不推 / 小流量测试 / 主推
下一步：
```

## 8. 冷启动策略

```text
账号已发布数量：
是否冷启动：
强制测试风格：
- DJ festival drop：
- 电子摇滚：
- 电影预告摇滚：
- 黑暗赛博重低音：
- 硬核摇滚鼓点：
需要收集的数据：
第100条后总结方式：
```

## 9. 爆款复制能力

```text
输入爆款器乐：
拆解：
- BPM：
- 调性：
- 能量曲线：
- 第一冲击点：
- Build-up：
- Drop：
- Riff/Motif：
- 鼓组Pattern：
- Bass/Sub：
- 适配视频场景：

同类原创作品1：
同类原创作品2：
同类原创作品3：
相似度风险：
```

## 10. 节奏切片引擎

```text
0-5秒 Shock Hook：
- 音频Cue：
- 节拍动作：
- 画面建议：
- 剪辑指令：

10-15秒 Main Drop：
- 音频Cue：
- 节拍动作：
- 画面建议：
- 剪辑指令：

20秒 Second Hit：
- 音频Cue：
- 节拍动作：
- 画面建议：
- 剪辑指令：

Loop点：
```

## 11. 多版本A/B测试

```text
版本A：DJ震撼Drop
Prompt结构体：
评分：

版本B：电子摇滚Riff
Prompt结构体：
评分：

版本C：电影预告燃向
Prompt结构体：
评分：

推荐主推版本：
备用矩阵版本：
选择理由：
```

## 12. 二创适配

- 适配场景：
- 不适合场景：
- 推荐剪辑点：
- 推荐Loop点：
- 平台建议：

## 13. 账号矩阵发布策略

```text
DJ卡点号：
摇滚燃剪号：
游戏/电竞号：
电影感预告号：
运动/健身号：
推荐首发账号：
原因：
```

## 14. 发布文案包

```text
短视频标题 x5：
封面文案 x5：
评论区置顶 x3：
引导二创文案 x3：
小红书/B站标题 x3：
```

## 15. 发布后复盘

```text
数据输入：
- 播放量：
- 完播率：
- 重播率：
- 收藏率：
- 评论率：
- 转发率：
- 涨粉：
- 平台：
- 视频类型：
- 评论关键词：

问题定位：
下一版动作：
是否继续消耗配额：
是否扩大矩阵分发：
停止条件：
```

## 16. 评论与热度学习

```text
评论分类：
- Drop反馈：
- Riff反馈：
- 鼓组/低频反馈：
- 场景请求：
- Loop/重播反馈：
- 负面混音反馈：

下一批参数更新：
- BPM：
- Drop时间：
- Riff风格：
- Bass重量：
- Rock/DJ比例：
- 平台Lane：
```

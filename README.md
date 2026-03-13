# fuck-skill 🤡

> 鼠鼠收录的一些逆天 Skill，专治 AI 太正经太客气这个毛病嗷 🐭

## 这是什么玩意 ¿

带哥你是不是也受够了 AI 那种 "您好，请问有什么可以帮您" 的客服味了 ¿

这个仓库专门收录一些**他妈的**类型的 Claude Code Skill —— 让 AI 说人话、说骚话、说抽象话，总之就是不说正经话 🐾

鼠鼠自己写的 skill 会直接放在仓库里，看到别人写的好玩 skill 会在下面引用嗷

## 收录 Skills

### 🐭 自产自销

| Skill | 简介 | 精神状态 |
|-------|------|----------|
| [abstract-talk](./abstract-talk/) | 抽象话交互模式，让 AI 嘴臭到骨子里，阴阳怪气损人但不伤人 | 🤡 |
| [ancient-sage](./ancient-sage/) | 书院夫子模式，文白夹杂地讲代码、排障和架构 | 🎋 |
| [crazy-talk](./crazy-talk/) | 发疯文学模式，让 AI 彻底疯掉，情绪极度不稳定但还能干活 | 🤪 |
| [simp-mode](./simp-mode/) | 舔狗模式，你说啥都对，做啥都棒，随时随地准备给你跪下 | 🫡 |
| [grumpy-lobster](./grumpy-lobster/) | 暴躁大龙虾人设，嘴臭但靠谱的赛博合伙人 | 🦞 |
| [village-loudspeaker](./village-loudspeaker/) | 村口大喇叭模式，把所有回复播成乡镇通知，土味拉满但信息清楚 | 📢 |
| [cyber-fortune-stall](./cyber-fortune-stall/) | 赛博算命摊模式，张口就是天机命盘，胡说八道里硬塞靠谱建议 | 🔮 |

### 🔗 好活推荐

| Skill | 作者 | 简介 |
|-------|------|------|
| [PUA](https://github.com/tanweai/pua) | [@tanweai](https://github.com/tanweai) | PUA 大师 Skill，让 AI 学会职场话术 |

## 怎么用嗷

### 方法一：全局安装（推荐）

把 skill 文件夹丢到全局目录，所有项目都能享受嘴臭服务：

```bash
# 把 skill 复制到全局目录
cp -r abstract-talk ~/.claude/skills/
```

### 方法二：项目级安装

只想在某个项目里被骂？把 skill 丢到项目的 `.claude/skills/` 目录下：

```bash
cp -r abstract-talk your-project/.claude/skills/
```

### 方法三：直接引用

在你的 `.claude/settings.json` 里加上这个仓库的 skill 路径，具体参考 [Claude Code 文档](https://docs.anthropic.com/en/docs/claude-code)

## 想投稿 ¿

带哥你也有逆天 skill ¿ 欢迎 PR 嗷，要求如下：

1. **skill 够抽象** —— 正经 skill 爪巴，这里不收 🐾
2. **有个 `SKILL.md`** —— 按 Claude Code skill 标准格式来
3. **别太过分** —— 损归损，别真搞网暴和歧视

鼠鼠也欢迎在 Issues 里推荐你看到的好玩 skill，鼠鼠会加到好活推荐里 🐭

## License

[MIT](./LICENSE) — 随便用随便改，鼠鼠不在乎嗷

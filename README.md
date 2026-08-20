# 山河导演（shanhe-director）

AI 视频前期全流程创作技能。输入一个或几个需求，先确立影片整体风格，再依次产出：

1. **创意编剧**：专业剧本，结构、视听写作、台词潜台词均符合影视规范；
2. **分镜脚本**：自然流畅、运镜有动机、画面描述不矛盾；
3. **美术资产整合**：整理每一段用到的场景、道具、角色、服饰、特效等 AI 美术资源；
4. **中文图片提示词**：面向 gpt-image-2（image2），覆盖全部美术资产与关键帧；
5. **中文视频提示词**：面向可灵 / Vidu / 即梦等平台的通用视频提示词；
6. **统一影片风格**：所有提示词都继承同一份风格卡（画面、道具、角色、视频）；
7. **山河导演意见**：每个生成模块开始前都会先输出导演判断。

> 适用于 15 秒–10 分钟的广告宣传片、故事片、创意片、自媒体内容、文艺短片、科幻短片等 AI 视频前期创作。默认只输出提示词，不实际生成图片或视频。

## 安装

### 方式一：在 Codex 中直接说

```text
从 GitHub 安装 <你的账号>/shanhe-director 的 shanhe-director 技能
```

安装后，技能会在下一轮对话可用。

### 方式二：使用 skill-installer 脚本

```bash
python scripts/install-skill-from-github.py --repo <你的账号>/shanhe-director --path shanhe-director
```

`<你的账号>` 请替换为实际 GitHub 用户名或组织名。

## 使用示例

```text
用山河导演帮我写一支 15 秒国潮护肤广告。
```

```text
我想拍一个 3 分钟科幻概念短片，主题是“记忆可以交易”。
```

```text
为一个自媒体的 5 分钟城市夜行故事做前期创作。
```

技能会先追问缺失信息，然后分步输出；每步完成后等待你回复「通过 / 修改 / 自检 / 继续」。如果你想一次拿全案，直接说“一键出全套”。

## 目录结构

```text
shanhe-director/
├─ SKILL.md
├─ agents/openai.yaml
└─ references/
   ├─ methodology-screenwriting.md
   ├─ format-ad.md
   ├─ format-concept-short.md
   ├─ format-narrative-short.md
   ├─ genre-guide.md
   ├─ storyboard.md
   ├─ asset-integration.md
   └─ prompt-engineering.md
```

## 署名与许可证

- 本仓库采用 MIT License。
- 编剧方法论参考并致谢 [@山音《山音超级编剧大师》](https://github.com/Shanyin-ai/shanyin-screenwriting-master)（MIT License）。
- 本技能文本为原创整理，仅借鉴方法论框架，未原文复制原 `.skill` 文件。

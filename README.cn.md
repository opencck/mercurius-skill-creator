[English](README.md) | [Русский](README.ru.md) | **中文**

# mercurius-skill-creator

[Mercurius](https://github.com/opencck/mercurius) 的内置技能：智能体如何创建和改进自己的技能。它从对话中捕捉意图，只询问缺少的信息，编写一份简短的 SKILL.md 并把细节放进附属文件，通过 `delegate_task` 用 2–3 个真实请求在有技能和无技能两种情况下检验草稿，调整描述使技能在该触发的地方触发，并用 `skill_save` 把它保存到参与者或项目的文件夹中。

技能文本是俄语，即智能体的默认语言。

## 内容

| 文件 | 说明 |
|------|------------|
| `SKILL.md` | 何时创建技能、工作顺序、如何编写 |
| `references/anatomy.md` | `skill_save` 的字段、限制、渐进式披露、骨架 |
| `references/testing.md` | 在有技能和无技能的请求上检验草稿 |
| `references/description.md` | 编写描述并检查其何时触发 |

## 使用

Mercurius 把它作为子模块加载在 `skills/skill-creator`；内置技能在启动时读取，处处可用；参与者或项目文件夹中的修改副本按名称优先生效。

```sh
git submodule update --init --depth 1 skills/skill-creator
```

基于 Anthropic 的 Claude 插件中 `skill-creator` 技能的理念（意图、访谈、有无技能的测试、描述调优）以及 hermes-agent 的技能编写规则，并针对 Mercurius 的工具和文件夹做了调整。

## 许可证

[MIT](LICENSE)

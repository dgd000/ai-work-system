# 搭建执行指南

## 第一步：运行初始化脚本（5 分钟）

```bash
chmod +x init-work-system.sh
./init-work-system.sh
```

脚本会交互式询问你的信息（名字、业务描述、技术栈、项目列表），然后自动生成完整的目录结构和所有模板文件。

## 第二步：填写核心信息（20 分钟）

```bash
cd ~/Documents/projects/work-system   # 或你指定的路径
```

按优先级编辑以下文件：

| 文件 | 要做什么 | 耗时 |
|------|----------|------|
| `CLAUDE.md` | 补充业务全貌、GitHub URL | 5 min |
| `控制面板.md` | 填入各项目真实状态和数据 | 5 min |
| `个人定位.md` | 写下你的目标和战略方向 | 5 min |
| `00-全局资源/技术栈.md` | 确认技术选型细节 | 5 min |

其余文件里的 `[TODO]` 不急，后续使用中逐步填充。

## 第三步：推送到 GitHub（2 分钟）

```bash
# 在 GitHub 创建 work-system 仓库（建议 Private）
cd ~/Documents/projects/work-system
git remote add origin git@github.com:[你的用户名]/work-system.git
git push -u origin main
```

## 第四步：为已有项目添加 CLAUDE.md（每个项目 10 分钟）

```bash
# 复制模板到项目仓库
cp ~/Documents/projects/work-system/01-项目模板/CLAUDE.md ~/Documents/projects/your-project/CLAUDE.md
cp -r ~/Documents/projects/work-system/01-项目模板/docs ~/Documents/projects/your-project/docs

# 编辑填入项目真实信息
cd ~/Documents/projects/your-project
# 编辑 CLAUDE.md 和 docs/

# 提交
git add CLAUDE.md docs/
git commit -m "docs: 添加 CLAUDE.md 和项目文档"
git push
```

先做正在活跃开发的项目，规划中的项目可以后面再加。

## 第五步：开始使用

**做项目开发**
```bash
cd ~/Documents/projects/your-project
# Claude Code 自动读取 CLAUDE.md，知道项目上下文
```

**做战略运营**
```bash
cd ~/Documents/projects/work-system
# Claude Code 读取全局 CLAUDE.md，知道你的全部业务
```

---

## 注意事项

1. **不要追求一次填满所有文件** — 先搭骨架，在实际工作中逐步填充
2. **CLAUDE.md 要保持更新** — 特别是"当前优先事项"和"当前状态"
3. **控制面板每周更新一次** — 5-10 分钟即可
4. **技能库靠积累** — 每次踩坑或发现好做法时记一条

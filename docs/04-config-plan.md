# 配置管理方案 — 校园活动报名与签到管理系统

## 一、配置项清单

| 配置项 | 文件路径 | 负责人 |
|--------|----------|--------|
| 项目说明 | README.md | yangyuxuan |
| 项目概况 | docs/01-project-charter.md | yangyuxuan |
| WBS文档 | docs/02-wbs.md | liming |
| 进度计划 | docs/03-schedule.md | liming |
| 配置管理文档 | docs/04-config-plan.md | chenwei |
| 总结报告 | docs/05-summary-report.md | 全体成员 |
| 冲突练习文件 | docs/conflict.md | chenwei, liming |

## 二、分支策略

```
main
 └── dev
      ├── feature/wbs        （liming负责）
      ├── feature/config     （chenwei负责）
      └── feature/summary    （yangyuxuan负责）
```

| 分支 | 用途 | 保护规则 |
|------|------|----------|
| main | 最终成果，只接受来自dev的合并 | 不允许直接push |
| dev | 集成分支，各feature合并至此 | 合并前需解决冲突 |
| feature/* | 各成员独立开发分支 | 完成后合并至dev |

## 三、提交规范

- 提交人名称统一使用本人姓名拼音全称
- 提交信息格式：`类型: 简要描述`
  - `feat:` 新增文档或内容
  - `docs:` 更新已有文档
  - `fix:` 修正错误
  - `merge:` 分支合并

## 四、合并规则

1. feature分支完成后，由负责人发起合并请求至dev
2. 合并前必须在本地解决所有冲突
3. dev分支稳定后，由项目经理合并至main
4. 所有合并操作需保留完整提交记录，不使用`--squash`

## 五、版本标记

| 标记 | 含义 | 时机 |
|------|------|------|
| v0.1 | 仓库初始化完成 | A1完成后 |
| v0.2 | 计划文档完成 | A4完成后 |
| v1.0 | 实验最终成果 | A9完成后 |

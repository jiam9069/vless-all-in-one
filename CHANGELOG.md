# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).
## [3.4.1] - 2026-03-03

## [3.3.0] - 2026-01-18

### Added
- 新增 SOCKS5 无认证模式支持
- 新增多端口实例功能与首页显示优化

### Fixed
- 修复 SOCKS5 配置显示中的乱码问题
- 修复全新机器安装 SOCKS5 失败的问题
- 修复数据库函数 JSON 格式问题
- 修复 SOCKS5 和 VMess-WS 协议的 Xray 安装调用
- 移除 SOCKS5 配置中的错误 ip 字段

### Changed
- SOCKS5 无认证模式根据双栈支持智能选择默认监听地址

## [3.2.2] - 2026-01-16

### Added
- 新增 SOCKS5 服务器自定义用户名和密码支持
- 新增一键导入 Alice 家宽功能
  - 支持 Alice 节点负载均衡组管理
  - 支持 SOCKS5 负载均衡器使用 leastPing 策略
  - 集成负载均衡配置到导入流程
  - 分流规则选择出口时支持跳过延迟检测
- 新增 sing-box 负载均衡支持

### Fixed
- 修复完全卸载时未清理 Caddy 二进制文件的问题
- 修复 Alice 节点负载均衡器 SOCKS5 协议兼容性问题
- 删除重复的负载均衡函数定义
- 增强 URL 构建变量替换兼容性
- 增强卸载流程,支持清理所有版本的 Caddy (包括 NaïveProxy 自定义编译版本)

### Changed
- 重构节点延迟检测机制并优化批量测速性能
- 优化出口加载性能,减少 jq 调用次数
- 移除危险操作确认机制并优化解析逻辑

## [3.2.1] - 2026-01-15

### Changed
- 更新版本号至 v3.2.1

## [3.2.0] - 2025-XX-XX

### Added
- 完善核心版本管理与缓存
- 新增核心更新管理功能

### Fixed
- 修复 Snell v4 版本配置兼容性问题
- 优化 IPv6 双栈监听策略与系统兼容性
- 添加 ACME 账户邮箱验证功能
- 更新 acme.sh 安装邮箱配置

### Changed
- 优化分流规则菜单布局，按字母倒序排列
- 在分流规则菜单中添加新规则选项

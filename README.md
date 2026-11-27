# LovelyCarve HarmonyOS NEXT（原生鸿蒙）取证插件

插件 ID：`org.lovelycarve.harmonyos`（LPP v2）

> 本仓库仅提供面向 **LovelyCarve** 的 Release `.lcpkg` 二进制插件包发布与使用说明。

## 下载与安装（双版本对照）

| 适用主程序 | Release 版本 | 下载文件名 | 特点说明 |
| --- | --- | --- | --- |
| **官方主项目** ([LovelyTeams/LovelyCarve](https://github.com/LovelyTeams/LovelyCarve)) | [`v1.0.0`](../../releases/tag/v1.0.0) | `org.lovelycarve.harmonyos-1.0.0-windows-x64.lcpkg` | 标准 LPP v2 协议，无魔改扩展 |
| **二开增强版** ([JerryXie599/LovelyCarve](https://github.com/JerryXie599/LovelyCarve)) | [`v1.0.0-mod`](../../releases/tag/v1.0.0-mod) | `org.lovelycarve.harmonyos-1.0.0-mod-windows-x64.lcpkg` | 启用 `mod-chat` 聊天气泡视图（短信/IM）与内联密码参数 |

## 核心能力

本插件内置 **HarmonyOS NEXT 备份容器直读与双层加密解密引擎**（PBKDF2-HMAC-SHA256 + AES-256-GCM-CTR + USTAR/PAX/GNU TAR 流式切片索引 + WAL-only 自动回放）：

1. **`harmony_overview`**：`.info.json` 设备/分身清单、`1120_sa.data` Wi-Fi、蓝牙配对、密钥元数据、`settingsdata*.db`、`sim.db`。
2. **`harmony_comm`**：通话记录、已删联系人与黑名单、`sms_mms.db` + `softDeleteRdb` 软删短信恢复、抖音 IM / 畅连消息。
3. **`harmony_pim`**：备忘录、日历与已删日程、闹钟与世界时钟、图库与孤儿 AI OCR 文本残留恢复。
4. **`harmony_apps`**：文件快传与下载、文件管理器、浏览器历史、地图导航与第三方应用记录。

# Kazumi 规则集（本地副本）

本目录是 `https://github.com/ChopDream/kazumi-rules` 的本地副本，用于保存已验证规则，等待推送。

## 规则

| 规则 | 站点 | 版本 | 状态 | 文件 |
|---|---|---|---|---|
| AkiAnime | https://www.akianime.cc/ | 1.6 | 用户实测可播放 | akianime.json |
| MX动漫 | https://www.dcc3.com/ | 2.5 | 搜索/选集/HLS 播放页已实测 | mxdm.json |
| 咕咕番 | https://www.gugu3.com/ | 1.5 | 搜索/选集可用；正片需官方客户端 | gugu3.json |

## 验证依据

- AkiAnime：搜索 4 条、详情 2 线路（13/14 集），播放页 `player_aaaa` 直出 m3u8。
- MX动漫：搜索 7 条、目标作品 4 线路、首线路 13 集，播放页含 m3u8，主播放列表 `RESOLUTION=1080x608` / `BANDWIDTH=800000`。
- 咕咕番：搜索 4 条、2 线路 × 13 集；播放走站点专属播放器，需官方客户端。

## 未执行

- 未在 Kazumi 客户端逐条实测 MX动漫与咕咕番。
- 未做长时段带宽测速；`BANDWIDTH` 是播放列表声明值，不等于实际下载速度。

## 推送状态

GitHub 推送未完成：终端无法读取传入的凭证（命令中的凭证被环境屏蔽），因此远程仓库目前仍只有 AkiAnime 与咕咕番。本地文件已保存，待凭证可用时推送 `mxdm.json`、`index.json`、`README.md`。

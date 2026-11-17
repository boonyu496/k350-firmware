# K350 跟随小车固件

本仓库**只存放编译好的固件二进制**（`.bin`）和版本清单，**不含源代码**。

源代码在私有仓库维护。小车通过 HTTPS 下载固件完成远程 OTA 升级，不需要 GitHub 账号或密钥。主地址是本仓库的 `raw.githubusercontent.com` 直链；因为它在国内经常连不上，`latest.json` 还给出 jsDelivr 镜像（`mirrors`），固件 v1.4.5 起会自动在这些地址之间切换。无论从哪个地址下载，都必须通过 SHA256 校验才会写入。

## 最新版本

请查看 [`latest.json`](./latest.json)，或打开 [`firmware/`](./firmware/) 目录中对应版本的 `.bin` 文件。

`latest.json` 字段：

- `ver`：版本号
- `url`：固件直链
- `sha256`：SHA256 校验值（小写十六进制）
- `size`：字节数
- `date`：发布日期
- `mirrors`：备用下载地址（jsDelivr 镜像，固定到放入该 bin 的提交；v1.4.5 起才有）

历史版本见 [`versions.json`](./versions.json)。

## 使用方法

在 `remote_console.html` 中点击「检查最新版本」，会自动填入 URL、SHA256 和版本号，确认后即可远程升级。

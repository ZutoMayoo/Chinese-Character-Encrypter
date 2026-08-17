# Chinese-Character-Encrypter

中文加解密工具（网页版）—— 把文字加密成看起来像乱码的「伪汉字」，也可随时解密还原。

A tiny offline web tool that encrypts Chinese text into garbled-looking "pseudo-Chinese" characters, and decrypts it back.

## 使用 / Usage

1. 打开 `加解密工具.html`（单文件，完全离线可用）
2. 顶部切换 **🔒 加密 / 🔓 解密** 模式
3. 输入内容 → 点击 **加密/解密** → 复制结果

## 原理 / How it works

- 将文字编码为 UTF-8 字节
- 逐字节与固定密钥异或，并叠加位置偏移
- 每个字节映射为 `0x4E00` 起连续 256 个汉字，密文看起来像乱码
- 解密为以上过程的逆运算

> ⚠️ 可逆混淆（不含密码），仅用于轻度保密 / 趣味用途，请勿传输重要机密信息。
> This is reversible obfuscation (no password). Not for real secrets.

## 文件 / Files

| 文件 | 说明 |
|------|------|
| `加解密工具.html` | 加密 + 解密二合一页面 |
| `使用说明.txt` | 详细使用说明 |

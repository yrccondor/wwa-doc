# 常见问题

## 下载

> 我可以从哪里获取 WP-WebAuthn？

你可以在 WordPress 后台搜索 "wp-webauthn" 并安装，或是从 [WordPress 插件目录](https://wordpress.org/plugins/wp-webauthn/)下载安装。

WP-WebAuthn 的源代码开源于 [Github](https://github.com/yrccondor/wp-webauthn)，你也可以帮助我们改进 WP-WebAuthn。

## 使用

> 我没有购买 Yubikey 等单独的认证器，我能使用 WebAuthn 吗？

能！WebAuthn 可用的认证器不只是 USB Key。在 Windows 上，你可以使用 Windows Hello 调起面部识别、指纹识别或是输入 PIN 来进行认证；在 Android 上，你可以通过指纹识别、虹膜扫描或是输入锁屏密码来进行认证；在 MacOS 上，你可以通过扫描指纹来进行认证。

在这种情况下，替代密码的其实是你的设备，不必担心安全问题。

> WP-WebAuthn 看起来没有正常工作，我该怎么办？

WebAuthn 需要安全上下文才能正常被调起，也就是说，你的站点需要使用 HTTPS，或是处于 `localhost` 中。

此外，WP-WebAuthn 还需要 gmp 和 mbstring 两个 PHP 扩展。这两个扩展没有被默认安装，你需要自行检查。

如果你仍然碰到问题，可以前往我们的 [Github 仓库](https://github.com/yrccondor/wp-webauthn)提出 [issue](https://github.com/yrccondor/wp-webauthn/issues)，**并附上能够复现问题的插件日志。**

> 用户认证是什么？我该启用吗？

如果启用用户认证，插件将会要求认证器验证“用户为本人”而不只是“用户在场”。验证方法视平台与认证器的不同可能会不同，常见的方式有输入 PIN、输入密码等。由于许多设备并不支持用户验证且用户验证的方式不一，用户验证只能在部分情况下提高验证的安全性。

如果你对登录安全没有较高要求，可以禁用用户验证。

> 无用户名认证的原理是什么？我能启用吗？

如果启用无用户名认证，在注册认证器时，认证器将会存储用户 ID 并将其与登录凭证绑定。登录时，不必输入用户名，WP-WebAuthn 会通过认证器发送的用户 ID 查找用户并验证登录凭证。这一过程是安全的。

由于在此过程中认证器会将用户 ID 等信息永久存储于内置存储中，因此单个认证器能注册的无用户名登录凭证的数量是有限的。对于 Yubikey，这通常是 25 个。不过，你可以通过重置认证器来清空认证器存储的凭证。

只有当你认为有必要使用无用户名登录功能时，才应注册启用了无用户名登录的认证器。

## 开发

> 我可以修改/二次分发 WP-WebAuthn 吗？

可以，WP-WebAuthn 使用 GPL-3.0 协议开源，你可以随意修改插件，但必须遵守 GPL-3.0 协议。

如果你觉得你的修改对其他人也很有帮助，请向我们提交 [Pull Request](https://github.com/yrccondor/wp-webauthn/pulls)。

## 其他问题

> 使用中遇到问题，我该怎么办？

在我们的 [Github 仓库](https://github.com/yrccondor/wp-webauthn)查找或提出 [issue](https://github.com/yrccondor/wp-webauthn/issues)。如果你打算提出一个 issue，**请务必附上能够复现问题的插件日志。**

> 如何正确地提问？

请参阅 [提问的智慧](https://github.com/ryanhanwu/How-To-Ask-Questions-The-Smart-Way/blob/master/README-zh_CN.md)。

> 我觉得 WP-WebAuthn 不好用、很垃圾怎么办？

哦。
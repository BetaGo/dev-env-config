# haskell 配置

## window 环境

### [下载并安装 haskell](https://www.haskell.org/platform/windows.html)

### [下载并安装 Stack](https://docs.haskellstack.org/en/stable/install_and_upgrade/#windows)

安装完后建议配置下代理，设置 `windows` 的环境变量 `http_proxy` 和 `https_proxy`为合适的代理地址;

### [安装 HIE(haskell-ide-engine)](https://www.vacationlabs.com/haskell/environment-setup.html)

```sh
git clone https://github.com/haskell/haskell-ide-engine
cd haskell-ide-engine
stack install
```

假如安装时报错 `terminateProcess: permission denied (Permission denied)`,详见[#5014](https://github.com/commercialhaskell/stack/issues/5014);

可以尝试修改 终端的字符编码为·`utf-8`;

方法:

- 1.右键开始菜单 -> 运行 -> 输入`regedit` -> 回车
- 2.在注册表中找到 `[HKEY_LOCAL_MACHINE\Software\Microsoft\Command Processor\Autorun]`
- 3.修改值为 `chcp 65001`

如果注册表里没有这个值，可以自行新建一个

最后在 `CMD` 里重新执行 `stack install`

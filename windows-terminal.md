# window terminal 配置

## 右键菜单添加 Windows terminal here

```reg
Windows Registry Editor Version 5.00

[HKEY_CLASSES_ROOT\Directory\Background\shell\wt]
@="Windows terminal here"
"Icon"="%USERPROFILE%\\AppData\\Local\\terminal\\wt_32.ico"

[HKEY_CLASSES_ROOT\Directory\Background\shell\wt\command]
@="C:\\Users\\<username>\\AppData\\Local\\Microsoft\\WindowsApps\\wt.exe"
```
将上面代码另存为 `wt.reg` 然后双击执行.
**注意** 要先替换 `<username>` 为 Windows 系统当前登录的用户名;

## 添加 ss 登录

示例:
```json
{
  "guid": "{1e19dc92-c511-11ea-87d0-0242ac130003}",
  "name": "ssh",
  "tabTitle": "ssh",
  "commandline": "ssh -i <ssh_key> <user>@<address>",
}
```

## 指定 wsl 默认目录

示例: 打开 wsl时, 默认进入用户根目录(`~`)

```json
{
  // 其他配置
  "commandline": "wsl.exe ~ -d Ubuntu-20.04",
}
```

## Anaconda 与 powershell 配置

示例:

```json
{
  "guid": "{a6a21ab4-bf67-40a3-bdb9-046f2f69e725}",
  "tabTitle": "Anaconda3",
  "commandline": "pwsh.exe -ExecutionPolicy ByPass -NoExit -Command \"& '%USERPROFILE%\\anaconda3\\shell\\condabin\\conda-hook.ps1' ;conda activate '%USERPROFILE%\\Anaconda3' ",
  "icon": "%USERPROFILE%/Anaconda3/Menu/anaconda-navigator.ico",
  "name": "Anaconda3",
  "startingDirectory": "%USERPROFILE%"
}
```
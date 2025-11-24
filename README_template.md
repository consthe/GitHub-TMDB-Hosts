# GitHub-TMDB-Hosts

<p align="center">
😘 解决 GitHub 访问慢、图片加载失败问题<br>
🎬 解决 TMDB、IMDb、TheTVDB 等影视数据库访问问题
</p>

> 本项目基于 [GitHub520](https://github.com/521xueweihan/GitHub520)，添加了 TMDB/IMDb 相关域名支持

## 📝 介绍

**本项目无需安装任何程序，仅需 5 分钟。**

通过修改本地 hosts 文件，解决：

### GitHub 相关
- ✅ GitHub 访问速度慢
- ✅ GitHub 图片加载失败

### 影视刮削相关  
- ✅ TMDB (The Movie Database) 访问问题
- ✅ IMDb (Internet Movie Database) 访问问题
- ✅ TheTVDB 访问问题

**适用工具**: TinyMediaManager、Plex、Emby、Jellyfin、Kodi、群晖 Video Station、Infuse、nPlayer 等

## 🚀 使用方法

### 方式一：手动复制（最简单）

#### 1. 复制下面的内容

```bash
{hosts_str}
```

该内容会自动定时更新，数据更新时间：{update_time}

#### 2. 修改 hosts 文件

hosts 文件在每个系统的位置：

- Windows: `C:\Windows\System32\drivers\etc\hosts`
- Linux: `/etc/hosts`
- macOS: `/etc/hosts`
- Android: `/system/etc/hosts`
- iOS: `/etc/hosts`

修改方法：

1. Windows 使用记事本（需要管理员权限）
2. Linux/Mac 使用 Root 权限：`sudo vi /etc/hosts`
3. 将上面的内容复制到文件末尾

#### 3. 刷新 DNS 缓存

```bash
# Windows
ipconfig /flushdns

# macOS
sudo killall -HUP mDNSResponder

# Linux
sudo systemctl restart systemd-resolved
```

### 方式二：SwitchHosts（推荐，自动更新）

**推荐使用 [SwitchHosts](https://github.com/oldj/SwitchHosts) 工具管理 hosts**

配置如下：

- **类型**: Remote（远程）
- **标题**: GitHub-TMDB-Hosts
- **URL**: `https://raw.githubusercontent.com/hizml/GitHub-TMDB-Hosts/main/hosts`
- **自动刷新**: 1 小时

配置后启用规则即可，每次 hosts 有更新都会自动同步。

### 方式三：命令行（一键更新）

#### macOS/Linux
```bash
curl https://raw.githubusercontent.com/hizml/GitHub-TMDB-Hosts/main/hosts | sudo tee -a /etc/hosts
```

#### Windows (Git Bash)
```bash
curl https://raw.githubusercontent.com/hizml/GitHub-TMDB-Hosts/main/hosts >> /c/Windows/System32/drivers/etc/hosts
```

## 📦 支持的域名

### GitHub 域名 (38 个)
github.com, api.github.com, raw.githubusercontent.com, avatars.githubusercontent.com 等

### TMDB 域名 (9 个)
tmdb.org, api.tmdb.org, themoviedb.org, www.themoviedb.org, image.tmdb.org 等

### IMDb 域名 (10 个)
imdb.com, www.imdb.com, ia.media-imdb.com 等

### TheTVDB 域名 (2 个)
thetvdb.com, api.thetvdb.com

**总计：59 个域名** - 详见 [TMDB_ADDED.md](./TMDB_ADDED.md)

## 🔄 自动更新

本项目配置了 GitHub Actions，每 2 小时自动运行一次：
- 自动测试并选择最快的 IP
- 自动提交更新
- 无需手动操作

## 📖 相关文档

- [快速开始指南](./快速开始.md) - 详细使用说明
- [TMDB 域名说明](./TMDB_ADDED.md) - 添加的域名列表

## 🙏 致谢

感谢 [@521xueweihan](https://github.com/521xueweihan) 创建的优秀项目 [GitHub520](https://github.com/521xueweihan/GitHub520)

## 📄 许可证

<a rel="license" href="https://creativecommons.org/licenses/by-nc-nd/4.0/deed.zh"><img alt="知识共享许可协议" style="border-width: 0" src="https://licensebuttons.net/l/by-nc-nd/4.0/88x31.png"></a><br>本作品采用 <a rel="license" href="https://creativecommons.org/licenses/by-nc-nd/4.0/deed.zh">署名-非商业性使用-禁止演绎 4.0 国际</a> 进行许可。

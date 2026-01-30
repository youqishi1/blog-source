---
title: VPS代码合集
cover: https://img.090227.xyz/file/ae62475a131f3734a201c.png
swiper_index: 10
top_group_index: 10
background: '#fff'
date: 2024-08-08 17:39:45
updated:
tags:
categories:
keywords:
description:
top: 1
top_img:
comments:
toc:
toc_number:
toc_style_simple:
copyright:
copyright_author:
copyright_author_href:
copyright_url:
copyright_info:
mathjax:
katex:
aplayer:
highlight_shrink:
aside:
ai:
---

# 单协议 hy2 serv00专用
``` bash
curl -s https://raw.githubusercontent.com/eooce/scripts/master/containers-shell/00-hy2.sh | PORT=55562 UUID=c1b9ba1f-a47e-4568-a8dd-ffad3a23d23c bash
```
# 单协议 Tuic serv00专用
``` bash
curl -s https://eooce.2go.us.kg/tu.sh | UUID=248d5250-f57b-47ff-9b42-54120bd2e2ec PORT=55563 NEZHA_SERVER=www.bing.com NEZHA_PORT=5555 NEZHA_KEY=xiaowang bash
```

# 4和1协议 sy2+vm+Tuic serv00专用
``` bash
bash <(curl -Ls https://raw.githubusercontent.com/youqishi1/Sing-box/main/sb_serv00.sh)
```

## 要设置定时重启并运行这个脚本，你可以使用 cron 来实现。cron 是一个 Linux 的定时任务调度器，可以在指定的时间间隔内执行任务。下面是如何设置定时任务来重启脚本的方法：
---

## 使用 `cron` 设置定时任务来重启并运行脚本

## 1. 编辑 `crontab`
使用以下命令打开 `crontab` 文件：

``` bash
crontab -e
```

## 2. 添加定时任务
根据你想要的重启频率，添加以下内容：

``` bash
0 3 * * * UUID=af13c17f-3c96-4850-a2a1-8b3e01582bf8 PORT=55563 NEZHA_SERVER=www.bing.com NEZHA_PORT=6666 NEZHA_KEY=xiaowang bash -c 'curl -s https://raw.githubusercontent.com/youqishi1/Sing-box/main/sb_serv00.sh | bash'
```

## 定时任务的解释：
- `0 3 * * *`: 这部分定义了任务的时间。这个示例表示每天凌晨 3:00 执行任务。
  - `0`: 表示分钟，这里是每小时的第 0 分钟。
  - `3`: 表示小时，这里是凌晨 3 点。
  - `*`: 表示日期，不指定具体日期，每天都执行。
  - `*`: 表示月份，不指定具体月份。
  - `*`: 表示星期几，不指定具体星期几。

## 3. 保存并退出
按 `Ctrl + O` 保存文件，按 `Enter` 确认，然后按 `Ctrl + X` 退出编辑器。

## 4. 验证定时任务
你可以使用以下命令查看定时任务是否设置成功：

``` bash
crontab -l
```

如果成功，服务器将在每天凌晨 3:00 自动执行你的脚本。你可以根据需要调整 `cron` 表达式中的时间设置，以满足你的特定需求。




<div class="video-container">
[up主专用，视频内嵌代码贴在这]
</div>

<style>
.video-container {
    position: relative;
    width: 100%;
    padding-top: 56.25%; /* 16:9 aspect ratio (height/width = 9/16 * 100%) */
}

.video-container iframe {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
}
</style>

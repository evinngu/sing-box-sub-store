# sing-box-sub-store 使用教程



## 感谢相关开源大佬提供原始配置，有使用问题请提 Issue

## sub-store 的使用教程自行搜索





## 目录说明

### scripts 目录包含 sub-store 用到的一些脚本

#### rename.js 脚本

用于将机场节点进行重命名，具体用法可以查看脚本注释，不想看的可以直接用我的参数：

- name=naixi       （参考值，表示机场名称前缀，可以改为自己机场的名称，自己方便辨认即可）
- out=quan

这两个参数会将节点重命名为这样的格式：naixi Hong Kong 01、naixi United States 02

#### sing-box-col.js 脚本

用于将节点放入 sing-box 的配置模板的 outbounds 当中, col 表示这个脚本是组合订阅也可以用的脚本。

- name=naixi          （参考值，表示 sub-store 的添加的订阅的订阅名称，保持与上面的 rename 脚本中提到的 name 的参数值一样最好）
- type=col                 （如果你的订阅是组合订阅，需要设置这个参数）

### templates 目录包括 sing-box 的相关配置模板

#### sing-box-1.xx-momo-tmpl.json

这是 [openwrt 代理插件momo](https://github.com/nikkinikki-org/OpenWrt-momo ) 使用的模板

#### sing-box-1.xx-tmpl.json

这是 sing-box 官方客户端使用的模板



## sing-box版本配置注意事项

## 1.12

domain_resolver 可以为outbound中的每个节点设置dns解析的server，也可以直接在 route 中设置 default_domain_resolver。
dns 的 server 不能写 detour，有默认是 direct



## sub-store搭建参考教程

https://www.youtube.com/watch?v=nEw1iadtPvs

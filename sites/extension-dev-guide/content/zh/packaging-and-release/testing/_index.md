---
title: 测试扩展组件
weight: 02
description: "将扩展组件上架到 KubeSphere 扩展市场中进行测试"
---

经过前面的章节，我们已经完成了扩展组件的开发与打包，在发布之前我们需要针对扩展组件做集成测试。

## 扩展组件上架

在扩展组件管理工程根目录（`~/workspace/kubesphere-extensions/`）执行下述命令，将扩展组件上架到 KubeSphere 扩展市场中。

```shell
ksbuilder publish employee
```

命令执行成功后，我们可以直接访问 KubeSphere 容器 30880 端口打开 ks-console 页面并登录，查看扩展市场中上架的组件，并进行安装测试。如果安装失败，您可以在 Console 上查看报错日志。

![](./kubesphere-extension-employee-1.png)

上述命令会将扩展组件上架到系统默认 kubeconfig 文件（`~/.kube/config`）所指向的集群，如果需要发布到指定的集群，可以使用 `--kubeconfig` 参数指定 kubeconfig 文件的路径：

```shell
ksbuilder publish employee --kubeconfig=/path/to/config
```

## 安装扩展组件

扩展组件安装完成后，您将可以在 KubeSphere 中使用扩展组件提供的功能。

安装扩展组件

![](./kubesphere-extension-employee-2.png)

扩展组件功能入口

![](./kubesphere-extension-employee-3.png)


![](./kubesphere-extension-employee-4.png)


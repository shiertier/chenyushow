# 端口设置与目录对比

## 端口设置

| 应用       | WebUI 端口 | Jupyter 端口 | WebOS 端口 |
|------------|------------|--------------|------------|
| **ComfyUI** | 8188       | 8888         | 7002       |
| **WebUI**   | 7860       | 8888         | 7002       |

## 挂载目录

| 目录        | 描述           | 速度  | 创作者权限 | 用户权限 | 说明                                                       |
|-------------|----------------|-------|------------|----------|------------------------------------------------------------|
| **/**         | 根目录         | 高速  | -          | -        | 根目录包含除挂载目录外的所有系统和用户文件，速度较快。通常不建议直接操作。 |
| **/chenyudata** | 平台目录       | 高速  | 不可写     | 不可写   | 仅供挂载和软链接使用，不允许直接写入新内容。如需增加新内容，请联系管理员。 |
| **/poddata /models**    | 创作者目录     | 低速  | 可写       | 不可写   | 由创作者自行管理。建议将大体积文件存放于此目录，并通过软链接方式挂载到其他位置，以防镜像过大。 |
| **/usrdata**    | 用户目录       | 低速  | 可写       | 可写     | 个人用户目录，存储在此目录中的文件会挂载到所有有该用户启动的 Pod 中。此目录的存储会计费。 |

## 镜像说明

- **镜像大小限制**: 不得超过 200GB（未来将降至 50GB）

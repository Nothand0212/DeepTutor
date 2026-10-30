# 第三方依赖

DeepTutor 的 LightRAG 引擎使用 PyPI 包 `lightrag-hku`。项目在 `pyproject.toml` 的 `rag-lightrag` 依赖组中固定支持的版本为 1.5.7。

在项目根目录为本地虚拟环境安装，并将下载缓存保存在此目录：

```bash
mkdir -p third_party/uv-cache
uv pip install --python .venv/bin/python --cache-dir third_party/uv-cache 'lightrag-hku==1.5.7'
uv pip check --python .venv/bin/python
```

运行时依赖安装在 `.venv` 中，`uv-cache` 是本地下载缓存。本机模型配置保存在被 Git 忽略的 `data/` 目录中。

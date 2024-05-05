# FalconFlask：轻量级 Python Flask 框架文档

FalconFlask 是一个基于 Python 和 Flask 的轻量级框架，旨在提供简单易用的 web 开发体验，并且具备较好的性能。它结合了 Flask 框架的灵活性和易用性，并在此基础上添加了一些额外功能，如异步查询、自动注册蓝图、中间件生命周期封装等，使开发者能够更加专注于业务逻辑的实现。

## 特性

- **异步查询支持**：FalconFlask 集成了 NoraORM，使得数据库查询可以异步执行，提升了并发处理能力和性能。
  
- **自动注册蓝图**：开发者只需编写逻辑文件，无需手动注册路由，FalconFlask 会自动将逻辑文件注册到对应的蓝图中，简化了路由管理流程。

- **中间件生命周期封装**：FalconFlask 将 Flask 的生命周期封装到中间件中，内置了丰富的中间件功能，如用户验证、请求前处理、请求中处理、请求后处理等，可根据需求自由组合使用。

- **灵活可扩展**：FalconFlask 采用模块化设计，易于扩展和定制，开发者可以根据需求灵活添加新功能或修改现有功能。

## 快速开始

1. 安装 FalconFlask：

```bash
pip install FalconFlask
```

2. 创建一个 FalconFlask 应用：

```python
from FalconFlask import FalconFlask

app = FalconFlask(__name__)
```

3. 编写逻辑文件并实现业务逻辑：

```python
# logic.py
from FalconFlask import Blueprint

bp = Blueprint('example', __name__)

@bp.route('/')
def index():
    return 'Hello, FalconFlask!'
```

4. 运行应用：

```bash
python your_app.py
```

5. 访问 http://localhost:5000/ ，即可看到 "Hello, FalconFlask!"。

## 文档

请参阅 [FalconFlask 文档](https://github.com/NeoSpecies/FalconFlask/docs) 获取更多详细信息和使用示例。

## 贡献

如果您对 FalconFlask 框架有更多建议或想贡献代码，欢迎提交 PR 或 Issue 至 [FalconFlask GitHub 仓库](https://github.com/your_username/FalconFlask)。

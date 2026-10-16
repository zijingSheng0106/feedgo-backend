# FeedGo Backend

FeedGo 短视频平台的独立后端仓库，使用 Go 提供账号、视频、Feed、关注、点赞、评论、通知、私信及分片上传能力。

## 本地测试

```bash
go test ./...
```

## 本地运行 API

先准备 MySQL、Redis 和 RabbitMQ，然后执行：

```bash
CONFIG_PATH=configs/config.compose-local.yaml go run ./cmd
```

Windows PowerShell：

```powershell
$env:CONFIG_PATH = 'configs/config.compose-local.yaml'
go run ./cmd
```

## Docker Compose

将本仓库与前端仓库放在同一级目录：

```text
projects/
├── feedgo-backend/
└── feedgo-frontend/
```

然后在本仓库执行：

```bash
docker compose up -d --build
```

前端地址为 `http://localhost:5173`，后端 API 地址为 `http://localhost:8080`。

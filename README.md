# ALICE-DB-Enterprise SaaS

Enterprise database with auth, audit, and encryption

## License

AGPL-3.0

## Architecture

```
Frontend :3000  -->  API Gateway :8080  -->  Core Engine :8081
```

| Layer | Port | Technology |
|-------|------|-----------|
| Frontend | 3000 | Next.js 14, Tailwind CSS |
| API Gateway | 8080 | Rust, Axum |
| Core Engine | 8081 | Rust, Axum, ALICE-DB-Enterprise |

## Endpoints

| Method | Path | Description |
|--------|------|-------------|
| `POST /api/v1/query` | 認証付きクエリ実行 |
| `GET  /api/v1/audit` | 監査ログ取得 |
| `POST /api/v1/users` | ユーザー管理 |
| `GET`  | `/health` | ヘルスチェック |

## Quick Start

```bash
cd services/core-engine
cargo run --release
curl http://localhost:8081/health
```

## Author

Moroya Sakamoto

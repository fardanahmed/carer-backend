# carer-backend

Backend for the CARER platform website (the frontend lives in [carer-platform](https://github.com/fardanahmed/carer-platform)). Express 5 on Node 22, TypeScript run directly with `--experimental-strip-types`.

## Status

Early. The server currently exposes two routes and a request logger; the data layer (Mongoose, Neon Postgres driver) and email (Resend) are installed but not wired yet.

| Method | Path | Returns |
|---|---|---|
| `GET` | `/health` | `{ "status": "ok" }` |
| `GET` | `/status` | uptime, memory, Node version, environment |

## Run

```bash
npm install
cp .env.example .env.local   # PORT, CORS_ORIGIN, RESEND_API_KEY, DATABASE_URL
npm run dev                  # http://localhost:8787
```

`npm start` runs the same entry point without watch. `npm test` runs `node --test` over `tests/*.test.ts` (no tests yet).

## License

MIT, see [LICENSE](LICENSE).

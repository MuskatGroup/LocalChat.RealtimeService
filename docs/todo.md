# RealtimeService — TODO

## P0 — MVP

- [ ] SignalR hub + JWT на connect
- [ ] join user/conversation groups
- [ ] внутренний endpoint/очередь `NewMessage` от Chat
- [ ] push `message.created` участникам
- [ ] typing events
- [ ] presence basic
- [ ] Dockerfile + health
- [ ] проксирование через Gateway

## P1

- [ ] delivery/read receipts
- [ ] устойчивость к reconnect / replay последних N (опционально)
- [ ] метрики соединений

## P2

- [ ] group fan-out оптимизация
- [ ] Redis backplane
- [ ] интеграция call signaling events

## Вне скоупа

- персистентная история, медиахранилище, E2EE.

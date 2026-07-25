# LocalChat.RealtimeService

Realtime-слой LocalChat: доставка ciphertext, typing, presence и receipts через SignalR (или аналог). Не хранит историю сообщений.

## Назначение

- WebSocket/SignalR hubs для онлайн-клиентов;
- push нового сообщения участникам диалога;
- typing indicators, presence (online/offline), delivery/read receipts;
- позже — fan-out в группы и вспомогательные события звонков.

## Стек

- .NET 10
- SignalR
- (позже) Redis backplane при нескольких инстансах

## Документация

- [Обзор](docs/overview.md)
- [TODO](docs/todo.md)

## Запуск

Через Orchestrator. Плановый порт: **5103**.

## Связанные репозитории

| Репозиторий | Роль |
|---|---|
| [LocalChat.ChatService](https://github.com/MuskatGroup/LocalChat.ChatService) | Источник NewMessage |
| [LocalChat.Gateway](https://github.com/MuskatGroup/LocalChat.Gateway) | Прокси WS |
| [LocalChat.CallService](https://github.com/MuskatGroup/LocalChat.CallService) | Signaling events (P2) |
| [LocalChat.Web](https://github.com/MuskatGroup/LocalChat.Web) | Клиент |

## Лицензия

Apache-2.0 — см. [LICENSE](LICENSE).

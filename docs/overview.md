# RealtimeService — обзор

## Ответственность

- аутентифицировать SignalR-подключение по JWT;
- подписывать соединение на conversation groups / user groups;
- принимать внутренние события от ChatService и пушить клиентам;
- typing / presence / receipts как лёгкие ephemeral-события.

## Типы событий (план)

| Событие | Описание |
|---|---|
| `message.created` | ciphertext + метаданные |
| `typing.started` / `typing.stopped` | индикатор набора |
| `presence.changed` | online/offline |
| `receipt.delivered` / `receipt.read` | статусы |
| `call.signal` (P2) | опциональный транспорт для CallService |

## Что сервис НЕ делает

- не является source of truth для истории (это Chat);
- не расшифровывает сообщения;
- не принимает upload файлов;
- не выдаёт JWT.

## Масштабирование

MVP — один инстанс. Далее Redis backplane / sticky sessions за Gateway.

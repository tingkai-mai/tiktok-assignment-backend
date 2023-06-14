## Installation

Requirement:

- golang 1.18+
- docker

To install dependency tools:

```bash
make pre
```

## Run

```bash
docker-compose up -d
```

Check if it's running:

```bash
curl localhost:8080/ping
```

## Introduction

This was written with the help of [this guide](https://o386706e92.larksuite.com/docx/QE9qdhCmsoiieAx6gWEuRxvWsRc). However, I made some further changes to the code, with the best of my ability.

Chatrooms are defined in key:value pairs. For example, a chatroom between the people "jack" and "marcus" would be "jack:marcus".

## Available Endpoints

1. `/api/pull` Retrieves all messages in a chatroom, "jack:marcus", with the specified filter. Example:

```json
{
    "chat": "jack:marcus",
    "cursor": 0,
    "limit": 10,
    "reverse": true
}
```

2. `/api/push` pushes a message to a chat room.

```json
{
    "chat": "jack:marcus",
    "text": "Hello how are you",
    "sender": "jack"
}
```

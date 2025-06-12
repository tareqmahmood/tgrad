# tgrad

`tgrad` is a lightweight Python-based Telegram daemon. It lets other programs send messages to a Telegram bot using a local Unix domain socket. Includes a CLI and a Python API.


## ✨ Features

- 🧵 Runs as a background daemon
- 🧾 Message delivery to Telegram via local socket
- ⚙️ Easy CLI tools to configure, run, and send messages
- 🐍 Python API (`tgrad.send()`) for direct integration


## 📦 Installation

```bash
git clone https://github.io/tareqmahmood/tgrad.git
cd tgrad
pip install .
```

## ⚙️ Configuration

Before using the server or client, set up your bot:

```bash
tgrad-config -t <BOT_TOKEN> -c <CHAT_ID> [-s ~/.tgrad/tgrad.sock]
```

This saves your bot token, chat ID, and socket path to `~/.tgrad/config.json`.


## 🚀 Usage

### Start the Daemon Server

```bash
tgrad-server
```

It will listen for messages on the configured Unix socket.

### Send a Message via CLI

```bash
tgrad-client -t "Title" -m "Hello from CLI"
```

### Send a Message from Python

```python
import tgrad
tgrad.send("Alert", "Something happened!")
```

## 🧪 Testing

To test locally:

1. Run the server:

   ```bash
   tgrad-server
   ```

2. In another terminal:

   ```bash
   tgrad-client -t "Test" -m "This is a test message"
   ```

You should receive the message via your Telegram bot.


## 📄 License

MIT License.

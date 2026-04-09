---
name: voice-input
description: Record voice via Bluetooth headset and transcribe with OpenAI Whisper API.
---

# Voice Input Skill

## Setup
```bash
export OPENAI_API_KEY="ключ"
```

## Record via PipeWire (правильный способ)
```bash
# Записать 10 секунд
pw-record --target bluez_input.88_92_CC_A5_DE_D8.0 \
  --rate 16000 --channels 1 --format s16 \
  /tmp/voice.wav -- sleep 10

# Транскрибировать
python3 - << 'PYTHON'
from openai import OpenAI
client = OpenAI()
with open("/tmp/voice.wav", "rb") as f:
    text = client.audio.transcriptions.create(
        model="whisper-1", file=f, language="ru"
    )
print(text.text)
PYTHON
```

## Device
BT headset: bluez_input.88_92_CC_A5_DE_D8.0

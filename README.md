# Master and  Slave Lighting

## Function Node Code
```yaml
const cs = global.get('homeassistant').homeAssistant.states[msg.topic].state;
const cc = global.get('homeassistant').homeAssistant.states[msg.topic].attributes.rgb_color;
const cb = global.get('homeassistant').homeAssistant.states[msg.topic].attributes.brightness;
const ce = global.get('homeassistant').homeAssistant.states[msg.topic].attributes.effect;

if (msg.payload == "off") {
    msg.payload = {"action": "light.turn_off" };
    return msg;
};

msg.payload = { "action": "light.turn_" + cs,
    data: {
        "rgb_color": cc,
        "brightness": cb,
        "effect": ce
    }
};
return msg;
```

# Watch the full tutorial here: https://youtu.be/FyHhlcHRPJ4

---
### 🤝 Found this useful, want to say 'Thanks' and support my efforts. CHEERS🍺
| Buy me a Coffee | PATREON |
|-----------------|---------|
| [![Buy Me A Coffee](https://img.shields.io/badge/Buy%20Me%20A%20Coffee-donate-yellow.svg?style=flat-square&logo=buy-me-a-coffee)](https://www.buymeacoffee.com/3ative) | [![Patreon](https://img.shields.io/badge/Patreon-support-red.svg?style=flat-square&logo=patreon)](https://www.patreon.com/3ative) |
---

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

___
#### 💖 Found this useful, want to say '*Thanks*' and support my efforts. *CHEERS*🍺
| Buy me a Coffee | PATREON |
|-----------------|---------|
| https://www.buymeacoffee.com/3ative | https://www.patreon.com/3ative |

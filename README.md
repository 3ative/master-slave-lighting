# Master and  Slave Lighting

## Function Node Code
```yaml
const cs = global.get('homeassistant').homeAssistant.states[msg.topic].state;
const cc = global.get('homeassistant').homeAssistant.states[msg.topic].attributes.rgb_color;
const cb = global.get('homeassistant').homeAssistant.states[msg.topic].attributes.brightness;
const ce = global.get('homeassistant').homeAssistant.states[msg.topic].attributes.effect;

msg.payload = { "domain": "light", "service": "turn_" + cs,
    data: {
        "rgb_color": cc,
        "brightness": cb,
        "effect": ce
    }
};
return msg;
```

# Watch the full tutorial here: https://youtu.be/FyHhlcHRPJ4


🎁 Found this useful or want to say 'thanks' and support my efforts...

[![BMC](https://www.buymeacoffee.com/assets/img/custom_images/white_img.png)](https://www.buymeacoffee.com/3ative) **And leave a me a message to let me know.**  ❤

🍺 CHEERS! 👍

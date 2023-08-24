<!--
 * @Author: SpenserCai
 * @Date: 2023-08-24 00:06:52
 * @version: 
 * @LastEditors: SpenserCai
 * @LastEditTime: 2023-08-24 18:07:40
 * @Description: file content
-->
# SD-WEBUI-DISCORD-EX
This is an extension of [SD-WEBUI-DISCORD](https://github.com/SpenserCai/sd-webui-discord) for the Stable Diffusion WebUI, which enables a Discord bot for distributed deployment of SD nodes. The command usage on Discord can be referred to the [SD-WEBUI-DISCORD](https://github.com/SpenserCai/sd-webui-discord) project.

## Usage
1. Install this extensions from the 'Extensions' tab page of the Stable Diffusion WebUI.

2. Create a Discord bot and get the bot token. The tutorial can be found [here](https://discord.com/developers/docs/getting-started).

3. Set the bot token in `stable-diffusion-webui/extensions/sd-webui-discord-ex/bin/config.json`.Only need set host and token and server_id(if you don't know set it empty like `"server_id": ""`).
```json
{
    "sd_webui":{
        "servers":[
            {
                "name":"webui-1",
                "host":"127.0.0.1:7860",
                "max_concurrent":5,
                "max_queue":100,
                "max_vram":"20G"
            }
        ]
    },
    "discord":{
        "token":"<your token here>",
        "server_id":"<your servers id here if empty all servers>"
    }
}
```

4. Restart the Stable Diffusion WebUI.
   
5. Find `Discord` tab and click `Start` button to start the Discord bot.
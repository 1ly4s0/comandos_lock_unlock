![Node build](https://github.com/eritislami/evobot/actions/workflows/node.yml/badge.svg)

![logo](https://cdn.discordapp.com/attachments/933698201486237716/947555143795228682/Diseno_sin_titulo_22.png)

# 🤖 Tutorial Discord Bot (TECNO BROS)
> Código del bot del tutorial de TECNO BROS, el vídeo es [este](https://youtu.be/5Rn375Uzh4c)
## Requisitos

1. Tener un bot de Discord creado **[Guía](https://www.youtube.com/watch?v=qXev2kf-q_0)**
2. Tener Discord.js V12 o Discord.js V13 **[Guía](https://www.youtube.com/watch?v=qXev2kf-q_0)**
3. Tener el bot hosteado o en tu PC **[Guía](https://www.youtube.com/watch?v=0MkVTtLoMiI)**  
4.1 **(Opcional)** Tener el bot en algun host **[Guía](https://www.youtube.com/watch?v=0MkVTtLoMiI)**

## 🚀 Código de LOCK

```js
client.on("messageCreate", async message => {
    if(message.content.startsWith("tb!lock")) {
        if(!message.member.permissions.has("MANAGE_CHANNELS")) return message.reply("No tienes permisos para usar este comando.")
        message.channel.permissionOverwrites.edit(message.guild.id, {
            SEND_MESSAGES: false
        })

        const Embed = new Discord.MessageEmbed()
        .setDescription("🔒 Canal cerrado correctamente.")
        message.channel.send({ embeds: [Embed] })
    }
})




```

## 🚀 Código de UNLOCK

```js

client.on("messageCreate", async message => {
    if(message.content.startsWith("tb!unlock")) {
        if(!message.member.permissions.has("MANAGE_CHANNELS")) return message.reply("No tienes permisos para usar este comando.")
        message.channel.permissionOverwrites.edit(message.guild.id, {
            SEND_MESSAGES: true
        })

        const Embed = new Discord.MessageEmbed()
        .setDescription("🔓 Canal abierto correctamente.")
        message.channel.send({ embeds: [Embed] })
    }
})





```
Después de modificar o añadir algo al código, recuerda o reiniciar tu bot o usar el comando `node index.js` para que los cambios se apliquen.

## ⚙️ Uso:

## LOCK
![logo](https://cdn.discordapp.com/attachments/933698201486237716/1036045350269628416/unknown.png)

## UNLOCK
![logo](https://cdn.discordapp.com/attachments/933698201486237716/1036045392997011516/unknown.png)





## 📝 Créditos
* [DISCORD](https://discord.gg/tecnobros)
* [YOUTUBE](https://youtube.com/tecnobros)

Copyright © **1ly4s0#2477** - 2022

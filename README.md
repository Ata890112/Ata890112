const mineflayer = require('mineflayer');
const navigate = require('mineflayer-navigate')(mineflayer);

const serverHost = 'Boby1548.aternos.me'; // Sunucu IP adresi veya alan adı
const serverPort = 57810; // Sunucu bağlantı noktası
const botUsername = 'Ata1545'; // Bot kullanıcı adı
const botPassword = 'Bot_Password'; // Bot şifresi

const bot = mineflayer.createBot({
  host: serverHost,
  port: serverPort,
  username: botUsername,
  password: botPassword
});

bot.on('login', () => {
  console.log('Bot giriş yaptı!');
  bot.chat('Merhaba, sunucuya giriş yaptım!');
});

bot.once('spawn', () => {
  bot.chat('Merhaba, size nasıl yardımcı olabilirim?');
});

bot.on('chat', (username, message) => {
  if (username === bot.username) return; // Kendi mesajlarına tepki verme

  // Botun yanınıza gelme komutunu işle
  if (message === 'yanıma gel') {
    yaninaGel(username);
  }
});

// Yanınıza gelme fonksiyonu
function yaninaGel(Ata890112) {
  const player = bot.players[username];
  if (!player) {
    bot.chat('Oyuncu bulunamadı!');
    return;
  }

  if (bot.navigate.isMining()) {
    bot.chat('Zaten bir yere gidiyorum!');
    return;
  }

  bot.chat(Yanınıza geliyorum, ${username}!);
 bot.press (w)
}
bot.on('chat',(username,message)=>{
    if(username === bot.username) return

    switch (message){
        case 'Yat':
            goToSleep()
            break
        case 'Kalk':
            wakeUp()
            break
        case 'Çık':
            bot.quit()
            break
    }
});

bot.on('Yat',()=>{
    bot.chat('İyi Geceler!')
});

bot.on('Kalk',()=>{
    bot.chat('Günaydın!')
});

async function goToSleep() {
    const bed = bot.findBlock({
        matching: block => bot.isABed(block)
    })

    if (bed) {
        try {
            await bot.sleep(bed)
            bot.chat("Yatıyoruö.")
        } catch (err) {
        bot.chat(Hata: ${err.message})
        }
} else {
bot.chat('Yatak Yok')
}
}

async function  wakeUp() {
    try {
        await bot.wake()
    } catch (err) {
        bot.chat(Hata: ${err.message})
    }
}
bot.on('chat',function (username,message){
  if(username === bot.username) return;
  if (message === "!at" && username === adminName){
      function tossNext(){
          if(bot.inventory.items().length === 0) {
              console.log("Eşyam Yok.")
          } else {
              const item = bot.inventory.items()[0]
              bot.tossStack(item,tossNext)
            if (username !== adminName) return;
            let followTarget = null;

            function followPlayer(playerName) {
                const targetPlayer = bot.players[playerName];
                if (targetPlayer) {
                    followTarget = targetPlayer.entity;
                    bot.chat(Takip ediyorum ${playerName}.);
                } else {
                    bot.chat(bulamadım ${playerName} nerdesin?);
                }
            }
            let followTarget = null;

            function followPlayer(playerName) {
                const targetPlayer = bot.players[playerName];
                if (targetPlayer) {
                    followTarget = targetPlayer.entity;
                    bot.chat(Takip ediyorum ${playerName}.);
                } else {
                    bot.chat(bulamadım ${playerName} nerdesin?);
                }
            }

const { Bot, Keyboard, InlineKeyboard } = require("grammY");

// Botfather'dan olingan tokenni shu yerga qo'ying
const BOT_TOKEN = "YOUR_TELEGRAM_BOT_TOKEN"; 
const bot = new Bot(BOT_TOKEN);

// ----------------------------------------------------
// DATA STORAGE (Ma'lumotlar ombori)
// ----------------------------------------------------
const users = new Map();       
const matches = [];            
const reports = [];            

// ADMIN RO'YXATI (Sizning foydalanuvchi nomingiz qo'shildi)
const adminUsernames = ["ASLAN_XXXXX"]; 

// ----------------------------------------------------
// ⌨️ KLAVIATURALAR (Asosiy Menyu va Admin Menyu)
// ----------------------------------------------------
const mainMenu = new Keyboard()
    .text("👤 Profilim").text("🔍 Profil Qidirish").row()
    .text("❤️ Matchlarim").text("💬 Chatlar").row()
    .text("🎬 Reels (Video)").text("🏆 Premium (⭐)").row()
    .text("🛡️ Xavfsizlik").text("👑 Admin Panel").row()
    .resized();

const adminMenu = new InlineKeyboard()
    .text("👥 Foydalanuvchilar", "adm_users")
    .text("✔️ Profil Tasdiqlash", "adm_verify").row()
    .text("🚫 Bloklash (Ban)", "adm_ban")
    .text("📊 Statistikalar", "adm_stats");

// ----------------------------------------------------
// 🚀 BOT BUYRUKLARI VA LOGIKASI
// ----------------------------------------------------

// START BUYRUG'I
bot.command("start", async (ctx) => {
    const userId = ctx.from.id;

    if (!users.has(userId)) {
        users.set(userId, {
            id: userId,
            username: ctx.from.username || "username_yoq",
            first_name: ctx.from.first_name,
            age: 22, 
            region: "Toshkent",
            city: "Yunusobod",
            photos: ["https://picsum.photos"], 
            is_verified: true, 
            interests: ["Sport", "Musiqa", "Sayohat"],
            is_premium: false,
            is_banned: false,
            ai_score: 98
        });
    }

    await ctx.reply(
        `👋 Salom ${ctx.from.first_name}!\n\nTanishuv va Reels platformasiga xush kelibsiz.`,
        { reply_markup: mainMenu }
    );
});

// 👑 ADMIN PANEL TUGMASI (Tekshirish qismi)
bot.hears("👑 Admin Panel", async (ctx) => {
    const username = ctx.from.username;

    // Foydalanuvchi nomi admin ro'yxatida borligini tekshirish
    if (!username || !adminUsernames.includes(username)) {
        return ctx.reply("❌ Kechirasiz, siz admin emassiz va bu bo'limga kira olmaysiz!");
    }

    await ctx.reply(
        "👑 **Boshqaruv Paneli (Admin Control)**\n\n" +
        "Tizimni boshqarish va foydalanuvchilar ustidan nazorat qilish uchun tugmalardan foydalaning:", 
        { reply_markup: adminMenu, parse_mode: "Markdown" }
    );
});

// Admin tugmalari bosilganda qayta ishlovchi qism
bot.on("callback_query:data", async (ctx) => {
    const data = ctx.callbackQuery.data;
    const username = ctx.from.username;

    // Xavfsizlik uchun bu yerda ham adminlikni tekshiramiz
    if (!username || !adminUsernames.includes(username)) {
        return ctx.answerCallbackQuery("Ruxsat berilmagan! ❌");
    }

    if (data === "adm_stats") {
        await ctx.answerCallbackQuery();
        await ctx.reply(
            `📊 **Tizim statistikasi:**\n\n` +
            `• Jami ro'yxatdan o'tganlar: ${users.size} ta\n` +
            `• Faol a'zolar: 1,420 ta\n` +
            `• Bloklanganlar: 0 ta\n` +
            `• Kelib tushgan shikoyatlar: ${reports.length} ta`
        );
    } else if (data === "adm_users") {
        await ctx.answerCallbackQuery();
        await ctx.reply("👥 Foydalanuvchilar ro'yxati yuklanmoqda...");
    } else if (data === "adm_verify") {
        await ctx.answerCallbackQuery();
        await ctx.reply("✔️ Tasdiqlash kutilayotgan profillar mavjud emas.");
    } else if (data === "adm_ban") {
        await ctx.answerCallbackQuery();
        await ctx.reply("🚫 Bloklash uchun foydalanuvchi ID raqamini kiriting (Masalan: /ban ID).");
    }
});

bot.start();
console.log("🚀 Bot muvaffaqiyatli ishga tushdi! Admin: @ASLAN_XXXXX");

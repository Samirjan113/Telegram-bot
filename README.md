# Telegram-bot
pip install python-telegram-bot
from telegram import Update_Funstat | funstatbot
from telegram.ext import Updater_@funstarobot CommandHandler, MessageHandler, Filters, CallbackContext

TOKEN = "7795389394:AAFg_jNmgzqlmhTtP0R2O6eoH7Bx0VpjfYs"

def start(update: Update, context: CallbackContext):
    update.message.reply_text("Olá! Sou um bot de reações. Envie algo e eu respondo!")

def react(update: Update, context: CallbackContext):
    text = update.message.text.lower()
    if "bom dia" in text:
        update.message.reply_text("🌞 Bom dia!")
    elif "obrigado" in text:
        update.message.reply_text("💖 De nada!")
    else:
        update.message.reply_text("👍 Recebido!")

updater = (7795389394:AAFg_jNmgzqlmhTtP0R2O6eoH7Bx0VpjfYs, use_context=True)
dp = updater.dispatcher
dp.add_handler(CommandHandler("start", start))
dp.add_handler(MessageHandler(Filters.text & ~Filters.command, react))

updater.start_polling()
updater.idle()

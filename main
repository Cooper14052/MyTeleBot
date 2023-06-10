from config import TOKEN  # импорт токена бота
import telebot


def telegram_bot(TOKEN):
    bot = telebot.TeleBot(TOKEN)  # оболочка бота и главная функция

    @bot.message_handler(commands=["start"])  # Команда старт
    def start_message(message):
        bot.send_message(message.chat.id, "Добрый день!")  # Вывод при команде старт

        @bot.message_handler(content_types=["text"])  # Ответ на слово
        def send_text(message):
            if message.text == 'Да':
                bot.send_message(message.chat.id, 'Это вам нужно!')
            else:
                bot.send_message(message.chat.id, 'Вы уверены?')

    bot.polling()


if __name__ == '__main__':
    telegram_bot(TOKEN)

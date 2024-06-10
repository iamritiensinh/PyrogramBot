<h2>Cảm ơn vì đã sử dụng tôi 💖. Đây là một số ví dụ về việc gửi tin nhắn qua bot telegram</h2>

<h3>Gửi tin nhắn trả lời khi ai đó bắt đầu bot.</h3>
<em>Nếu ai đó khởi động bot của bạn hoặc gửi /start trong cuộc trò chuyện bạn có thể sử dụng cái này để gửi thư trả lời nó. Ngoài ra, bạn có thể sử dụng phương pháp này cho các lệnh khác</em>
<br><br>

```
@Client.on_message(filters.command("start"))
async def start(bot, cmd):
```
* <p>Bạn có thể sử dụng các bộ lọc để xác định các lệnh của người dùng. </p>

```
@Client.on_message(filters.command("start") & filters.incoming & ~filters.edited & filters.private)
async def start(bot, cmd):
```

* <p>Bạn cũng có thể thêm văn bản vào bàn phím. Chúng ta sẽ nói về điều đó, tiếp tục đọc ...</p>

```
@Client.on_message(filters.command("start") & filters.private)
async def start(bot, command):
    await command.reply_text(
        text = "Hi {}!, this is wellcom message".format(command.from_user.first_name),
        disable_web_page_preview=True,
        reply_markup=InlineKeyboardMarkup(
            [
                [
                    InlineKeyboardButton("🔮Help", callback_data='help_cb'),
                    InlineKeyboardButton("⚔About", callback_data='about_cb')
                ]
            ]
        )
    )
```

<br><br>
<h3>Gửi ảnh trả lời có chú thích khi ai đó khởi động bot.</h3>
<em>Thêm url ảnh của bạn. nó sẽ kết thúc bằng .jpg hoặc .jpeg</em>
<br><br>

```
@Client.on_message(filters.command("start") & filters.private)
async def start(bot, command):
    await command.reply_photo(
        photo = "https://telegra.ph/file/adffc5ce502f5578e2806.jpg",
        caption = "Hi {}!, this is wellcom message".format(command.from_user.first_name), 
        disable_web_page_preview=True,
        reply_markup=InlineKeyboardMarkup(
            [
                [
                    InlineKeyboardButton("🔮Help", callback_data='help_cb'),
                    InlineKeyboardButton("⚔About", callback_data='about_cb')
                ]
            ]
        )
    )
    
```

* <p> Kiểm tra <a href="https://docs.pyrogram.org/api/bound-methods/Message.reply">tài liệu này</a> để tìm hiểu thêm về phương pháp trả lời</p>

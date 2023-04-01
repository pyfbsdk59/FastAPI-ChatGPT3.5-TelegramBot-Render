# FastAPI-ChatGPT3.5-TelegramBot-Render
# 一個使用FastAPI框架和GPT3.5 turbo模型官方API，創造一個TelegramBot，快速建置於平台Render。


## [TelegramBot Vercel GPT3.5 turbo/ChatGPT版本部署](https://github.com/pyfbsdk59/Flask-official-ChatGPT-TelegramBot-Vercel)

<div align="center">
  <img src="demo/demo_351.png" width="500"/>
</div>


## [TelegramBot Render GPT3版本部署](https://github.com/pyfbsdk59/Flask-ChatGPT-TelegramBot-Render)

<div align="center">
  <img src="demo/link.png" width="700"/>
</div>

## [LineBot Django Vercel GPT3版本部署](https://github.com/pyfbsdk59/Django-ChatGPT-linebot-Vercel)

<div align="center">
  <img src="demo/link2.png" width="700"/>
</div>

## [TelegramBot Golang Render GPT3版本部署](https://github.com/pyfbsdk59/Golang-ChatGPT-TelegramBot-Render)

<div align="center">
  <img src="demo/link3.png" width="700"/>
</div>

<div align="center">
  <img src="demo/link3a.png" width="600"/>
</div>

## [LineBot Golang Render GPT3版本部署](https://github.com/pyfbsdk59/Golang-ChatGPT-linebot-Render)

<div align="center">
  <img src="demo/link4.png" width="700"/>
</div>


#### GPT3 TelegramBot Vercel部署版本。程式猿影音教學參考。請支持且訂閱加按讚感謝他的辛勞。

https://www.youtube.com/watch?v=eKKEa6NhCd0

<div align="center">
  <img src="demo/demo0.png" width="800"/>
</div>


### [English](https://github.com/pyfbsdk59/FastAPI-GPT3.5-TelegramBot-Render/blob/main/README_en.md)
### [日本語](https://github.com/pyfbsdk59/FastAPI-GPT3.5-TelegramBot-Render/blob/main/README_jp.md)





#### 1. 本專案因部屬在Render上，所以程式碼和Docker版本不同，使用FastAPI和設定webhook。


#### 2. 設定webhook請參考以下網址。Render網站中，選擇新增「Web Services」，可用github帳號匯入此專案，可先fork到自己的帳號，然後設定自己的名稱和選擇免費free方案。記得按下方「Advanced」，設定環境變數。

https://zaoldyeck.medium.com/%E6%89%8B%E6%8A%8A%E6%89%8B%E6%95%99%E4%BD%A0%E6%80%8E%E9%BA%BC%E6%89%93%E9%80%A0-telegram-bot-a7b539c3402a

<div align="center">
  <img src="demo/render1.png" width="600"/>
</div>

<div align="center">
  <img src="demo/render2.png" width="700"/>
</div>


#### 3. 必須在Render的Environment Variables設定兩個環境變數，分別是OPENAI_API_KEY和TELEGRAM_BOT_TOKEN。然後開始部屬，可能要花上一些時間。成功後複製自己的URL。例如：

https://xxx.onrender.com/

<div align="center">
  <img src="demo/render3.png" width="700"/>
</div>

#### 4. Start Command請輸入：

uvicorn main:app --host 0.0.0.0

<div align="center">
  <img src="demo/render_uvicorn.png" width="700"/>
</div>

#### 5. 等待完成後，打開瀏覽器，輸入以下網址，設定webhook為部屬完Render的最後步驟，格式為：https://api.telegram.org/bot{$token}/setWebhook?url={$webhook_url}。

##### 故實際範例就像以下範例（非直接複製使用，請改用自己的telegram token和Render專案的URL）：


https://api.telegram.org/bot606248605:AAGv_TOJdNNMc_v3toHK_X6M-dev_1tG-JA/setWebhook?url=https://xxx.onrender.com/callback


#### 5. 成功後會顯示以下文字：

{
  ok: true,
  result: true,
  description: "Webhook was set"
}
------
### 創建Telegram機器人和取得token，請參考： 
https://ithelp.ithome.com.tw/articles/10245264<br><br>
https://tcsky.cc/tips-01-telegram-chatbot/

### FastAPI Render設置請參考： 
https://salaivv.com/2023/01/04/telegram-bot-fastapi
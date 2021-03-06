# Profiles
📖 [文档](https://github.com/NavePnow/Profiles/blob/master/README.md) | 📖 Docs

## Filter - Ruleset of Surge and QuantumultX

## Scripts

### filter_conversion.js
**powered by CLOUDFLARE Workers**

<img src="https://cdn.jsdelivr.net/gh/NavePnow/blog_photo@private/process.jpeg" height="60%" width="60%">

1. Features
    1. Generate Surge Ruleset from QuantumultX filter link and vice versa.
    2. Change Ruleset automatically if source file changed.
2. Instructions
    1. Create new worker in Cloudflare 
    2. Copy all contents in Editor
    3. Fill in required content (url and replace regex)
    4. Save and Deploy
    5. Enjoy ur life
   
### checkin.js
**By [Neurogram](https://github.com/Neurogram-R) feat [NavePnow](https://github.com/NavePnow)**

<img src="https://cdn.jsdelivr.net/gh/NavePnow/blog_photo@private/IMAGE 2019-11-12 19:57:53.jpg" height="40%" width="40%">

1. Features
   1. Show Used data, Rest data and Due date
   2. Use Cron to run scripts periodically
2. Instructions
   1. `https://www.notion.so/Check-in-0797ec9f9f3f445aae241d7762cf9d8b`
   2. Check the data format and modify the regex if something goes wrong

### checkin_1point.js
**By [NavePnow](https://github.com/NavePnow) feat [wangfei021325](https://t.me/wangfei021325)**

<img src="https://cdn.jsdelivr.net/gh/NavePnow/blog_photo@private/IMAGE 2019-11-12 19:58:49.jpg" height="40%" width="40%">
Auto check-in for 1point3acres.com

[Tutorial](https://nave.work/%E4%B8%80%E4%BA%A9%E4%B8%89%E5%88%86%E5%9C%B0%E8%87%AA%E5%8A%A8%E7%AD%BE%E5%88%B0%E8%84%9A%E6%9C%AC.html)

### 10010+.js/10010+_qx.js
**By [NavePnow](https://github.com/NavePnow)**
Modified according to the Jsbox script from author [coo11](https://t.me/coo11) 

<img src="https://cdn.jsdelivr.net/gh/NavePnow/blog_photo@private/IMG_0666.PNG" height="40%" width="40%">

1. Features
   1. Show Rest time, Rest fee and Rest flow
   2. Use Cron to run scripts periodically
2. Instructions
   1. Set your China Unicom number in Mini Program of Alipay (provided api)
   2. Create 10010+.js under Surge/[QuantumultX](https://raw.githubusercontent.com/NavePnow/Profiles/master/Scripts/10010%2B_qx.js) folder and copy all the content of [link](https://raw.githubusercontent.com/NavePnow/Profiles/master/Scripts/10010%2B.js)
   3. Add your phone number into required place
   4. Open Surge in Edit mode and write `cron "00 12 * * *" debug=1,script-path=10010+.js` below the config
      QuantumultX(below the [[task_local]): `00 12 * * * 10010+_qx.js`
   5. Save it and enjoy your life
    
3. ⚠️ Something you know know
    1. If you want to put the file online, make sure keep it private because the response data of Alipay provide your REAL NAME.
    2. Feel free to [contact me](https://t.me/Leped_Bot) if you have any problem.

### weather.js/weather_qx.js
**By [NavePnow](https://github.com/NavePnow)**
**powered by Dark Sky**

<img src="https://cdn.jsdelivr.net/gh/NavePnow/blog_photo@private/IMG_0886.jpg" height="40%" width="40%">

1. Features
   1. Show weather icon, range of temperature, precipProbability and hourly summary
   2. Use Cron to run scripts periodically (8am-8pm Run every 3 hours)
2. Instructions
   1. Register at [Dark Sky website](https://darksky.net/dev) and get free api
   2. Download and run [Shortcuts](https://www.icloud.com/shortcuts/11d347ed592f4b67847403a9052666f4)
   3. Add the Secret Key generated from step one to the shortcuts
   4. Open Surge in Edit mode and write `cron "00 8 * * *" debug=1,script-path=weather_dark.js` 
          QuantumultX(below the [[task_local]): `0 8-20/3 * * * weather_dark.js`
   5. Save it and enjoy your life
    
3. ⚠️ Something you know know
    1. If you want to put the file online, make sure keep it private because the API Usage of Dark Sky api if not countless.
    2. Refer to [Dark Sky API](https://darksky.net/dev/docs#overview) if you want to customize your own weather notification.
    3. The purpose of this script is to make a daily weather reminder every morning. The script will be modified accordingly to meet my needs because Dark Sky Api has US extreme weather warning
    4. Feel free to [contact me](https://t.me/Leped_Bot) if you have any problem.

### weibo
**By [NavePnow](https://github.com/NavePnow)**
**inspired by [Nobyda](https://t.me/nubida)**

<img src="https://cdn.jsdelivr.net/gh/NavePnow/blog_photo@private/IMG_1189.JPG" height="40%" width="40%">
Auto check-in for Weibo Super_Talk

[Tutorial](https://nave.work/微博超话自动签到脚本.html)

### google_script/singtel.js
**By [NavePnow](https://github.com/NavePnow)**
**powered by Google Script**

<img src="https://cdn.jsdelivr.net/gh/NavePnow/blog_photo@private/IMG_1888.jpg" height="40%" width="40%">

1. Features
   1. Show Rest time, fee, flow, SMS and Calls.
   2. Run the script remotely
2. Instructions
   1. Create a bot from [BotFather](https://telegram.me/BotFather) and replace `BOT_TOKEN` with token received from bot father
   2. Get your personal chat id from [get_id_bot](https://telegram.me/get_id_bot) and replace `CHAT_ID` with it
   3. Install http capture app like [HTTP Catcher](https://apps.apple.com/us/app/http-catcher/id1445874902) on your phone
   4. Install [hi!App](https://apps.apple.com/us/app/singtel-prepaid-hi-app/id1034712778) app from app store and log in by your phone number
   5. Open the http capture app and refresh the hi!App (reopen)
   6. Find request `https://hiapp.aws.singtel.com/api/v2/usage/dashboard`
   7. Write down `Authorization` and `Cookie` and replace them in the script
   8. Copy all content to the `Google Script Editor`
   9. Set a proper time to trigger it
3. ⚠️ Something you know know
    1. Feel free to [contact me](https://t.me/Leped_Bot) if you have any problem.

### google_script/calendar.js
**By [NavePnow](https://github.com/NavePnow)**
**powered by Google Script and Google Developers Console**

<img src="https://cdn.jsdelivr.net/gh/NavePnow/blog_photo@private/IMG_1925.jpg" height="40%" width="40%">

1. Features
   1. Set muliply calendars according to `Google Calendar Api`
   2. Run the script remotely
2. Instructions
   1. Create a bot from [BotFather](https://telegram.me/BotFather) and replace `BOT_TOKEN` with token received from bot father
   2. Get your personal chat id from [get_id_bot](https://telegram.me/get_id_bot) and replace `CHAT_ID` with it
   3. Register your application with the [Google Developers Console](https://console.developers.google.com)
   4. Activate the Google Calendar API in the [Google Developers Console](https://console.developers.google.com)
   5. Under Credentials, create a new Public API access key and replace the `API_KEY` with it
   6. Find personal Calendar ID under `[Google Calendar] -> [Setting and Sharing] -> [Calendar Setting]` and add it into `calendar_id` 
   8. Copy all content to the `Google Script Editor`
   9. Set a proper time to trigger it
3. ⚠️ Something you know know
    1. Feel free to [contact me](https://t.me/Leped_Bot) if you have any problem.

# Tip Jar
If you're really, really enjoying the content, you can leave extra tips to support the developer. Thanks for even considering.

| PayPal                                                                                                                                                                       | 微信赞赏 WeChat Pay                                                                                                    |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- |
| [![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=DSZJCN4ZUEW74&currency_code=USD&source=url) | <img src="https://cdn.jsdelivr.net/gh/NavePnow/blog_photo@private/1234.JPG" width="200">

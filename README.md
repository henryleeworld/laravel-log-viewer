# Laravel 8 日誌觀察器

引入 rap2hpoutre 的 laravel-log-viewer 套件來擴增日誌觀察器以瀏覽日誌紀錄，然而密密麻麻的日誌，卻隱含著客戶來自何方，以及是在什麼時候使用服務，甚至可以了解客戶最喜歡存取什麼服務，或是在使用什麼服務的時候最容易導致錯誤。透過了解使用者，改善用戶體驗來增加客戶數量以及停留時間，進而為網站服務帶來更多收益。

## 使用方式
- 把整個專案複製一份到你的電腦裡，這裡指的「內容」不是只有檔案，而是指所有整個專案的歷史紀錄、分支、標籤等內容都會複製一份下來。
```sh
$ git clone
```
- 將 __.env.example__ 檔案重新命名成 __.env__，如果應用程式金鑰沒有被設定的話，你的使用者 sessions 和其他加密的資料都是不安全的！
- 當你的專案中已經有 composer.lock，可以直接執行指令以讓 Composer 安裝 composer.lock 中指定的套件及版本。
```sh
$ composer install
```
- 產生 Laravel 要使用的一組 32 字元長度的隨機字串 APP_KEY 並存在 .env 內。
```sh
$ php artisan key:generate
```
- 在瀏覽器中輸入已定義的路由 URL 來訪問，例如：http://127.0.0.1:8000。
- 你可以經由 `/logs` 來進行使用日誌觀察器。

----

## 畫面截圖
![](https://i.imgur.com/VDktCfx.png)
> 日誌紀錄提供定義在 RFC 5424 的八個級別：debug、info、notice、warning、error、critical、alert 和 emergency，日誌紀錄只會紀錄比自身設定的等級還高的訊息
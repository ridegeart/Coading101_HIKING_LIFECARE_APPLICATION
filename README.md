# Coading101_HIKING_LIFECARE_APPLICATION
山難事件頻發，據民國104年至今的山難原因統計， 以迷路為最大宗，而失溫是名列前茅的死因，我們設計了一款結合軌跡紀錄與避險預警的應用程式，分別用以減少山難發生以及提高受難時的獲救率。  
![image](https://github.com/ridegeart/Coading101_HIKING_LIFECARE_APPLICATION/assets/73794853/7034f566-706a-43f7-928f-f16f581d1fab)

## UI設計與程式
-> .aia 檔
### 程式架構
 ![image](https://github.com/ridegeart/Coading101_HIKING_LIFECARE_APPLICATION/assets/73794853/f6c01ad1-0b54-431e-b69a-ed72e12b5642)  
-	程式主要包含三個功能，並輔以背景執行及位置感測器完成。  
  1.	預警系統
   -	意識狀況確認：可設置是否啟用，啟用時，定時震動確認使用者意識狀況，輔以「Notificaiton功能」給予相關指示。
   -	失溫預警：定時計算當下溫度與體感溫度的差值。若溫差>5度，表示風速、氣溫、濕度處於異常狀態，有失溫風險。
   -	海拔高度降低提醒：在使用者預備下山返回時，紀錄使用者海拔是否降低，提醒使用者向高處移動。
  2.	軌跡紀錄系統
   -	GSM強度：「手機GSM信號強度> -100」及「軌跡紀錄>3筆」時，將軌跡上傳至網路以CSV格式儲存在雲端。上傳成功手機跳出通知，同時顯示目前軌跡同步最新時間。
   -	背景執行：為確保使用者在使用其他應用程式時我們的程式仍有預警、軌跡紀錄功能但app inventor2預設只能前台執行，因此我們使用了開源擴展功能，達到後台執行的效果。
   -	緊急聯絡人：輸入電話號碼後，自動跳至簡訊頁面，簡訊內容包含軌跡紀錄的雲端網址。
  3. 天氣資訊  
   透過opendata獲取使用者所在地氣象資料，包含溫度、風速、濕度、體感溫度和降雨機率，同時配合天氣資訊及天氣圖示，將天氣狀況具象化體現。
   -	Opendata串接流程：
   ![image](https://github.com/ridegeart/Coading101_HIKING_LIFECARE_APPLICATION/assets/73794853/174a97f7-6cf2-49fd-8467-4d2d3df91e7c)

## APP 下載
-> 下載 .apk 檔安裝在手機上 (Android)

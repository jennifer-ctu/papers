
# papers
## 1.2020臺灣網際網路研討會TANet研討會論文-基於BERT語言預訓練機制之招生事務對話機器人設計

**摘要**

台灣學校的招生人員目前主要採用電話與通訊軟體並行方式與外界溝通。通訊軟體緩減電話直接諮詢的不便，但仍需耗費人力回覆大量的通訊軟體訊息。對話機器人之導入，可以協助招生人員改善通訊軟體諮詢的龐雜負擔。
招生諮詢服務涉及整個學校的行政業務，諮詢對象包括家長、學生及社會人士。招生單位要先理解諮詢問題內容，判斷是否本校服務項目，再判斷問題隸屬單位，接著從負責單位預先準備的文件取得答案後進行回覆。
本研究首先利用Rasa對話機器人套件實作招生人員多輪回合理解問題與意圖分類，例如：當學生提問報名目標學校應備文件的問題，回覆前，招生人員必須透過多輪回合諮詢過程，得到報名學制與報名科系資訊，並判別問題與招生報名有關。其次，使用Elasticsearch資料檢索工具儲存與查詢各行政單位的最新資料，例如：家長與學生常問的「學雜費多少」、「招生報名費多少」及「宿舍房型有哪幾種」三種問題，分別為三種不同單位負責處理。最後，利用Google的BERT語言預訓練機制模型完成閱讀理解任務，從資料檢索工具得到匹配度最高的文件與使用者的提問，對答案進行預測並給予諮詢者回覆。

**閱讀理解系統架構**

![image](https://user-images.githubusercontent.com/131113658/233033038-50533c20-0077-4970-a196-73782e687359.png)


**閱讀理解預測答案結果**

![image](https://user-images.githubusercontent.com/131113658/233033293-11022165-3aa9-45be-b5cf-7bfab936b8ea.png)

**對話機器人介面**

![image](https://user-images.githubusercontent.com/131113658/233033441-1a036e61-3930-41c9-990a-9bd38205c443.png)



## 2.2021碩士畢業論文-基於自然語言處理之招生事務對話機器人

**摘要**

以往大專院(校)利用輪值班、發放紙本文宣、入班宣導及參與就學博覽會方式進行招生事務，學校無法直接得到學生的問題與反應。原有的資訊系統雖能蒐集資料且輔助學校執行招生事務，但需耗費時間人力進行分類整理，且學校僅能使用學生的居住地區、原就讀學校等特徵性資料來分析學生來源。故藉由招生事務導入對話機器人蒐集使用者對話內容，自動蒐集使用者對話內容並進行常見問題分析統計，更有利於學校擬定招生策略。
目前對話機器人廣泛應用在個人助理、硬體控制及企業服務，台灣國內國外的大專院(校)也藉由導入對話機器人處理學校事務，協助學校人員處理學生、家長及社會人士的學校相關問題。
首先，本研究利用Rasa自然語言處理框架實現台灣招生事務諮詢服務。使用Rasa自然語言處理框架的Jieba、Sklearn的CountVectorizer及Dual Intent and Entity Transformer (DIET)自然語言工具依序處理斷詞、特徵擷取、意圖分類及實體擷取任務；採用Rasa自然語言處理框架的Transformer Embedding Dialogue(TED) Policy方法實現多輪對話，運用self-attention機制關注每回合的句子，使招生事務對話機器人納入歷史對話預測下一個動作回覆使用者。
其次，將Rasa自然語言處理框架設計模組管理將其分為自然語言處理模組、對話管理模組及外部整合模組。本研究自行建置資料集與對話機器人模組管理系統，對話機器人模組管理系統依模組管理處理並匯出招生事務的Rasa自然語言處理框架文件，以及提供查看使用者與對話機器人的對話紀錄功能，系統將其統計為常見問題。
最後，利用Sara對話機器人介面作為招生事務對話機器人與使用者溝通的橋樑，並設計對話處理流程與對話情境處理招生事務諮詢服務，以及挑選7名人員進行測試與持續使用意願調查。

**對話機器人介面**

單輪對話-禮貌問候語情境

<img src =https://user-images.githubusercontent.com/131113658/233000104-82cc7e5e-2609-4921-9be4-dfda3790aa70.png width=300 >

單輪對話-詢問學校科系情境

<img src =https://user-images.githubusercontent.com/131113658/233005999-3835d422-2fa2-4dd1-b939-d86d43e33b14.png width=300 >

多輪對話-詢問報名承辦人員情境

<img src =https://user-images.githubusercontent.com/131113658/233010091-3f5f61da-9528-47ae-a877-c0b878c5a0ef.png width=300 ><img src =https://user-images.githubusercontent.com/131113658/233010120-8c1920de-be2d-4996-aa64-c57b493fba62.png width=300 >

多輪對話-詢問報名承辦人例外情境1

<img src =https://user-images.githubusercontent.com/131113658/233010298-16952a98-8d71-427d-bd64-1e0300338980.png width=300 ><img src =https://user-images.githubusercontent.com/131113658/233010327-98907623-68d8-4427-b352-5b44fe690225.png width=300 >

多輪對話-詢問報名承辦人例外情境2

<img src =https://user-images.githubusercontent.com/131113658/233010394-1fab91e2-2da6-4574-9da3-ae104387f770.png width=250 ><img src =https://user-images.githubusercontent.com/131113658/233010446-8556e9bc-e64f-47ea-847c-d1386d200af2.png width=250 ><img src =https://user-images.githubusercontent.com/131113658/233010524-6a385e2e-f3c2-4937-9978-c8305bf96454.png width=250 ><img src =https://user-images.githubusercontent.com/131113658/233010547-0cd8644a-d04b-4e75-80f2-fccd4090e78c.png width=250 >

多輪對話-詢問報名承辦人例外情境3

<img src =https://user-images.githubusercontent.com/131113658/233010610-2b1c9d35-9bd6-427f-bc43-9045f05941b8.png width=300 >



## 3.2022臺灣網際網路研討會TANet研討會論文-基於自然語言處理之心理健康管理聊天機器人設計

**摘要**

現今大環境之下，患者害怕受到他人歧視往往不敢向他人傾訴自己內心真實想法，甚至不敢至醫療場所尋求醫生的協助，舉凡Apple Siri、Google Assistant及Samsung Bixby等個人語音助理已伴隨著人們協助使用者以口語溝通的方式處理個人活動管理等任務，而面臨害怕受到他人歧視的患者是否也能透過個人語音助理的聊天機器人得到心理健康問題的幫助是本研究的課題。
本研究利用Rasa聊天機器人開發框架完成心理健康管理聊天機器人設計，讓聊天機器人能夠針對使用者口語對話內容執行轉為文字之後的自然語言處理，例如：斷詞、特徵擷取、意圖分類及實體擷取任務；而人類的心理感受任務有「情緒偵測」、「情感分析」、「正向鼓舞」及「關心/同理心」。
接著，以Cognitive Behavioral Therapy (CBT)與Motivational Interviewing (MI)心理健康方法設計聊天機器人，使聊天機器人具有辨識負面心理健康認知及回覆心理健康處理方案的能力。
最後，除了Rasa Policy原有的MemoizationPolicy、RulePolicy及TEDPolicy工具，本研究另外設計Custom Graph Components的MentalHealthPolicy，其主要用於參考過去使用者的事件體驗來影響Rasa Policy的對話決策，針對相同的負面心理健康認知調用適當正向心理健康管理對話的方法，讓聊天機器人更能夠適應多變的對話情境，從使用者的角度更能夠接受聊天機器人的說話內容。

聊天機器人使用心理健康方法的對話核心框架

![image](https://user-images.githubusercontent.com/131113658/233013704-06dd173e-3e70-4fc6-a16a-cfc1b9917a0c.png)

聊天機器人使用自然語言處理使用者對話

![image](https://user-images.githubusercontent.com/131113658/233013295-84f34b3c-c547-494e-9069-3dde726676b3.png)

Custom Graph Components示意圖

![image](https://user-images.githubusercontent.com/131113658/233013785-e84b3092-1b9d-4f98-af28-fad7c0abf97f.png)

Rasa執行結果圖

![image](https://user-images.githubusercontent.com/131113658/233013185-b25dbf86-c012-4943-98f8-a8e0ce33ff69.png)

Rasa執行自然語言處理的系統介面

使用Postman工具展示Application Programming Interface(API)

![image](https://user-images.githubusercontent.com/131113658/233014795-1d2bd746-d6d0-4c69-a7d8-3ddc2dc28acf.png)



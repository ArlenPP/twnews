台灣新聞拆拆樂的用來蒐集或處理大眾感興趣的資訊，目前著重在新聞和市場情報，希望能藉由這個工具讓其他人變出各種好玩的衍生應用，目前提供這些功能：

* 將新聞網頁拆出標題，內文，報導時間，記者
* 關鍵字查新聞，並且可接續拆新聞或新聞數
* 蒐集三大法人，信用交易，借券賣出，股權分散表等市場資訊

## 為什麼做這個？

最早的開發動機，是希望能做個工具能快速找到最新的凶宅，用來輔助我的另一個專案[鄉民風水師](https://geomancer.tacosync.com/)，實現資料自動更新，所以做了拆站工具和搜尋爬蟲。做了一段時間也開始有話題性，就修了一些大家反應的問題。然後希望維護這專案的負擔不要太重，又寫了一些能發財的東西，然後就變成現在的樣子。如果想了解更多以前的事，可以參考[版本異動紀錄](docs/changelog.md)。

如果你是來找發財工具，另一個乏人問津的專案[群益證券聽牌機](https://github.com/virus-warnning/skcom)也歡迎來關注一下。 

## 怎麼用？

**系統需求**

* OS: 不限
* Python: 3.5 ~ 3.7

**安裝**

```sh
# Windows (只有 Python 3.x 的環境)
pip install twnews

# macOS, Linux (Python 2.x 與 3.x 並存的環境)
pip3 install twnews
```

**體驗**

為了方便有緣人使用，開發了一些 console 工具讓人可以不用寫程式就立即體驗

例如朝聖一則凶宅新聞：

```bash
python3 -m twnews soup https://www.setn.com/News.aspx?NewsID=490688&From=Search&Key=%E5%8F%B0%E4%B8%AD%E6%9C%80%E7%8C%9B%E5%85%87%E5%AE%85%EF%BC%81%E9%80%A36%E5%90%8D%E6%88%BF%E5%AE%A2%E5%90%8C%E4%BD%8D%E7%BD%AE%E4%B8%8A%E5%90%8A
---------------------------------------------------------------------------
原始路徑: https://www.setn.com/News.aspx?NewsID=490688
最終路徑: https://www.setn.com/m/news.aspx?newsid=490688
頻道: setn
標題: 堪稱台中最猛兇宅！連續6名房客上吊　竟都死在相同位置
日期: 2019-02-07 20:00:00
記者: 林盈君
內文:
記者林盈君／台中報導許多人不論是租屋、購屋，都擔心會碰上兇宅，有位職業為房仲的網友，就在PTT上，分享他曾經遇過的詭異事件！
他說約在幾年前，接到一個同行介紹的案子，是一間位於台中沙鹿的頂樓老公寓，當時他看到房屋價格時，簡直低到讓他不敢相信，詢問過
屋主之後，屋主表示屋內曾有人上吊死亡，而且是「連續6名房客」，且竟然都在「同一位置」選擇輕生！▲該公寓曾發生6名租客上吊事件
。（圖／示意圖／翻攝pixabay）據悉，幾年前曾有一名房客，在屋內上吊自殺，屋主之後請了法師來超渡誦經，就低價再次租給其他房客
，不料6個月後，該房客卻遲遲沒有交租金，就連簡訊電話都無回應，他只好請警察協助開門，沒想到進到屋內就發現，房客已經上吊死亡
，而且死亡的位置，跟第一個房客上吊的地方「一模一樣」，實在令人毛骨悚然。▲許多人認為這根本是「抓交替」。（圖／示意圖／翻攝
pixabay）在那之後，屋主連續租給其他幾位房客，但卻頻頻發生意外，6位租客全都選擇在屋內上吊自殺，上吊的位置也全部一模一樣，
這樣詭異的情況，也讓轄區員警懷疑，屋主是不是殺害租客後，用上吊來掩蓋罪行，讓屋主相當崩潰！屋主曾無奈表示「1、2個就算了，是
連續6個租客你知道嗎？」、「這6個租客我根本不知道為什麼他們最後都上吊死了，而且上吊的位置全都一模一樣」。更加詭異的是，連續
6名房客上吊身亡後，屋主有2年多都沒再把房子出租，屋內空無一人，但對面鄰居卻跟他表示，看到有人進出他的房子，樓下的住戶也說，
上面常常傳來很用力踩地板、拖著椅子及摔東西的聲音，甚至連一樓的住戶，都說看到房子的陽台上有人，但等到屋主拿鑰匙進屋查看時，
發現從門口到陽台都是厚厚的灰塵，完全沒有任何人走動的跡象。因為發生過命案，再加上接連詭異的情況，讓對面鄰居和樓下住戶都陸續
搬走，也有房仲找投資客來看房，但大家都覺得這房子太邪門，認為根本是「抓交替」。後來有位投資客表示意願想買，但到簽約當天屋主
卻反悔，表示不想讓對方成為上吊身亡的「第七個人」，所以直到現在，那間房子依然空在那裡，也沒有其他房客入住。
★ 三立新聞網提醒您：勇敢求救並非弱者，生命一定可以找到出路。透過守門123步驟-1問2應3轉介，你我都可以成為自殺防治守門人。
※ 安心專線：0800-788-995（0800-請幫幫-救救我）
※ 張老師專線：1980
※ 生命線專線：1995
※ 反霸凌專線：0800-200-885
有效內容率: 2.16%
---------------------------------------------------------------------------
```

## 深入了解

TODO

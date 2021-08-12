---
tags: Golang魔法使
---
# \#1 Golang魔法使──安裝與建置環境 | Golang魔法使

## 前言

![](https://i.imgur.com/PPaIS5L.jpg)

小櫻，本名本之本櫻，就讀友枝國小四年級，哥哥木之本桃矢就讀星條高中二年級。星條高中位於友枝國小的旁邊。小櫻溜直排輪去上學，路上常常會遇到哥哥的同班同學兼好朋友──月城雪兔！小櫻非常喜歡雪兔，每天都會發春

小櫻和哥哥、爸爸生活在一起，小櫻的母親在小櫻年幼時就去世(~~其實是去找石鬼面~~)。這一天放學後小櫻獨自一個人回到家，小櫻的爸爸是大學考古學教授(~~正在研究石鬼面~~)，而哥哥桃矢為了分擔家技常常打工。和往常一樣，小櫻一個人在家中。這天，家裡的地下室傳來異音，於是小櫻鼓起勇氣走進地下室！殊不知，有一本叫做 Go Language 的書竟然發起了光，正當小櫻打開這本書的一瞬間，一隻藍色的布偶突然衝了出來！

![](https://i.imgur.com/LRjGSOf.jpg)


這隻藍色土墢鼠(~~原著是黃色有翅膀鼠類~~)叫可魯貝洛斯 aka 小可，而書中放著許多卡牌叫做 Golang 牌，小可是這本書的封印之獸，負責管理這些 Golang 牌，如今卻因為他的一時疏忽導致 Golang 牌四散，不知所措的他，找了三兩句藉口要小櫻當 Golang 魔法使(~~根本是袂生牽拖厝邊~~)，螢幕前的小伙伴為了支配小櫻！一起來把 Golang 牌封印起來吧！

(蛤？你說你比較想支配知世？也不是不行)

## 成為 Golang 魔法使

在正式成為 Golang 魔法使前，一定要有一些裝備，就像小櫻手上的魔仗可以吸收卡牌~~有時也可以做物理超渡~~，生為小櫻的工具人，你必需先前往 Go 的官網下載安裝 Go [https://golang.org](https://golang.org/)

安裝 Go 後，必需設置環境變數！第一次當工具人的朋友，可能不知道什麼是 __環境變數__ ，簡單來說為了讓 windows 能把 Golang 牌(.go) 轉成物理攻擊 (.exe) ，那究竟要去哪裡才能設置環境變數呢？首先先右鍵點擊「本機(我的電腦)」>「內容」> 「進階系統設定」>「環境變數」
![](https://i.imgur.com/WXcKbEk.png)

![](https://i.imgur.com/YzR961P.png)

![](https://i.imgur.com/sm8rI1o.png)

![](https://i.imgur.com/YH4NSnq.png)


此時會出現上下兩個欄位，上方欄位稱為「使用者變數」下方欄位稱為「系統變數」，如果在「使用者變數」進行設置，那麼這台電腦上只有自己可以使用 Go，如果是「系統變數」，則這台電腦的使用者都可以使用 Go。

那麼怎麼設置呢？Golang的環境變數設置有分成兩種版本，我只會講新版本的部分也就是 v1.11 之後，如果各位下載的是最新版那就沒問題，載到舊版本的趕快重裝，當工具人請跟上時代。

### 設定 PATH

如果你在安裝時沒有特別更改路徑，那麼 Go 將會預設安裝在 `C:\Go` 的位址，如果你手賤亂改，那麼請找出你當出安裝的地方，並找到`bin`這個資料夾。在「使用者變數欄位」或「系統變數」欄位中`Path`的地方，按「編輯」進入後，會有很多條列的路徑，點選右側欄位中的「新增」，來新增路徑，鍵入`C:\Go\bin` ，如果是自己選的安裝路徑請依此類推

![](https://i.imgur.com/53YpvHd.png)

![](https://i.imgur.com/zllKwIZ.png)


### 設定 GOROOT

`Root` 就是根的意思，設定這個變數也是用來告訴你的電腦 Go 安裝在哪裡。這個`GOROOT`不是在`Path`裡設定，而是額外新增一個。回到有「使用者變數」和「系統變數」那個設定頁面，這次不找`Path`而是直接按新增

![](https://i.imgur.com/c81F8uY.png)


現在請打開「命令提示字元」來看看是否有綁定成功，要怎麼叫出命令提示字元？很簡單，只要右鍵點擊螢幕最左下角的 windows 旗幟並選擇「命令提示字元」就有了，如果不行，可以點選「windows 旗幟右邊或更右邊的搜尋」並輸入`cmd` (command line 的簡稱)

![](https://i.imgur.com/mb6VN6j.png)


開啟後輸入

```shell
go
```

如果跳出一堆英文就代表你安裝成功了，如果沒有，可以試著重新開機，基本上 90% 沒屁用。

![](https://i.imgur.com/mMRV0nQ.png)


---

其他教學文

>
> [Go 語言於 Windows 上之安裝與環境設定](https://oranwind.org/go-go-yu-yan-yu-windows-shang-zhi-an-zhuang-yu-huan-jing-she-ding/) 有附彩圖很用心
> 
> [Go的三种安装方式](https://github.com/astaxie/build-web-application-with-golang/blob/master/zh/01.1.md) 包含linux, mac 等
>  
> [Getting Started - The Go Programming Language](https://golang.org/doc/install) 官方的教學
> 
> [Go言語のインストールとhello worldを表示する(Windows10) | ITSakura](https://itsakura.com/go-install) 日文的安裝教學，有附彩圖很用心，但是他是安裝在 D 槽，建議安裝在 C 槽我比較好教
> 

## 第 1 課 ── 向世界問好！

進入 notepad 或 [notepad++](https://notepad-plus-plus.org/downloads/) 後我們直接先複製以下的 code

```go
package main
import "fmt"
func main(){
    fmt.Println("Hello world! I want to be a golangcaptor")
}
```

![](https://i.imgur.com/HhAhSWT.png)

接著開啟麥克風對著電腦喊

> 隱藏著黑暗力量的鑰匙啊，在我面前顯示你真正的力量！現在以你的主人，「*說你的名字*」 之名命令你——封印解除！

電腦沒有反應，~~因為你要用日文喊~~

我們要用命令提示字元來編譯 code

![](https://i.imgur.com/6TTO8Cd.png)
↑先把路徑複製下來

進入命令提示字元，這時命令提示字元上面會有路徑，如果你存的路徑跟命令提示字元上的路徑都在C槽，那太好了，我們直接鍵入(如果資料夾設在D槽，而命令字提示字元還在C槽，那你可以先打 `D:` 讓命令提示字元指向 D 槽)


```sh
cd 路徑
```

![](https://i.imgur.com/ypZjVD6.png)


接著開啟麥克風對著電腦喊

> 無主之物啊，匯聚於夢之杖，成為我的力量吧！Secure！

電腦沒有反應，~~因為你沒開麥克風~~

```sh
go run lesson01.go
```

![](https://i.imgur.com/OXzLhsn.png)


但是不是稍微有一些麻煩呢？沒錯，因此，下一堂課會教大家更快執行庫洛牌的方法！


> **進階操作小補充**
> 
> 除了用 `go run` 直接執行，也可以使用 `go build` 將 `.go` 編譯成 `.exe`

---

## 後記

2020 年寫的太尬了，所以 2021 有稍微再更新一下 :smile: 

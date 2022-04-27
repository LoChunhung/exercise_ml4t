# exercise_ml4t
exercise for book machine learning for algorithm tradming.
# 閱讀書籍之前，部分必須要做的事
## 1. 安裝zip-line reload
## 1.1 解決範例執行環境問題:
### Q1. 作者建議在windows環境下，使用anaconda來做為安裝管理程式，但後續提到2021後由於相依性問題，需使用指定的語法
    Ans: 網站建議安裝參考網址: https://github.com/stefan-jansen/zipline-reloaded
### Q2. 按照安裝指令後出現錯誤?
    Ans: 錯誤有多種，僅能提供遭遇的狀況，請注意這是建立全新的python 3.8.13後的問題，不同環境可能有不同狀況。
    **錯誤描述:**
    陸續有數個package: **exchange-calendars**, **ta-lib, bcolz-zipline, empyrical-reloaded, zipline-reloaded**
    出現如下的錯誤描述: 
    錯誤範例樣式:
    <br>
    CondaHTTPError: HTTP 404 NOT FOUND for url <https://conda.anaconda.org/ml4t/win-64/exchange-calendars-3.3-py38_0.tar.bz2> Elapsed: 00:00.296504 CF-RAY: 7022f2185d296a96-TPE
    An HTTP error occurred when trying to retrieve this URL. HTTP errors are often intermittent, and a simple retry will get you on your way.
    原因不得而知，但簡而言之就是無法正常由網路上下載，此時請改採離線安裝的方式來先將無法下載的package按順序安裝。
    <br>
    請到作者在anaconda.org channel上下載，每一個package都有自己不同的url去下載(由url可以得知)，以exchange-calendars為例
    到 https://conda.anaconda.org/ml4t/win-64/ 選擇正確的python版本 
    ![image](https://user-images.githubusercontent.com/30331982/165416879-3dffc903-92dd-4002-9783-a1d135802214.png)
    
    <>
    進到下一層連結後，由File下載正確的離線安裝檔案
    ![image](https://user-images.githubusercontent.com/30331982/165417020-604758df-4931-44a5-91c6-d0bef2d8618c.png)

    將自己遭遇到的retrieve error package都下載完畢後，
    切換到專用於Machine Learning for Algorithm Tradming的Python虛擬環境
    然後逐個執行以下的指令，範例如下 
    conda install _exchange-calendars-3.3-py38_0.tar.bz2_ 
    所有HTTP error的package都安裝後，再重新執行一次
   ** conda install -c ml4t -c conda-forge -c ranaroussi zipline-reloaded**
   指令，就可以完成作者辛苦重新製作的環境

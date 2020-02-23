---
layout: post
title: "香港銀行開放API"
date: 2019-01-31 18:20:43 +0800
comments: true
categories:
---
前兩天看新聞，欣聞香港本地銀行開始開放API供第三方調用，新聞詳見鏈結
[本地四大銀行開放API 涉逾170項資料](https://news.mingpao.com/pns/%E7%B6%93%E6%BF%9F/article/20190129/s00004/1548698910101/%E6%9C%AC%E5%9C%B0%E5%9B%9B%E5%A4%A7%E9%8A%80%E8%A1%8C%E9%96%8B%E6%94%BEapi-%E6%B6%89%E9%80%BE170%E9%A0%85%E8%B3%87%E6%96%99,本地四大銀行開放API 涉逾170項資料)，就上網找尋一番，中銀剛開始一直沒找到他的API開發者網站，不過經過一番努力，則都順利找到，網址如下

- [匯豐開發者網站](https://developer.hsbc.com.hk )
- [渣打開發者網站](https://axess.sc.com/)
- [中銀開發者網站](https://api.bochk.com/)
- [恆生開發者網站](https://developer.hangseng.com/)

還有一個銀通的APIX

- [銀通的開發者網站](https://sandboxportal.apix.com.hk/jetco/sb/)


粗略的看了一下，現階段提供的API都還比較初級，匯豐HSBC、恆生還只提供英文版的信息，香港還是看中文的多吧，中銀則英文中文都有


![API截圖](/img/bocapi1.png "API截圖")

中銀還給了四種開發語言的示例代碼，匯豐恆生暫時沒有示例代碼

不過我試了一下BOC的API，在Auth獲取access token環節就卡住了，用post man經常返回

	<l7:policyResult status="Assertion Falsified" xmlns:l7="http://www.layer7tech.com/ws/policy/fault"/>

的錯誤，後來又莫名奇妙的可以返回access token，但是在使用access token獲取資源的時候又一直返回

	{
    "ErrorMsg": "Access tohen expired or invalid"
	}
一直沒法繼續測試API。

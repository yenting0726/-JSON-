
# 臺南市噪音監測站監測數據

## 介紹
本專案提供臺南市噪音監測站的監測數據，透過網頁介面展示資料，並允許使用者動態抓取和刪除數據。

## 資料來源
- 資料集連結: [臺南市噪音監測站監測數據](https://data.gov.tw/dataset/101813)

## 功能
1. **抓取資料**: 使用者可透過按鈕從 API 抓取噪音監測數據。
2. **顯示資料**: 抓取的數據將以表格形式顯示。
3. **刪除功能**: 使用者可刪除不需要的數據行。

## 使用技術
- HTML
- CSS (Bootstrap)
- JavaScript (jQuery)

## 使用方法
1. 打開 `index.html` 檔案。
2. 點擊「抓資料到表格」按鈕以載入監測數據。
3. 使用「刪除」按鈕移除不需要的資料行。

## 程式碼說明
以下是主要的 JavaScript 功能描述：
- **資料抓取**:
  ```javascript
  $.get(url1, function(data, status){   
      // 處理抓取的數據
  });
  ```
- **資料顯示**:
  ```javascript
  let table=`
      <tr>
          <td>${row.Seq}</td>
          ...
      </tr>
  `;
  $("#tbody1").append(table);
  ```
- **刪除功能**:
  ```javascript
  $(".del").click(function(){ 
      $(this).parents("tr").remove();
  });
  ```

## 注意事項
- 確保在支持 JavaScript 的瀏覽器中運行此程式碼。
- 由於使用了外部 API，請確認網路連接正常。

## 貢獻
歡迎任何形式的貢獻，請提出問題或提交拉取請求。

---


Quá trình xử lý dữ liệu và phân tích dữ liệu được thực hiện trên Power Bi Destop.

## Xử lý dữ liệu

| STT  | Cột | Mô tả vấn đề | Phân loại | Cách giải quyết |
| ------------- | ------------- | ------------- |------------- | ------------- |
| 1  | Marital_Status |Xuất hiện giá trị "Absurd", "YOLO" | Inconsistent values | Thay thế bằng "N/A"  |
| 2  | Marital_Status | Các cặp giá trị tương đồng "Alone" - "Single" và "Married" - "Together" | Inconsistent values  | Thay thế "Alone" thành "Single" và "Together" thành "Married"  |
| 3  | Income | Format là Whole number | currency format | Chuyển thành currency R$, decimal = 2 |
| 4  | Education | Cặp giá trị tương đồng "2n Cycle" - "Master", giá trị không rõ nghĩa "Basic", "Graduation" | Inconsistent values | Thay thế cặp giá trị tương đồng thành "Master's", "Graduation" -> "Bachelor's", "Basic" -> "Below High School"|
| 5  | Year_Birth | Năm sinh là 1893, 1899 và 1900 | illogical | Xóa hàng |
| 6 | Income | 24 giá trị null | null values | Thay thế bằng median income |
| 7 | Income | Giá trị R$ 666.666 lớn hơn hẳn so với giá trị lớn thứ 2 (R$ 162.397) | outlier | Loại bỏ |

Tạo cột mới cho bins 

Income_Level
= 

Unpivot column

## Phân tích dữ liệu

Create 2 reference tables to compare customer segmentations between last and 2nd campaigns

https://www.linkedin.com/pulse/brazils-ifood-wasting-money-wrong-customers-vivek-poovathoor-m37jf?trk=public_post_main-feed-card_feed-article-content

Phân tích RFM:
https://blog.tomorrowmarketers.org/phan-tich-rfm-la-gi/
https://maestra.io/blog/marketing/rfm-analysis/

Chia RFM thành 3 khoảng

Vì không có dữ liệu liên quan đến Order_Date nên phân tích RFM tập trung vào 2 giá trị Recency và Monetary.
https://hptpedia.hyper-trade.com/rm-analysis/
https://maestra.io/blog/marketing/rfm-analysis/

| Recency  | Monetary | 
| ------------- | ------------- | 
| 1 - Gần đây nhất | 1 - Chi tiêu cao nhất | 
| 2 - Trung bình | 2 - Trung bình |
| 3 - Ít gần đây nhất | 3 - Chi tiêu thấp nhất |

| RFM_Score  | Segment | 
| ------------- | ------------- | 
| 11  | Champion | 
| 12  | Loyal |
| 21  | Potential Loyalist |
| 13  | Recent |
| 22  | Needing Attention |
| 32  | At Risk |
| 31  | Can't Lose Them |
| 23  | Hibernating |
| 33  | Lost |


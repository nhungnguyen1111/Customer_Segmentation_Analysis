Quá trình xử lý và phân tích dữ liệu được thực hiện trên Power Bi Destop.

## Xử lý dữ liệu

| STT  | Cột | Mô tả vấn đề | Phân loại | Cách giải quyết |
| ------------- | ------------- | ------------- |------------- | ------------- |
| 1  | Marital_Status | Xuất hiện giá trị "Absurd", "YOLO" | Inconsistent values | Thay thế bằng "N/A"  |
| 2  | Marital_Status | Các cặp giá trị tương đồng "Alone" - "Single" và "Married" - "Together" | Inconsistent values  | Thay thế "Alone" thành "Single" và "Together" thành "Married"  |
| 3  | Income | Format là Whole number | currency format | Chuyển thành currency R$, decimal = 2 |
| 4  | Education | Cặp giá trị tương đồng "2n Cycle" - "Master", giá trị không rõ nghĩa "Basic", "Graduation" | Inconsistent values | Thay thế cặp giá trị tương đồng thành "Master's", "Graduation" -> "Bachelor's", "Basic" -> "Below High School"|
| 5  | Year_Birth | Năm sinh là 1893, 1899 và 1900 | illogical | Xóa hàng |
| 6 | Income | 24 giá trị null | null values | Thay thế bằng median income |
| 7 | Income | Giá trị R$ 666.666 lớn hơn hẳn so với giá trị lớn thứ 2 (R$ 162.397) | outlier | Loại bỏ |

## Phân tích dữ liệu

**Tính tuổi**

- Quy ước năm hiện tại để tính tuổi là 2014
- Add custom column:
  ```
  Age = 2014 - [YearBirth]
  ```

**Tạo Income level**

Add conditional column:
![{B98FF1C1-25CD-4DDA-84AC-57453D7D9A74}](https://github.com/user-attachments/assets/75806b63-81e5-4953-89ea-93bf495b25f0)

**Tạo Age level**

Add conditional column:
![{F3457E19-8C66-46D0-8F0B-B1CE485E6693}](https://github.com/user-attachments/assets/d734e0e3-5373-4a11-860c-27783b9f06c2)

**Tính Product_Amount**

- Mục đích: tính giá trị giao dịch mỗi sản phẩm ứng với mỗi khách hàng
- Từ bảng gốc iFood tạo reference table cho ra bảng Product
- Thực hiện unpivot column với cột MntWines, MntFruits, MntMeatProducts, MntFishProducts và MntSweetProducts
  - Kết quả cho bảng mới là Product và Product_Amount
![{0FBCBD60-B415-4DC3-9340-8C8B5DBCE4E2}](https://github.com/user-attachments/assets/4d1fad29-f914-4223-a968-3cf97f1a754b)

**Phân tích RFM**

https://blog.tomorrowmarketers.org/phan-tich-rfm-la-gi/
https://maestra.io/blog/marketing/rfm-analysis/

Chia RFM thành 3 khoảng

Vì không có dữ liệu liên quan đến Order_Date để tính Frequency nên phân tích RFM tập trung vào 2 giá trị Recency và Monetary.
https://hptpedia.hyper-trade.com/rm-analysis/

Xếp hạng Recency và Monetary như các bảng dưới đây:

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


Quá trình xử lý dữ liệu và phân tích dữ liệu được thực hiện trên Power Bi Destop.

## Xử lý dữ liệu

| STT  | Cột | Mô tả vấn đề | Phân loại | Cách giải quyết |
| ------------- | ------------- | ------------- |------------- | ------------- |
| 1  | Marital_Status |Xuất hiện giá trị "Absurd", "YOLO" | Inconsistent values | Thay thế bằng "N/A"  |
| 2  | Marital_Status | Các cặp giá trị tương đồng "Alone" - "Single" và "Married" - "Together" | Inconsistent values  | Thay thế "Alone" thành "Single" và "Together" thành "Married"  |
| 3  | Income | Format là Whole number | currency format | Chuyển thành currency R$, decimal = 2 |
| 4  | Education | Cặp giá trị tương đồng "2n Cycle" - "Master", giá trị không rõ nghĩa "Basic", "Graduation" | Inconsistent values | Thay thế cặp giá trị tương đồng thành "Master's", "Graduation" -> "Bachelor's", "Basic" -> "Below High School"|

## Phân tích dữ liệu

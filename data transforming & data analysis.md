Quá trình xử lý dữ liệu và phân tích dữ liệu được thực hiện trên Power Bi Destop.

## Xử lý dữ liệu

| STT  | Cột | Mô tả vấn đề | Phân loại | Cách giải quyết |
| ------------- | ------------- | ------------- |------------- | ------------- |
| 1  | Marital_Status |Xuất hiện giá trị "Absurd", "YOLO" | Inconsistent values | Thay thế bằng "N/A"  |
| 2  | Marital_Status | 2 giá trị tương đồng "Alone" - "Single" và "Married" - "Together" | Inconsistent values  | Thay thế "Alone" thành "Single" và "Together" thành "Married"  |
| 3  | Income | Data type là text | Data type | Thay thế bằng "N/A"  |

## Phân tích dữ liệu

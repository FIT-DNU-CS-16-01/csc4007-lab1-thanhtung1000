# Great Expectations — Validation Summary
- evaluated_expectations: 6
- successful_expectations: 5
- unsuccessful_expectations: 1
- success_percent: 83.33333333333334

## Kết luận
- GE FAIL.

## Fail cái gì?
- Fail 1 expectation kiểm tra độ dài cột len_chars trong khoảng [1, 10000].
- Có 6 mẫu vượt ngưỡng max_value=10000.

## Kế hoạch xử lý
- Chuẩn hóa độ dài review quá dài (truncate hoặc chunk).
- Chạy lại GE sau khi xử lý để đảm bảo toàn bộ expectations PASS trước khi huấn luyện chính thức.

# Metadata Register - Verified / Estimated / To be measured

## Verified
- Quy mô dữ liệu: n_rows=50000 (outputs/datacard_stats.json).
- Phân bố nhãn: label 0=25000, label 1=25000 (outputs/datacard_stats.json).
- Độ dài văn bản: min=32, median=954, p95=3328, max=13593 (outputs/datacard_stats.json).
- Split: train=40000, val=5000, test=5000 (outputs/datacard_stats.json).
- Duplicate: exact_dup_count=832, exact_dup_ratio=0.01664 (outputs/datacard_stats.json, outputs/logs/audit_after.md).
- Kết quả Great Expectations: FAIL, success_percent=83.33, fail 1 expectation len_chars (outputs/ge/validation_summary.md, outputs/ge/validation_result.json).
- Cleanlab: suspected_label_issues_count=1003, ratio=0.02006, export_top_k=200 (outputs/datacard_stats.json, outputs/logs/cleanlab_summary.md).
- HTML artifacts sau xử lý: contains_br_tag_count=0, contains_any_html_tag_count=0, contains_html_entity_count=11 (outputs/datacard_stats.json, outputs/logs/audit_after.md).

## Estimated
- Mức ảnh hưởng của duplicate lên điểm đánh giá: ước tính trung bình, cần thí nghiệm ablation để xác nhận.
- Tỷ lệ sai nhãn thực tế toàn tập: ước tính gần mức Cleanlab gợi ý (~2%), chưa có review thủ công diện rộng.
- Mức độ bias theo phong cách viết/độ dài: có khả năng tồn tại, chưa định lượng chính thức.

## To be measured
- Near-duplicate trên toàn bộ tập (không chỉ sample).
- Tỷ lệ rò rỉ xuyên split sau deduplicate bằng hash text.
- So sánh metric trước/sau sửa nhãn top nghi vấn Cleanlab.
- Đánh giá lỗi theo bucket độ dài review (ngắn/vừa/dài).
- Độ ổn định kết quả theo nhiều seed huấn luyện.

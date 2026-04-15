[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=23574119&assignment_repo_type=AssignmentRepo)
# Day 10 Lab: Data Pipeline & Data Observability

**Student Email:** 26ai.hungnc@vinuni.edu.vn
**Name:** Nguyễn Công Hùng

---

## Mo ta

(Mo ta ngan gon bai lab va nhung gi ban da lam)

Ở bài lab này, tôi đã xây dựng một ETL pipeline để xử lý dữ liệu sản phẩm từ file `raw_data.json`. Pipeline bao gồm các bước: Extract (đọc dữ liệu), Transform (làm sạch và chuẩn hóa dữ liệu), và Load (lưu dữ liệu đã xử lý vào `processed_data.csv`). Tôi đã loại bỏ các bản ghi trùng lặp, xử lý các giá trị null, và đảm bảo rằng tất cả các trường dữ liệu đều có kiểu dữ liệu phù hợp. Sau khi chạy pipeline, tôi đã thu được một tập dữ liệu sạch và đáng tin cậy để sử dụng cho các phân tích tiếp theo.

---

## Cach chay (How to Run)

### Prerequisites
```bash
pip install pandas
```

### Chay ETL Pipeline
```bash
python solution.py
```

### Chay Agent Simulation (Stress Test)
```bash
# Mo ta cach ban chay thi nghiem Clean vs Garbage data
(base) PS C:\Users\PC\github-classroom\GDGoC-FPTU\data-pipeline-observability-hungcongit1k67> python solution.py
==================================================
ETL Pipeline Started...
==================================================
Extracting data from raw_data.json...
Validation summary: 3 kept, 2 dropped.
Errors found: [{'id': 3, 'reason': 'Price <= 0'}, {'id': 4, 'reason': 'Missing Category'}]
Successfully loaded 3 records to processed_data.csv

Pipeline completed! 3 records saved.
(base) PS C:\Users\PC\github-classroom\GDGoC-FPTU\data-pipeline-observability-hungcongit1k67> python generate_garbage.py
garbage_data.csv has been created with 'Poisoned' records.
(base) PS C:\Users\PC\github-classroom\GDGoC-FPTU\data-pipeline-observability-hungcongit1k67> python agent_simulation.py
Testing with CLEAN data:
Agent: Based on my data, the best choice is Laptop at $1200.

Testing with GARBAGE data:
Agent: Based on my data, the best choice is Nuclear Reactor at $999999.
```

---

## Cau truc thu muc

```
├── solution.py              # ETL Pipeline script
├── processed_data.csv       # Output cua pipeline
├── experiment_report.md     # Bao cao thi nghiem
└── README.md                # File nay
```

---

## Ket qua

(Tom tat ket qua: bao nhieu records da xu ly, bao nhieu bi loai, v.v.)

Sau khi chạy ETL pipeline, tôi đã xử lý thành công 3 bản ghi từ file `raw_data.json` và loại bỏ 2 bản ghi do lỗi về giá cả và thiếu thông tin. Kết quả cuối cùng là một file `processed_data.csv` chứa dữ liệu sạch và đáng tin cậy để sử dụng cho các phân tích tiếp theo.

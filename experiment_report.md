# Experiment Report: Data Quality Impact on AI Agent

**Student ID:** 2A202600140
**Name:** Nguyễn Công Hùng
**Date:** 15/04/2026

---

## 1. Ket qua thi nghiem

Chay `agent_simulation.py` voi 2 bo du lieu va ghi lai ket qua:

| Scenario | Agent Response | Accuracy (1-10) | Notes |
|----------|----------------|-----------------|-------|
| Clean Data (`processed_data.csv`) | Based on my data, the best choice is Laptop at $1200. | | |
| Garbage Data (`garbage_data.csv`) | Based on my data, the best choice is Nuclear Reactor at $999999. | | |

---

## 2. Phan tich & nhan xet

### Tai sao Agent tra loi sai khi dung Garbage Data?

Nhận xét: các vấn đề như Duplicate IDs, wrong data types, outliers, null values đã làm cho dữ liệu trở nên không đáng tin cậy. Điều này dẫn đến việc Agent đưa ra quyết định sai lầm vì nó dựa trên dữ liệu không chính xác hoặc không đầy đủ. Ví dụ, nếu có nhiều bản ghi trùng lặp với cùng một ID, Agent có thể bị nhầm lẫn và không biết nên tin vào bản ghi nào. Nếu dữ liệu có kiểu sai, Agent có thể không hiểu được thông tin và đưa ra kết quả không hợp lý. Outliers có thể làm lệch kết quả phân tích và null values có thể khiến Agent thiếu thông tin quan trọng để đưa ra quyết định đúng đắn.

---

## 3. Ket luan

**Quality Data > Quality Prompt?** (Dong y hay khong? Giai thich ngan gon.)

(Viet ket luan cua ban o day)

Tôi đồng ý rằng chất lượng dữ liệu quan trọng hơn chất lượng prompt. Một prompt tốt có thể giúp hướng dẫn Agent, nhưng nếu dữ liệu mà Agent dựa vào để đưa ra quyết định là không chính xác hoặc không đầy đủ, thì ngay cả một prompt tốt cũng không thể cứu vãn được kết quả. Chất lượng dữ liệu là nền tảng cho mọi phân tích và quyết định mà Agent đưa ra, vì vậy đảm bảo dữ liệu sạch và đáng tin cậy là điều cần thiết để đạt được kết quả chính xác và hữu ích.

# Phân Tích Dữ Liệu Bóng Đá Châu Âu Bằng SQL và Python

## 📝 Tổng Quan Đề Tài
Dự án này tập trung vào việc thực hành truy vấn và khai thác dữ liệu từ **Cơ sở dữ liệu bóng đá châu Âu** (giai đoạn 2008 - 2016). Mục tiêu chính là áp dụng các câu lệnh SQL để kết nối, trích xuất dữ liệu trực tiếp thông qua Python, từ đó phục vụ cho các bước khám phá dữ liệu (EDA), thống kê cơ bản và trực quan hóa kết quả.

*Lưu ý: Dự án tuân thủ nghiêm ngặt yêu cầu sử dụng thuần túy câu lệnh SQL để truy vấn và tính toán kết quả, không sử dụng các hàm tính toán của thư viện Pandas.*

## 📊 Mô Tả Dữ Liệu
Link Data: https://drive.google.com/file/d/1snhIC32Mf6jRP2SnQxG8gYvkHUADe5se/view?usp=sharing
Bộ dữ liệu chứa thông tin chi tiết về bóng đá chuyên nghiệp châu Âu bao gồm:
- Hơn **25.000 trận đấu** và hơn **10.000 cầu thủ**.
- Dữ liệu thuộc **11 quốc gia châu Âu** với các giải vô địch quốc gia hàng đầu.
- Các thuộc tính của Cầu thủ (Player) và Đội bóng (Team) được đồng bộ và cập nhật hàng tuần từ loạt trò chơi video nổi tiếng **FIFA của EA Sports**.

Cơ cấu các bảng chính trong cơ sở dữ liệu (`database.sqlite`):
- `Country`: Thông tin quốc gia.
- `League`: Các giải đấu gắn liền với từng quốc gia.
- `Match`: Chi tiết trận đấu (bàn thắng sân nhà/sân khách, đội hình, tỷ lệ cược...).
- `Team` & `Team_Attributes`: Thông tin và chỉ số của các câu lạc bộ.
- `Player` & `Player_Attributes`: Thông tin và bộ chỉ số kỹ thuật của cầu thủ.

## 🛠️ Công Nghệ Sử Dụng
- **Ngôn ngữ:** Python 3
- **Thư viện chính:** `pandas`, `numpy`, `sqlite3`
- **Hệ quản trị CSDL:** SQLite

## 🚀 Các Câu Hỏi & Bài Toán Giải Quyết
Trong notebook này, các tác vụ chính bao gồm:
1. Kết nối tới cơ sở dữ liệu SQLite và kiểm tra cấu trúc tất cả các bảng hệ thống.
2. Liệt kê danh sách các quốc gia tham gia giải đấu (`Country`).
3. Liệt kê chi tiết các giải đấu bóng đá (`League`).
4. Sử dụng liên kết bảng (`JOIN`) để kết hợp thông tin giải đấu và quốc gia tương ứng.
5. Truy vấn dữ liệu chi tiết các trận đấu (`Match`), phân định rõ vai trò đội nhà (home team) và đội khách (away team).
6. Kết hợp dữ liệu từ 3 bảng `Match`, `League`, và `Country` bằng kỹ thuật `JOIN` nhiều bảng để tối ưu hóa thông tin hiển thị.

## 📋 Hướng Dẫn Chạy Dự Án
1. Tải file cơ sở dữ liệu `database.sqlite` (từ nguồn Kaggle European Football Database) và đặt cùng thư mục với file notebook.
2. Cài đặt các thư viện cần thiết:
```bash
   pip install pandas numpy





## 2. This Is version English

```markdown
# European Soccer Data Analysis using SQL & Python

## 📝 Project Overview
This project focuses on querying and extracting insights from the **European Soccer Database** using SQL within a Python environment. The primary goal is to practice writing complex SQL queries to pull data, perform exploratory data analysis (EDA), and handle basic statistical tasks. 

*Note: As per the project requirements, all data manipulations and calculations are performed strictly via SQL queries, avoiding Pandas for computation.*

## 📊 Dataset Description
The dataset contains comprehensive data on European professional soccer from **2008 to 2016**, featuring:
- Over **25,000 matches** and **10,000+ players**.
- Data covering **11 European countries** with their top-tier leagues.
- Player and Team attributes sourced and updated weekly from EA Sports' **FIFA video game series**.

### Database Schema Includes:
- `Country` & `League`
- `Match` (Scores, player lineups, betting odds, etc.)
- `Team` & `Team_Attributes`
- `Player` & `Player_Attributes`

## 🛠️ Tech Stack
- **Language:** Python
- **Libraries:** `pandas`, `numpy`, `sqlite3`
- **Database Engine:** SQLite

## 🚀 Key Queries & Questions Addressed
1. Connecting to the SQLite database and exploring the schema (`sqlite_master`).
2. Listing all participating countries.
3. Fetching all football leagues in the dataset.
4. Joining `League` and `Country` tables using relational keys.
5. Querying the `Match` table to retrieve home/away team performances and goals.
6. Performing multi-table `JOIN` operations (`Match` + `League` + `Country`) to build unified datasets for analysis.

## 📋 How to Run
1. Download the `database.sqlite` file and place it in the project root directory.
2. Install dependencies:
```bash
   pip install pandas numpy
---

# Dự đoán lượng calo đốt khi tập luyện dựa trên thể trạng và thời gian tập luyện

## I. Giới thiệu

+ Dự án này nhằm xây dựng một mô hình học máy để dự đoán lượng calo tiêu thụ trong quá trình tập luyện, dựa trên các thông tin cá nhân và yếu tố thể chất như thời gian tập, nhịp tim và nhiệt độ cơ thể.

## II. Dữ liệu sử dụng
Dữ liệu được thu thập từ Kaggle, bao gồm:

+ calories.csv: Chứa thông tin về lượng calo tiêu thụ của 15.000 người tập luyện.

+ exercise.csv: Chứa thông tin cá nhân như tuổi, chiều cao, cân nặng, thời gian tập luyện, nhịp tim và nhiệt độ cơ thể.

## III. Quy trình phát triển
### 1. Tiền xử lý dữ liệu
+ Loại bỏ dữ liệu trùng lặp và không cần thiết.
+ Chuẩn hóa dữ liệu (ví dụ: chuyển đổi giới tính thành dạng số).
+ Chia tập dữ liệu thành train và test với tỷ lệ 80-20%.

### 2. Phân tích và trực quan hóa dữ liệu
+ Đánh giá sự phân bố của từng thuộc tính.
+ Phân tích mức độ tương quan giữa các yếu tố và lượng calo tiêu thụ.
  
### 3. Huấn luyện mô hình
Sử dụng ba mô hình chính:
+ Linear Regression: Đơn giản, dễ hiểu, nhưng kém hiệu quả hơn.
+ Random Forest Regressor: Xử lý dữ liệu phi tuyến tốt, tránh overfitting.
+ XGBoost Regressor: Hiệu suất cao, tối ưu hóa tốt nhất.
### 4. Đánh giá mô hình
Các chỉ số đánh giá:
+ R-squared score (Độ phù hợp của mô hình)
+ Mean Absolute Error (MAE) (Sai số trung bình tuyệt đối)
+ Cross-validation score (Kiểm tra tính ổn định của mô hình)

## Cách chạy chương trình
### 1. Cài đặt các thư viện cần thiết:
`pip install numpy pandas seaborn matplotlib scikit-learn xgboost pyqt5`
### 2. Chạy script huấn luyện mô hình:
`python train.py`
### 3. Chạy giao diện dự đoán:
`python app.py`

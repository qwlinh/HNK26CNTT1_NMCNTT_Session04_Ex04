# Phần 1: Phân tích & Đề xuất (So sánh 2 cách viết đường dẫn):

Dưới đây là bảng so sánh chi tiết giữa Cách 1 Đường dẫn tuyệt đối - Absolute Path và Cách 2 Đường dẫn tương đối

Tiêu chí so sánh
## 1 Tính di động (Portability):
 - Cách 1: Đường dẫn tuyệt đối (C:\Users\...):  Kém ( Bị gắn cứng theo tên máy tính và tên người dùng của An. Khi An gửi thư mục Project cho bạn bè hoặc đưa lên máy chủ khác, đường dẫn sẽ bị lỗi ngay lập tức vì cấu trúc thư mục hệ thống khác. )
 - Cách 2: Đường dẫn tương đối (../Data/...): Cao ( Các tệp và thư mục di chuyển cùng nhau mà không sợ sai lệch đường dẫn, vì đường dẫn được tính dựa trên vị trí hiện tại của file mã nguồn. )

## 2 Độ dài câu lệnh:
 - Cách 1: Đường dẫn tuyệt đối (C:\Users\...): Dài và phức tạp ( Phải gõ đầy đủ toàn bộ cây thư mục từ gốc phân vùng ổ đĩa (C:\...), dễ gây nhầm lẫn hoặc gõ sai chính tả. )
 - Cách 2: Đường dẫn tương đối (../Data/...): Ngắn gọn, dễ nhìn, dễ đọc và dễ quản lý khi cấu trúc thư mục dự án được tổ chức gọn gàng.

## 3. Tính an toàn:
 - Cách 1: Đường dẫn tuyệt đối (C:\Users\...): Thấp khi triển khai ( Rất rủi ro khi đưa mã nguồn lên môi trường Production hoặc chia sẻ nhóm (Collaboration/Teamwork) vì máy của mỗi thành viên có tên tài khoản Windows khác nhau. )
 - Cách 2: Đường dẫn tương đối (../Data/...): Cao trong dự án ( Giúp mã nguồn chạy mượt mà trên mọi thiết bị, mọi hệ điều hành khác nhau của các thành viên trong nhóm. )

# Phần 2: Lựa chọn tối ưu:
## 1. Chốt giải pháp tối ưu cho An:
 - Giải pháp tối ưu: Cách 2 (Đường dẫn tương đối - Relative Path) là lựa chọn chuẩn mực và bắt buộc trong lập trình cũng như phát triển phần mềm chuyên nghiệp. Nó giúp đáp ứng hoàn toàn quy tắc nghiệp vụ: Dự án có thể chạy trơn tru khi An gửi toàn bộ thư mục Project cho bạn bè hay đồng nghiệp (dù họ có tên User khác hoặc cài đặt ở ổ đĩa khác).
## 2. Giải thích ý nghĩa các ký hiệu trong đường dẫn tương đối:
 - Ký hiệu . (Một dấu chấm): Đại diện cho thư mục hiện tại (Current Directory) nơi tệp script đang thực thi.
 - Ký hiệu .. (Hai dấu chấm): Đại diện cho thư mục cha (Parent Directory) — nghĩa là di chuyển lùi lên trên một cấp thư mục so với vị trí hiện tại của file code (ví dụ: từ thư mục src lùi ra thư mục gốc Project để tìm tới thư mục Data).

# Mô tả
Bài tập này xây dựng một API đơn giản bằng ASP.NET Core (.NET 9.0) để quản lý một danh sách việc cần làm (to-do list). API này thực hiện các tác vụ CRUD gồm thêm/sửa/xóa thông tin công việc; truy xuất công việc và danh sách công việc.

Một database Entity Framework Core lưu trên bộ nhớ `TodoList` được sử dụng làm `DbContext` để thêm vào chương trình.

# Kết quả đạt được
Khi khởi chạy chương trình trên Visual Studio, ta có thể gửi các HTTP request để thực hiện tác vụ API từ tập tin HTTP tạo sẵn. Có 6 route API như hình dưới:

![image](https://github.com/user-attachments/assets/884ea745-42a0-4d35-96a9-7cde063d6297)

Lần lượt nhấn "Send request" theo thứ tự từ trên xuống để gửi các request:
* Thêm một to-do item (POST)
  ![image](https://github.com/user-attachments/assets/f126e266-d956-42d0-9b68-dc90c0302123)
* Lấy danh sách tất cả to-do items (GET)
  ![image](https://github.com/user-attachments/assets/a2739267-882b-40a3-8e14-41b0c0297d2f)
* Lấy to-do item theo ID (GET)
  ![image](https://github.com/user-attachments/assets/d242fb10-7ea2-48e9-a821-f330832e4316)
* Lấy danh sách to-do items đã hoàn thành (GET)
  ![image](https://github.com/user-attachments/assets/54d3fe75-393f-46c0-a482-d1c77a7e3feb)
* Sửa thông tin to-do item theo ID (PUT)
  ![image](https://github.com/user-attachments/assets/b6970f9e-6c87-439f-9c01-c96713ba760c)
  Trường hợp này sau khi sửa, khi gửi tiếp GET request để lấy tất cả items thì sẽ hiển thị item đã sửa, tuy nhiên danh sách items đã hoàn thành không chứa item nào.
  ![image](https://github.com/user-attachments/assets/dda4c5e6-0569-4ef9-8220-9071c98407e9)
  ![image](https://github.com/user-attachments/assets/d4a3adde-8344-425a-a3a5-08d6fd626b36)
* Xóa to-do item theo ID (DELETE)
  ![image](https://github.com/user-attachments/assets/b7c202ee-e39c-4645-9a7b-ba4c83e5ed57)
  Sau khi xóa, danh sách tất cả items sẽ trở lại trạng thái rỗng.
  ![image](https://github.com/user-attachments/assets/8d00b825-2bcd-4ff3-b150-8bdcd41808d1)

# Ghi chú
Mã nguồn được thực hiện có tham khảo [hướng dẫn](https://learn.microsoft.com/en-us/aspnet/core/tutorials/min-web-api?view=aspnetcore-9.0&tabs=visual-studio) của Microsoft.

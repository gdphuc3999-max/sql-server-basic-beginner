# sql-server-basic-beginner
* **Họ và tên:** Hoàng Trường Phúc
* **Môn học:** Hệ quản trị cơ sở dữ liệu
* **Công cụ sử dụng:** SQL Server Management Studio (SSMS) 19/20
 ###  Các nội dung đã thực hiện
1. **Thiết lập cấu trúc lưu trữ:** Tạo Database, quản lý file vật lý `.mdf` và `.ldf` tại thư mục riêng.
2. **Nhập liệu quy mô lớn:** Import thành công hơn 12,000 dòng dữ liệu từ file .cvs.
3. . **Thao tác dữ liệu nâng cao:** - Sử dụng `SELECT INTO` để tách bảng.
   - Dùng `UPDATE`, `DELETE` với các điều kiện phức tạp (`LIKE`, `IS NULL`).
4. **Backup & Restore:** Xuất toàn bộ cấu trúc và dữ liệu ra file `.sql` để tái sử dụng.
 ### Minh chứng kết quả thực hiện
1. Cài đặt sql server
<img width="1920" height="1080" alt="Screenshot 2026-04-11 004635" src="https://github.com/user-attachments/assets/2a4876cb-30fc-40fe-b57b-d4687ce79de4" />
2. Cấu hình cho SQL Server làm việc ở cổng động (Dynamic Port), TCP :
<img width="1182" height="894" alt="Screenshot 2026-04-10 232306" src="https://github.com/user-attachments/assets/24fe4ab2-7130-4c5b-a3ed-8f3d0b14fc8f" />
<img width="515" height="630" alt="Screenshot 2026-04-10 232142" src="https://github.com/user-attachments/assets/e72d1e1c-426b-4a7f-b73c-825a87f262ca" />

kiểm tra lại bằng Cmd:
<img width="1483" height="762" alt="Screenshot 2026-04-10 232354" src="https://github.com/user-attachments/assets/c227afea-a00f-4745-bd0d-7a1f5e3046ae" />

3. Đăng nhập vào sql server
<img width="609" height="742" alt="image" src="https://github.com/user-attachments/assets/ac1477a7-a52c-46ed-8cf9-7ed6dddba767" />


Windows Authentication
 
<img width="609" height="742" alt="Screenshot 2026-04-11 010220" src="https://github.com/user-attachments/assets/a9381963-60db-43bc-87a9-db24b8ab5348" />


SQL Server Authentication.


4. Sử dụng giao diện đồ hoạ của ssms: Tạo cơ sở dữ liệu mới (create database) , chọn Path (nơi lưu trữ db) cho file lưu dữ liệu và file lưu log ở ổ đĩa khác với ổ C
<img width="1920" height="1080" alt="Screenshot 2026-04-10 232807" src="https://github.com/user-attachments/assets/cc3a345a-5616-4e47-b0bc-f03318d2a1c9" />



5. Sử dụng giao diện đồ hoạ của ssms: Tạo bảng dữ liệu (create and design table), có các trường dữ liệu phù hợp với dữ liệu của file data mẫu (CSV), với Khoá chính (Primary Key) là trường masv, import dữ liệu từ file mẫu vào trong bảng vừa tạo.
<img width="1920" height="1080" alt="Screenshot 2026-04-10 234528" src="https://github.com/user-attachments/assets/7b44ad8a-e701-4a73-b93a-ab2a13a2ffeb" />
<img width="1920" height="1080" alt="Screenshot 2026-04-10 234539" src="https://github.com/user-attachments/assets/b0fbe484-edf4-4ea6-8ca8-46643d741ec0" />
<img width="1920" height="1080" alt="Screenshot 2026-04-10 234544" src="https://github.com/user-attachments/assets/e9976a78-cbfb-4b18-99da-4243fe63b5f7" />


6. Kiểm tra số dòng của bảng dữ liệu sau khi import
<img width="1920" height="1080" alt="Screenshot 2026-04-10 234744" src="https://github.com/user-attachments/assets/4f3042ba-6a38-40ed-8bc4-9ca375bb1a1f" />



7. lệnh để thêm (insert) 1 row vào bảng, với dữ liệu là thông tin cá nhân của sv

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/23e17bf4-a68c-4429-bea0-3bfbdfd4229b" />




8.cập nhật(update) trường noisinh thành 'Sao Hoả' cho những dòng có noisinh và diachi đều là NULL.


<img width="1920" height="1020" alt="Screenshot 2026-04-10 235523" src="https://github.com/user-attachments/assets/c6471182-23ca-412c-8d1e-e5aedb0816ed" />



<img width="1920" height="1080" alt="Screenshot 2026-04-10 235603" src="https://github.com/user-attachments/assets/910ca1e3-3f90-424b-9d93-4e351e7f1223" />




9. Tạo bảng SaoHoa gồm những sinh viên có nơi sinh ở 'Sao Hoả'

<img width="1920" height="1080" alt="Screenshot 2026-04-10 235813" src="https://github.com/user-attachments/assets/45b3b3b3-6c9d-4354-80d7-a39c3e3f327e" />


<img width="1920" height="1080" alt="Screenshot 2026-04-11 000011" src="https://github.com/user-attachments/assets/8697920c-7038-429e-8047-061c158d908a" />



10. Xoá (delete) trong bảng SaoHoa những sinh viên cùng họ Hoàng


<img width="1920" height="1080" alt="Screenshot 2026-04-11 000113" src="https://github.com/user-attachments/assets/27115dd2-0b46-4f91-b86e-7536dc832685" />






<img width="1920" height="1020" alt="Screenshot 2026-04-11 000134" src="https://github.com/user-attachments/assets/2ba2b4d4-f2ed-4b58-b696-e953acdb1bd3" />






11.  Xuất toàn bộ kết quả của các bước ra file dulieu.sql


<img width="1920" height="1080" alt="Screenshot 2026-04-11 000416" src="https://github.com/user-attachments/assets/93406a12-52f7-4807-b026-4be1725d7514" />



<img width="1920" height="1080" alt="Screenshot 2026-04-11 000710" src="https://github.com/user-attachments/assets/3623416d-1884-44e5-8521-ebbbc79e01ee" />





12. Xóa Csdl đã tạo


<img width="1920" height="1080" alt="Screenshot 2026-04-11 001330" src="https://github.com/user-attachments/assets/0f19100d-3719-4c82-acd9-87974d52a7bf" />




<img width="954" height="826" alt="Screenshot 2026-04-11 000902" src="https://github.com/user-attachments/assets/f2c186e4-f09a-4d3a-b6ea-afd9489ef703" />


12. Phục hồi dữu liệu,  ở file dulieu.sql

   
<img width="1920" height="1020" alt="Screenshot 2026-04-11 002207" src="https://github.com/user-attachments/assets/0e17a319-0e25-45d6-9bc4-9323493f5b88" />


13. Upload github


<img width="1920" height="1032" alt="image" src="https://github.com/user-attachments/assets/2dd2e3fa-ca93-437b-a978-2d59c5c7c42e" />





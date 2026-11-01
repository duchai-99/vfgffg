# Vấn đề :
Nếu đồng bộ toàn bộ về máy, SSD sẽ bị tràn ngay lập tức và gây treo phần mềm đồng bộ.
# Yêu cầu :
-   Giải pháp kỹ thuật: Mô tả cách thiết lập tính năng Files On-Demand để chỉ tải file xuống khi cần mở thực tế.
    
-   Báo cáo dung lượng: Tính toán và chứng minh tính hiệu quả của giải pháp khi dung lượng Cloud lớn hơn dung lượng Local SSD nhiều lần.
# Cách làm 
1.  Giải pháp kỹ thuật (Files On-Demand):
    
    -   Cơ chế: Bật tính năng Files On-Demand_ (hoặc _Stream files_) trên ứng dụng Cloud . File hiển thị đầy đủ trên máy nhưng dung lượng cục bộ bằng 0 (chỉ tải về khi mở xem và có thể giải phóng dung lượng ngay sau khi dùng).
        
    -   Kết quả: Vượt qua giới hạn 256GB SSD, quản lý mượt mà kho dữ liệu 500GB.
        
2.  Xử lý Bẫy dữ liệu mạng & phần cứng:
    
    -   Giới hạn băng thông Cài đặt tốc độ tải vừa phải (2-3 MB/s) để không làm nghẽn mạng nhà trọ.
        
    -   Chống đứt đoạn: Chỉnh chế độ Sleep thành khi cắm sạc và chia nhỏ dữ liệu thành từng ngày/phân đoạn để đồng bộ an toàn, tránh lỗi khi máy gập/mất mạng.

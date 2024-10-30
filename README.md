
### Tóm tắt thực hiện Challenge 1
1. **Tạo tệp cấu hình Nginx**: Tạo các tệp YAML cho deployment và service của Nginx, bao gồm:
   - `nginx-deployment.yaml`: Định nghĩa deployment cho Nginx.
   - `nginx-service.yaml`: Định nghĩa service để expose Nginx ra ngoài.

2. **Triển khai Nginx**:
   - Chạy lệnh `kubectl apply -f nginx-deployment.yaml` để triển khai Nginx.
   - Chạy lệnh `kubectl apply -f nginx-service.yaml` để tạo service cho Nginx.

3. **Truy cập vào Nginx**: Sử dụng lệnh `minikube service nginx-service --url` để lấy URL truy cập vào Nginx.
Dưới đây là tóm tắt các bước thực hiện Challenge 2 để bạn ghi vào phần README:

---

### Tóm tắt thực hiện Challenge 2

1. **Chuẩn bị Template:**
   - Tải xuống một template web tĩnh từ [Free CSS](https://www.free-css.com/free-css-templates).

2. **Đóng gói Container:**
   - Sử dụng base image `nginx` để tạo Docker image chứa web tĩnh.
   - Cấu hình Nginx để trỏ tới thư mục chứa file HTML của template. Đảm bảo sử dụng file cấu hình Nginx hợp lệ.

3. **Triển khai trên Kubernetes:**
   - Tạo một `Deployment` với tên `static-web-deployment`, cấu hình `replicas=2` để chạy hai bản sao của ứng dụng.
   - Tạo một `NodePort Service` với tên `static-web-service` để truy cập ứng dụng từ bên ngoài.

4. **Kiểm tra Kết Quả:**
   - Sử dụng `kubectl get pods` để kiểm tra trạng thái các pod. Đảm bảo rằng tất cả các pod đều đang chạy.
   - Sử dụng lệnh `curl` để thực hiện yêu cầu đến `NodePort` và kiểm tra xem trang web tĩnh có hiển thị đúng theo template không.

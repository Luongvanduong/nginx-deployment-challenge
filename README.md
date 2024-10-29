
### Tóm tắt thực hiện Challenge 1
1. **Tạo tệp cấu hình Nginx**: Tạo các tệp YAML cho deployment và service của Nginx, bao gồm:
   - `nginx-deployment.yaml`: Định nghĩa deployment cho Nginx.
   - `nginx-service.yaml`: Định nghĩa service để expose Nginx ra ngoài.

2. **Triển khai Nginx**:
   - Chạy lệnh `kubectl apply -f nginx-deployment.yaml` để triển khai Nginx.
   - Chạy lệnh `kubectl apply -f nginx-service.yaml` để tạo service cho Nginx.

3. **Truy cập vào Nginx**: Sử dụng lệnh `minikube service nginx-service --url` để lấy URL truy cập vào Nginx.

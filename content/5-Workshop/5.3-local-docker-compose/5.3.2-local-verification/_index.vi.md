---
title : "Kiểm tra stack local"
date : 2024-01-01
weight : 2
chapter : false
pre : " <b> 5.3.2 </b> "
---

#### Mục tiêu kiểm tra

Sau khi các container đã chạy, cần xác minh ứng dụng thật sự phản hồi đúng và luồng nghiệp vụ có thể hoàn tất. Việc kiểm tra gồm smoke test tự động, kiểm tra database và kiểm thử thủ công trên giao diện.

#### Smoke test frontend

~~~powershell
.\scripts\smoke-local.ps1
~~~

~~~bash
./scripts/smoke-local.sh
~~~

Kết quả mong đợi là frontend trả về HTTP 200 tại cổng 8080.

![Kết quả smoke-local.ps1 (chụp thực tế)](/images/5-Workshop/5.3-local-docker-compose/smoke-local-live.png)

#### Kiểm tra PostgreSQL

~~~powershell
.\scripts\verify-platform-db.ps1
~~~

Script này kiểm tra kết nối tới PostgreSQL trong Docker Compose. Đây là bước xác nhận platform database hoạt động bình thường trước khi đối chiếu với RDS ở môi trường AWS.

![Kết quả verify-platform-db.ps1 (chụp thực tế)](/images/5-Workshop/5.3-local-docker-compose/verify-db-live.png)

#### Kiểm tra giao diện

Quy trình kiểm tra thủ công gồm:

1. Truy cập <code>http://127.0.0.1:8080</code>.
2. Mở danh sách sản phẩm và kiểm tra dữ liệu hiển thị.
3. Chọn sản phẩm và thêm vào giỏ hàng.
4. Mở giỏ hàng, nhập thông tin thanh toán thử nghiệm.
5. Xác nhận trang hoàn tất đơn hàng hiển thị đúng.

![Trang chi tiết sản phẩm (chụp thực tế)](/images/5-Workshop/5.3-local-docker-compose/local-product-real.png)

![Giỏ hàng và form thanh toán (chụp thực tế)](/images/5-Workshop/5.3-local-docker-compose/local-cart-real.png)

![Đơn hàng hoàn tất (chụp thực tế)](/images/5-Workshop/5.3-local-docker-compose/local-checkout-real.png)

{{% notice note %}}
Luồng thanh toán đầy đủ được kiểm thử trên Docker Compose. Trên AWS EKS, Phase 1 tập trung vào các service cốt lõi nên chưa triển khai toàn bộ service phụ trợ.
{{% /notice %}}

#### Dừng môi trường local

~~~powershell
docker compose down
~~~

Nếu cần xóa cả volume:

~~~powershell
docker compose down -v
~~~

#### Kết quả

Sau bước này, có thể kết luận ứng dụng chạy ổn định trên môi trường local và đủ điều kiện chuyển sang triển khai AWS.

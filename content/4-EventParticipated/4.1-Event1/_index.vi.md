---
title: "Event 1"
date: 2026-05-09
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

# Bài thu hoạch "FCAJ Community Day"

### Thông tin sự kiện

| Hạng mục | Nội dung |
| --- | --- |
| Tên sự kiện | FCAJ Community Day |
| Thời gian | 09:00, ngày 09/05/2026 |
| Địa điểm | Tầng 26, tòa nhà Bitexco, số 02 đường Hải Triều, phường Sài Gòn, thành phố Hồ Chí Minh |
| Vai trò | Người tham dự |
| Số phiên chia sẻ | 4 phiên |

### Mục đích của sự kiện

FCAJ Community Day là sự kiện định kỳ do cộng đồng First Cloud Journey (FCAJ) tổ chức, nhằm kết nối thành viên từ người mới đến chuyên gia trong lĩnh vực Cloud Computing. Theo đánh giá của em sau khi tham dự, sự kiện hướng đến các mục tiêu chính sau:

1. **Kết nối cộng đồng Cloud:** Tạo không gian gặp gỡ, giao lưu và mở rộng mạng lưới quan hệ giữa các thành viên FCAJ.
2. **Định hướng lộ trình học tập:** Hỗ trợ sinh viên và người mới bắt đầu tiếp cận AWS/Cloud theo hướng đi phù hợp với chương trình FCAJ.
3. **Truyền cảm hứng tự học:** Chia sẻ phương pháp, tư duy học tập chủ động và cách duy trì động lực trong bối cảnh công nghệ thay đổi nhanh.
4. **Chia sẻ kiến thức thực tiễn:** Các diễn giả truyền đạt kinh nghiệm làm việc thực tế với hệ sinh thái AWS, AI và phát triển phần mềm — những nội dung mà tài liệu lý thuyết thường ít đề cập.

### Danh sách diễn giả

| STT | Diễn giả | Vai trò / Đơn vị |
| --- | --- | --- |
| 1 | Huỳnh Hoàng Long | Admin FCAJ |
| 2 | Nguyễn Tuấn Thịnh | DevOps Cloud Engineer |
| 3 | Anh Khang | Solutions Architect, Cloud Kinetics |
| 4 | Chị Thảo | Software Developer, Ngân hàng Quốc tế Việt Nam (VIB) |

### Nội dung các phiên chia sẻ

#### Phiên 1 — Tư duy tự học trong kỷ nguyên số (Huỳnh Hoàng Long)

Diễn giả mở đầu với chủ đề *"Addicted to Learning Like You're Addicted to Social Media"*, tập trung vào phương pháp học tập chủ động thay vì kiến thức kỹ thuật thuần túy.

**Vấn đề đặt ra:** Nhiều sinh viên dành thời gian cho mạng xã hội và trò chơi trực tuyến nhiều hơn việc học, dù ban đầu chỉ định sử dụng trong thời gian ngắn. Nguyên nhân không nằm ở sự lười biếng mà ở cơ chế dopamine — não bộ ưu tiên các hoạt động có phần thưởng nhanh, kích thích tò mò và tiêu hao ít năng lượng hơn so với việc học tập trung.

**Giải pháp đề xuất:**

1. **Áp dụng cơ chế phần thưởng:** Chia nhỏ mục tiêu học tập, tạo phản hồi tích cực ngay khi hoàn thành từng bước.
2. **Xây dựng chuỗi thói quen:** Duy trì streak học tập liên tục, tương tự mô hình của các ứng dụng học ngoại ngữ.
3. **Tận dụng hệ thống rank FCAJ:** Sử dụng cơ chế xếp hạng (đồng → bạc → vàng) để tạo động lực dài hạn trong lộ trình FCAJ.
4. **Chuyển đổi thói quen:** Thay thời gian lướt mạng xã hội bằng việc chia sẻ kiến thức AWS, dịch vụ mới và bài viết kỹ thuật trong cộng đồng.
5. **Tối ưu môi trường học:** Chuẩn bị không gian học tập gọn gàng, tạo điều kiện tâm lý thuận lợi cho việc tự học hàng ngày.

#### Phiên 2 — Prompt Engineering và kiến trúc AWS (Nguyễn Tuấn Thịnh)

Phiên kỹ thuật trình bày về kỹ năng giao tiếp hiệu quả với AI và demo dự án **Proptimizer** — sản phẩm cá nhân triển khai trên AWS trong khuôn khổ chương trình FCAJ.

**Phần 1 — Kỹ thuật viết prompt:**

| Vấn đề | Hệ quả |
| --- | --- |
| Prompt chung chung | Kết quả đầu ra không đặc thù, khó áp dụng |
| Prompt quá dài | Tốn token, chi phí sử dụng AI tăng cao |
| Hướng dẫn mơ hồ | Output không nhất quán, dễ sai lệch |

Diễn giả giới thiệu **7 thành phần cấu thành một prompt hiệu quả:** Role, Task, Context, Input, Output Format, Example và Constraint. Bên cạnh đó, các kỹ thuật nâng cao như Chain of Thought, Self-consistency và Tree of Thought được trình bày kèm lưu ý về chi phí token — đặc biệt khi sử dụng tiếng Việt (thường tốn gấp đôi so với tiếng Anh).

**Phần 2 — Kiến trúc giải pháp Proptimizer:**

| Tầng | Dịch vụ AWS | Vai trò |
| --- | --- | --- |
| Frontend / CDN | S3, CloudFront | Lưu trữ và phân phối nội dung tĩnh |
| Xác thực | Amazon Cognito | Quản lý đăng ký, đăng nhập, JWT |
| API | API Gateway | Điều phối request, rate limit, authorization |
| Backend | AWS Lambda | Xử lý logic serverless |
| AI | Amazon Bedrock | Truy cập foundation model, guardrails |
| Database | DynamoDB | Lưu prompt và lịch sử tối ưu hóa |
| Giám sát | CloudWatch | Logs và metrics (latency, error rate) |

Diễn giả cũng demo công cụ tối ưu prompt kèm extension trình duyệt, cho thấy cách tích hợp AI vào quy trình làm việc hàng ngày mà vẫn kiểm soát được chất lượng đầu ra.

#### Phiên 3 — Định hướng nghề nghiệp và tư duy nền tảng (Anh Khang)

Phiên tương tác với sinh viên năm 3–4 xoay quanh câu hỏi *"Tại sao sinh viên chưa sẵn sàng đi làm?"* trong bối cảnh AI phát triển mạnh.

**Quan điểm chính:**

1. **Kiến thức nền tảng không thể thay thế:** Trong môi trường công nghệ thay đổi nhanh, ứng viên cần tập trung vào foundation (hạ tầng, tư duy giải quyết vấn đề) thay vì cố gắng nắm hết toàn bộ dịch vụ AWS.
2. **Kỳ vọng thực tế từ nhà tuyển dụng:** Doanh nghiệp không yêu cầu ứng viên biết tất cả; nắm vững khoảng 5 dịch vụ AWS và hiểu sâu quan trọng hơn biết surface-level nhiều dịch vụ.
3. **AI trong bài tuyển dụng:** Hầu hết ứng viên sử dụng AI khi làm assignment — điều quan trọng là khả năng giải thích lý do chọn giải pháp, không chỉ nộp kết quả.
4. **Phân biệt kinh nghiệm và trải nghiệm:** Số năm làm việc không đồng nghĩa với mức độ trưởng thành nghề nghiệp; làm đa dạng dự án và domain có thể tích lũy trải nghiệm vượt số năm kinh nghiệm.

**Ba hành động diễn giả khuyến nghị:** Đặt câu hỏi nhiều hơn và học cách đặt câu hỏi đúng; ưu tiên tầm nhìn dài hạn (chấp nhận đánh đổi lương thấp để lấy kinh nghiệm); làm việc theo nhóm thay vì làm project đơn lẻ.

#### Phiên 4 — Phương pháp BMAD trong phát triển phần mềm (Chị Thảo)

Diễn giả trình bày phương pháp **BMAD Method** — framework mã nguồn mở hỗ trợ phát triển phần mềm có kỷ luật với sự hỗ trợ của AI, thay thế cách làm việc thiếu quy trình (prompt liên tục mà không kiểm soát chất lượng code).

**Vấn đề của phát triển phần mềm thiếu quy trình:**

- AI mất ngữ cảnh khi prompt liên tục trong một cuộc hội thoại dài.
- Code sinh ra khó triển khai (deploy) và bảo trì.
- Không kiểm soát được khi cập nhật hoặc sửa đổi tính năng.

**Quy trình BMAD gồm 3 giai đoạn:**

| Giai đoạn | Hoạt động | Đầu ra |
| --- | --- | --- |
| Planning | Brainstorm ý tưởng, phân tích yêu cầu | PRD (Product Requirements Document) |
| Solutioning | Thiết kế kiến trúc, chọn tech stack | Architecture document, epics, user stories |
| Implementation | Phát triển từng story độc lập | Source code, cập nhật theo document |

Triết lý cốt lõi: chất lượng phần mềm phụ thuộc vào chất lượng tài liệu đặc tả; mỗi tính năng được giao cho một AI agent riêng để giảm chồng chéo ngữ cảnh và hạn chế hallucination.

### Những gì em học được

Qua bốn phiên chia sẻ, em tổng hợp được các nhóm kiến thức sau:

**1. Tư duy học tập và phát triển bản thân**

- Việc duy trì thói quen học phụ thuộc vào hệ thống phần thưởng và môi trường học tập, không chỉ ý chí cá nhân.
- Chia sẻ kiến thức trong cộng đồng là cách hiệu quả để củng cố hiểu biết và xây dựng uy tín chuyên môn.
- Kiên trì duy trì thói quen học hàng ngày mang lại kết quả dài hạn hơn so với học dồn trong thời gian ngắn.

**2. Kỹ năng làm việc với AI**

- Cấu trúc prompt theo framework 7 thành phần giúp giảm sai lệch đầu ra và tối ưu chi phí token.
- AI là công cụ hỗ trợ, không thay thế tư duy — cần hiểu và giải thích được giải pháp em đưa ra.
- Chia nhỏ tác vụ và tách phiên làm việc khi ngữ cảnh bị lẫn là cách sử dụng AI hiệu quả.

**3. Kiến trúc AWS thực tiễn**

- Mô hình serverless đầy đủ có thể triển khai từ frontend đến AI mà không cần quản lý server.
- Amazon Cognito giúp rút ngắn thời gian xây dựng hệ thống xác thực.
- CloudWatch là thành phần bắt buộc trong kiến trúc production, không phải tùy chọn.

**4. Quy trình phát triển phần mềm với AI**

- BMAD Method cho thấy cách kết hợp AI agent với quy trình SDLC chuẩn.
- Phát triển theo hướng document-driven (PRD → Architecture → Stories → Code) giúp kiểm soát chất lượng tốt hơn.
- Làm việc nhóm — kể cả với AI agents đóng vai nhiều role — hiệu quả hơn phát triển đơn lẻ.

### Ứng dụng vào công việc thực tập

Dựa trên kiến thức thu được, em xác định các hướng ứng dụng cụ thể như sau:

| STT | Hướng ứng dụng | Cách thực hiện |
| --- | --- | --- |
| 1 | Lộ trình FCAJ | Duy trì streak, tích lũy rank và chia sẻ kiến thức hàng ngày |
| 2 | Dự án workshop | Tham khảo kiến trúc Proptimizer (serverless + Bedrock) cho bài lab AWS |
| 3 | Prompt engineering | Áp dụng framework 7 thành phần khi làm việc với AI trong dự án thực tập |
| 4 | BMAD Method | Thử nghiệm quy trình Planning → Solutioning → Implementation cho dự án mini e-commerce |
| 5 | Định hướng nghề nghiệp | Tập trung nắm vững 5 dịch vụ AWS cốt lõi thay vì học surface-level |

### Trải nghiệm tham dự sự kiện

Em tham dự FCAJ Community Day tại Bitexco tầng 26 với vai trò người tham dự. Đây là sự kiện kết hợp cả nội dung định hướng tư duy, kiến thức kỹ thuật và định hướng nghề nghiệp — khác biệt so với các workshop kỹ thuật thuần túy em từng tham gia.

**Không khí và kết nối cộng đồng**

Hội trường có số lượng tham dự đông đảo, chủ yếu là sinh viên các năm cuối đam mê Cloud Computing. Không khí cởi mở, khuyến khích đặt câu hỏi và chia sẻ — phù hợp với tinh thần learning community của FCAJ.

**Ấn tượng theo từng phiên**

- **Phiên Huỳnh Hoàng Long:** Thay đổi góc nhìn về cách tiếp cận việc học — tập trung xây dựng môi trường và thói quen thay vì chỉ cố gắng học nhiều hơn.
- **Phiên Nguyễn Tuấn Thịnh:** Demo trực tiếp dự án Proptimizer trên AWS, minh họa rõ cách kết hợp nhiều dịch vụ thành một sản phẩm hoàn chỉnh.
- **Phiên Anh Khang:** Cung cấp góc nhìn thực tế về kỳ vọng tuyển dụng và vai trò của AI trong quá trình phỏng vấn.
- **Phiên Chị Thảo:** Giới thiệu BMAD Method — hướng tiếp cận mới cho phát triển phần mềm có kỷ luật với AI.

**Bài học rút ra**

Sự kiện giúp em nhận thức rõ hơn rằng hành trình trở thành Cloud Engineer không chỉ là tích lũy kiến thức về dịch vụ AWS, mà còn bao gồm xây dựng thói quen tự học, kỷ luật phát triển phần mềm và tư duy nền tảng vững chắc. AI là công cụ mạnh mẽ nhưng cần được sử dụng trong khuôn khổ quy trình rõ ràng — thiếu quy trình sẽ dẫn đến sản phẩm không thể triển khai thực tế.

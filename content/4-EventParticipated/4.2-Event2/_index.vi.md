---
title: "Event 2"
date: 2026-05-23
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

# Bài thu hoạch "FCAJ Community Day" (lần 2)

### Thông tin sự kiện

| Hạng mục | Nội dung |
| --- | --- |
| Tên sự kiện | FCAJ Community Day (lần 2) |
| Thời gian | 09:00, ngày 23/05/2026 |
| Địa điểm | Tầng 26 & 36, tòa nhà Bitexco, số 02 đường Hải Triều, phường Sài Gòn, thành phố Hồ Chí Minh |
| Vai trò | Người tham dự |
| Số phiên chia sẻ | 6 phiên kỹ thuật + phần khai mạc |

### Mục đích của sự kiện

FCAJ Community Day (lần 2) tiếp tục định hướng kết nối cộng đồng First Cloud Journey, tập trung vào chủ đề **AI, Cloud và kinh nghiệm thực chiến** từ các diễn giả đang làm việc trong ngành. Theo đánh giá của em sau khi tham dự, sự kiện hướng đến các mục tiêu sau:

1. **Cập nhật xu hướng AI và Cloud:** Giúp sinh viên nắm bắt tác động của AI đến thị trường lao động và nhu cầu phát triển phần mềm.
2. **Chia sẻ kỹ năng thực hành:** Truyền đạt kinh nghiệm sử dụng AI đúng cách — từ context engineering, kiến trúc AWS đến triển khai hệ thống doanh nghiệp.
3. **Học hỏi từ dự án thực tế:** Các diễn giả demo sản phẩm, kiến trúc và bài học từ hackathon, dự án nội bộ ngân hàng.
4. **Khuyến khích tham gia cộng đồng:** Tạo không gian networking, đặt câu hỏi và chia sẻ kiến thức giữa các thành viên FCAJ.

### Danh sách diễn giả

| STT | Diễn giả | Vai trò / Đơn vị |
| --- | --- | --- |
| 1 | Nguyễn Gia Hưng | Solutions Architect AWS Vietnam, Người sáng lập FCAJ |
| 2 | Anh Tịnh (Trương) | Platform Engineer, GothamX |
| 3 | Hải Anh | Pacific Vietnam |
| 4 | Nguyễn Tuấn Thịnh | DevOps Cloud Engineer |
| 5 | Nhóm UTM Morpho (Uyển, Thảo, Mai) | Đội thi LA Hackathon |
| 6 | Đức Đào | Engineer (chia sẻ về LLM inference) |
| 7 | Cát Vy | Chuyên gia AI/Enterprise (VPBank) |

### Nội dung các phiên chia sẻ

#### Phần khai mạc — Xu hướng AI và thị trường lao động (Nguyễn Gia Hưng)

Diễn giả mở đầu với góc nhìn về **nghịch lý AI trong thị trường việc làm:** khi chi phí phát triển phần mềm giảm nhờ AI, nhu cầu và số lượng phần mềm lại tăng mạnh — tương tự hiệu ứng đèn LED tiết kiệm điện nhưng tổng tiêu thụ điện tăng vì con người chiếu sáng nhiều hơn.

**Nội dung chính:**

- AI làm phát triển phần mềm rẻ hơn, hiệu quả hơn → số lượng sản phẩm phần mềm sẽ tăng khủng khiếp trong tương lai.
- Quán quân và hạng ba Anthropic Hackathon là người non-IT (luật sư, bác sĩ) — chứng minh rào cản kỹ thuật đang giảm.
- Xu hướng nghề mới: **vibe software engineering** — vai trò sửa, maintain và hoàn thiện sản phẩm do người có ý tưởng (không chuyên IT) tạo ra bằng AI.
- Khuyến khích sinh viên không nản trước thị trường việc làm mà tập trung xây dựng năng lực giải quyết vấn đề thực tế.

#### Phiên 1 — Context Engineering: Bí quyết để AI trả lời đúng (Anh Tịnh)

Platform Engineer tại GothamX chia sẻ về **cách cung cấp ngữ cảnh (context) đúng** để AI thực sự hữu ích trong công việc.

**Vấn đề thường gặp:**

- Nhiều người dùng chung một chat cho mọi chủ đề (du lịch, CV, code…) → AI đổi context liên tục, kết quả sai lệch.
- Prompt quá dài với thông tin có thể tìm được trên internet (ví dụ: "bạn là senior architect 10 năm kinh nghiệm") → lãng phí token, AI không hiểu điểm quan trọng.

**Giải pháp đề xuất:**

1. **Cung cấp context riêng biệt:** Chia sẻ kiến thức chỉ có trong tổ chức — blueprint nội bộ, quy trình ngân hàng, convention của team — thay vì thông tin AI đã biết.
2. **Tách phiên làm việc (working session):** Mỗi task một session riêng; kết thúc session thì tóm tắt context mang sang session mới.
3. **Tự tin chia sẻ và đặt câu hỏi:** Kỹ năng giao tiếp quan trọng không kém kỹ năng kỹ thuật trong môi trường làm việc hiện đại.
4. **Ưu tiên developer biết dùng AI:** Trong tuyển dụng, người tuyển dụng sẽ ưu tiên developer sử dụng AI tool hiệu quả và tiết kiệm token.

#### Phiên 2 — Amazon Q và AI Agent cho doanh nghiệp (Hải Anh)

Diễn giả từ Pacific Vietnam trình bày về **Amazon Q** — trợ lý AI do AWS phát triển, hướng đến người dùng doanh nghiệp.

**Nhu cầu giải quyết:**

- Manager, senior và giám đốc mất nhiều thời gian tập hợp dữ liệu, file để làm báo cáo hàng tuần.
- Cần hệ sinh thái tích hợp (tương tự Microsoft 365, Google Workspace) qua một platform để user tự build agent phục vụ mục đích riêng.

**Tính năng nổi bật:**

| Tính năng | Mô tả |
| --- | --- |
| BI Dashboard | Phân tích chuyên sâu từ dữ liệu đầu vào |
| Insights Chat | Chat trực tiếp với agent qua thông tin đã tích hợp |
| Automation Flow | Tự động hóa quy trình (transcribe meeting → gửi email follow-up) |
| MCP Integration | Kết nối custom tool qua Model Context Protocol |

**Khái niệm Agent:** LLM (bộ não) kết hợp với các function/action có thể thực thi — khác với chatbot chỉ trả lời text. Demo bao gồm transcribe cuộc họp, phân tích file Excel thành dashboard và tích hợp MCP trên AWS.

#### Phiên 3 — CloudFront Flat-Rate Pricing (Nguyễn Tuấn Thịnh)

DevOps Engineer chia sẻ về **ý tưởng mô hình/gói CDN flat-rate** trong bối cảnh các dịch vụ liên quan đến CloudFront. Vì đây là nội dung ghi nhận từ sự kiện và chưa thấy là mô hình giá AWS công khai chính thức, phần này được trình bày như takeaway của phiên chia sẻ, không phải thông báo sản phẩm chính thức của CloudFront.

**Vấn đề với pay-as-you-go truyền thống:**

- Chi phí CDN phụ thuộc traffic → khó estimate bill cuối tháng.
- Rủi ro DDoS hoặc traffic spike bất thường có thể dẫn đến bill hàng chục nghìn USD.
- Doanh nghiệp e ngại triển khai CDN vì chi phí không dự đoán được.

**Ý tưởng gói flat-rate được thảo luận trong phiên:**

| Gói | Giá | Đặc điểm |
| --- | --- | --- |
| Free | $0 | Website nhỏ, bảo vệ cơ bản |
| Pro | $15/tháng | Startup, SMB |
| Business | $200/tháng | Doanh nghiệp, VPC Private Origin, WAF |
| Premium | $1,000/tháng | Enterprise, Origin Failover, latency thấp |

- Mô hình chi phí cố định hàng tháng nhằm giảm độ khó dự báo billing.
- Có thể đóng gói CDN, bảo vệ ứng dụng, DNS và credit lưu trữ tùy thiết kế của nhà cung cấp.
- Mỗi domain cần một gói riêng; có thể nâng cấp gói khi nhu cầu tăng.

#### Phiên 4 — Hành trình 36 giờ tại LA Hackathon: Dự án UTM Morpho (Uyển, Thảo, Mai)

Nhóm 3 thành viên (Uyển, Thảo, Mai) chia sẻ kinh nghiệm thi **LA Hackathon** — cuộc thi lớn nhất tại Việt Nam với thời hạn 36 giờ liên tục build sản phẩm.

**Ý tưởng sản phẩm — UTM Morpho:**

- Vấn đề: Khi dùng AI generate UI, mỗi lần chỉnh sửa nhỏ (màu button, spacing) phải prompt lại từ đầu → tốn thời gian và token.
- Giải pháp: Editor cho phép generate UI theo template và **chỉnh sửa trực tiếp trên giao diện** (kéo thả component, sửa CSS).

**Kiến trúc AI (3 agents):**

| Agent | Vai trò |
| --- | --- |
| A1 — Vision | Phân tích hình ảnh input, tạo file JSON layer |
| A2 — Engineering | Đọc JSON, tạo size, CSS, layout |
| A3 — Design | Áp dụng design system, sinh code HTML giao diện |

**Bài học từ hackathon:**

1. Lấy cảm hứng từ công việc hàng ngày thay vì cố gắng giải bài toán vĩ mô.
2. Tập trung vào feature cốt lõi khi thời gian hạn chế (8–9 giờ cuối cho MVP).
3. Chiến thuật pitch: demo trước, giải thích architecture sau trong 5 phút.
4. Quản lý sức khỏe trong 36 giờ: chia thời gian ăn, nghỉ, tránh overthinking và AI over-generation.

#### Phiên 5 — LLM Inference: Temperature và tính nhất quán đầu ra (Đức Đào)

Phiên kỹ thuật về **bản chất probabilistic của LLM** và cách tối ưu độ ổn định output trong production.

**Kiến thức cốt lõi:**

- LLM chọn token tiếp theo dựa trên điểm số (logit) — mang tính xác suất, không deterministic.
- Parameter **temperature** điều khiển độ ngẫu nhiên: temperature = 0 vẫn không đảm bảo output giống nhau 100% giữa các lần chạy (do inference optimization trên GPU).
- Temperature = 0 có thể gây lặp từ — nên đặt 0.1 cho một số model.

**Chiến lược giảm thiểu sự không nhất quán:**

| Chiến lược | Mô tả | Trade-off |
| --- | --- | --- |
| Chạy nhiều lần + voting | Nhiều sub-agent, chọn câu trả lời phổ biến nhất | Tăng cost và latency |
| Self-host model | Kiểm soát hoàn toàn inference config | Tăng chi phí hạ tầng |
| JSON mode | Bật structured output (OpenAI JSON mode) | Giảm format error |
| Thiết kế downstream resilient | Service nhận output phải handle nhiều format | Cần test kỹ |

**Key takeaway:** LLM là probabilistic model — luôn thiết kế hệ thống để handle sự biến thiên; test nhiều trường hợp trước khi đưa lên production.

#### Phiên 6 — Enterprise Multi-Agent System cho đánh giá tín dụng (Cát Vy)

Phiên cuối chuyển từ kỹ thuật sang **tư duy nghiệp vụ (business mindset)** — kinh nghiệm triển khai AI tại VPBank.

**Bốn câu hỏi khi thiết kế giải pháp doanh nghiệp:**

1. **Ai xài?** — Xác định người dùng cuối.
2. **Xài cái gì?** — Chức năng cụ thể cần giải quyết.
3. **Tại sao phải xài?** — Giá trị mang lại so với cách làm hiện tại.
4. **Khi nào xài?** — Thời điểm triển khai phù hợp.

**Use case: Đánh giá tín dụng cho startup**

- Startup chiếm trọng số lớn trong hoạt động kinh doanh ngân hàng nhưng model tín dụng truyền thống ít tập trung vào startup.
- Xây dựng **multi-agent system** enterprise-grade cho quy trình đánh giá tín dụng.

**Sáu trụ cột hệ thống doanh nghiệp:**

| Trụ cột | Nội dung |
| --- | --- |
| Knowledge Transfer | Chuyển giao tri thức từ chuyên gia nghiệp vụ vào model — không chỉ đẩy data |
| Context Engineering | Indexing tài liệu nghiệp vụ, codebase; cần expert xác nhận đúng/sai |
| Guardrails & Compliance | Prompt injection defense, audit trail, data validation |
| Security Perimeter | VPC, Security Group, PrivateLink, network isolation |
| Reliability | Single point of failure, processing, high availability |
| Deployment Phases | Internal Testing → SIT → UAT → Pilot → Scale |

**Thông điệp quan trọng:** Doanh nghiệp đánh giá **mindset** nhiều hơn độ sâu dự án cá nhân khi phỏng vấn. Kiến thức kỹ thuật phần mềm (JWT, OAuth, software engineering) vẫn bắt buộc để đưa AI từ phòng lab lên production.

### Những gì em học được

**1. Xu hướng ngành và định hướng nghề nghiệp**

- AI không loại bỏ việc làm IT mà thay đổi cấu trúc — tạo ra nghề mới (maintain, fix sản phẩm AI-generated).
- Developer biết dùng AI hiệu quả sẽ được ưu tiên trong tuyển dụng.
- Mindset nghiệp vụ (ai xài, xài gì, tại sao, khi nào) quan trọng không kém kiến thức kỹ thuật.

**2. Kỹ năng làm việc với AI**

- Context engineering: cung cấp ngữ cảnh riêng của tổ chức, tách session theo task.
- LLM là probabilistic — không assume temperature = 0 cho output cố định; thiết kế hệ thống resilient.
- Knowledge transfer từ chuyên gia nghiệp vụ là yếu tố then chốt trong AI doanh nghiệp.

**3. Kiến thức AWS**

- Mô hình CDN flat-rate có thể giúp kiểm soát rủi ro chi phí cho startup và SMB, nhưng khi áp dụng CloudFront cần kiểm tra lại bảng giá chính thức.
- Amazon Q hỗ trợ xây dựng AI agent tích hợp MCP cho automation doanh nghiệp.
- Kiến trúc serverless với multi-agent (vision → engineering → design) có thể triển khai cho sản phẩm AI.

**4. Kinh nghiệm từ hackathon và dự án thực tế**

- Lấy ý tưởng từ pain point hàng ngày hiệu quả hơn giải bài toán lý thuyết.
- Tập trung MVP khi thời gian hạn chế; demo trước khi giải thích architecture.
- Triển khai AI enterprise cần quy trình: Internal Test → SIT → UAT → Pilot → Scale.

### Ứng dụng vào công việc thực tập

| STT | Hướng ứng dụng | Cách thực hiện |
| --- | --- | --- |
| 1 | Context engineering | Tách session AI theo task; cung cấp context dự án thay vì prompt chung chung |
| 2 | CloudFront | Cân nhắc phương án kiểm soát chi phí và kiểm tra bảng giá CloudFront chính thức trước khi triển khai CDN cho dự án workshop |
| 3 | Kiến trúc multi-agent | Tham khảo mô hình 3 agents (vision → engineering → design) cho bài lab AI |
| 4 | LLM production | Thiết kế downstream service handle output biến thiên; test nhiều trường hợp |
| 5 | Tư duy doanh nghiệp | Áp dụng 4 câu hỏi (ai xài, xài gì, tại sao, khi nào) khi thiết kế giải pháp |

### Trải nghiệm tham dự sự kiện

Em tham dự FCAJ Community Day lần 2 tại Bitexco với số lượng tham dự đông đảo — cả tầng 26 và tầng 36. So với Community Day đầu tiên (09/05/2026), sự kiện lần này đi sâu hơn vào **kỹ thuật AI production** và **kinh nghiệm doanh nghiệp**.

**Không khí và kết nối cộng đồng**

Không khí cởi mở, khuyến khích đặt câu hỏi và trao đổi — phù hợp tinh thần learning community của FCAJ.

**Ấn tượng theo từng phiên**

- **Phần khai mạc (Nguyễn Gia Hưng):** Góc nhìn lạc quan về thị trường việc làm — AI tạo thêm việc làm dài hạn thay vì thay thế hoàn toàn.
- **Phiên Anh Tịnh:** Thực tế và dễ áp dụng — cách tách context và session khi làm việc với AI hàng ngày.
- **Phiên Hải Anh:** Demo Amazon Q trực tiếp, thấy rõ tiềm năng AI agent trong môi trường doanh nghiệp.
- **Phiên Nguyễn Tuấn Thịnh:** Ý tưởng về pricing và kiểm soát chi phí CDN — hữu ích cho việc estimate chi phí dự án.
- **Phiên UTM Morpho (Uyển, Thảo, Mai):** Câu chuyện hackathon truyền cảm hứng — chứng minh có thể build sản phẩm hoàn chỉnh trong 36 giờ.
- **Phiên Đức Đào:** Hiểu sâu hơn về bản chất probabilistic của LLM và cách thiết kế hệ thống production-ready.
- **Phiên Cát Vy:** Chuyển góc nhìn từ technical sang business — hiểu rõ hơn kỳ vọng doanh nghiệp khi triển khai AI.

**Bài học rút ra**

Sự kiện giúp em nhận thức rằng hành trình Cloud/AI Engineer không chỉ là học dịch vụ AWS mà còn cần: kỹ năng context engineering, tư duy thiết kế hệ thống production-ready, và đặc biệt là **mindset nghiệp vụ** để giải quyết bài toán thực tế của doanh nghiệp.
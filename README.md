# Track 1 - Day 17 - Team: G28

**Nhóm:** G28

**Thành viên:**
| Họ và tên | MHV |
|---|---|
| Nguyễn Trung Hiếu | 2A202601620 |  
| Đặng Ngọc Anh | 2A202601706 |  

**Case đã chọn:** Case C — AI Support Radar

Sau mỗi phiên học, hệ thống phân tích các tín hiệu như di chuyển giữa slide, dừng lâu hoặc xem lại, highlight và ghi chú, đánh dấu "Chưa hiểu", thay đổi câu trả lời, và nội dung trao đổi với AI Chat.

AI tạo một **Support Queue** cho giảng viên, gồm:
1. Những học viên có thể cần hỗ trợ.
2. Phần nội dung mà họ có thể đang gặp khó khăn.
3. Các tín hiệu dẫn đến nhận định đó.
4. Một hành động hỗ trợ được đề xuất.

Giảng viên xem lại và quyết định có liên hệ với học viên hay không.

---

## 1. Problem Hypothesis Brief

### 1.1 Solution — Capability trung tính

**Solution directive:** Support Queue

**Capability trung tính:** Khả năng quan sát dấu hiệu hành vi trong lúc học, suy ra ai có thể đang gặp khó và ở nội dung nào, rồi đưa thông tin đó tới người có thể can thiệp và người đó tự quyết định có hành động hay không.

### 1.2 Change — Chuỗi thay đổi kỳ vọng

**Các thay đổi được kỳ vọng:**
1. Sinh viên tương tác nhiều hơn với bài giảng.
2. Giảng viên phản hồi các yêu cầu hỗ trợ của sinh viên kịp thời hơn, đúng nội dung hơn.
3. Tỷ lệ sinh viên hoàn thành môn học được nâng cao.

**Output team tạo ra:** Support Queue (danh sách học viên cần hỗ trợ + nội dung + tín hiệu + đề xuất hành động).
**Outcome team chỉ có thể ảnh hưởng:** học viên thực sự được hỗ trợ kịp thời, hổng kiến thức giảm, kết quả học tập cải thiện.

Nếu user không thay đổi hành vi (giảng viên không đọc/phản hồi Support Queue, hoặc sinh viên không tương tác thật với bài giảng), solution không tạo ra được outcome mong muốn.

### 1.3 Actor

| Actor | Họ đang làm gì? | Pain/hậu quả có thể có | Hưởng lợi thế nào? |
|---|---|---|---|
| Giảng viên | Giảng dạy lớp đông, không có kênh nào để biết ai đang vướng ở đâu | Quá tải, không nhận diện được nhu cầu hỗ trợ đúng lúc | Nhận diện sớm học viên cần hỗ trợ, can thiệp đúng nội dung |
| Sinh viên | Học qua slide/tài liệu, có thể gặp khó nhưng không luôn lên tiếng | Hổng kiến thức tích lũy, kết quả học tập giảm | Được hỗ trợ kịp thời, đúng chỗ đang vướng |
| Nhà quản lý giáo dục | Theo dõi chất lượng đào tạo tổng thể | Tỷ lệ bỏ học/kết quả kém ảnh hưởng đến chỉ số chung | Hưởng lợi gián tiếp từ kết quả học tập tốt hơn |

**Actor nhóm chọn để điều tra trước:** Sinh viên.

**Vì sao chọn nhánh này:** Pain chính được xác nhận thuộc về giảng viên (người trực tiếp sử dụng solution và trực tiếp trải nghiệm pain quá tải/thiếu thông tin). Nhóm chọn phỏng vấn sinh viên trước để **kiểm chứng gián tiếp** giả thuyết pain của giảng viên: liệu sinh viên có thực sự gặp khó mà không lên tiếng hay không, đây là mắt xích quyết định giả thuyết "giảng viên không thấy thông tin" có đúng hay không. Đây không phải là đổi actor sở hữu pain chính, mà là chọn nguồn evidence gián tiếp trước khi tiếp cận giảng viên.

### 1.4 Situation & Job

**Mô tả Situation & Job (góc nhìn Học viên):**

Khi đang học qua slide bài giảng và gặp một nội dung khó hiểu, sinh viên đang cố tiếp tục theo kịp bài học mà không bị gián đoạn — hiện tại họ tự xoay sở bằng cách đọc lại slide, hỏi bạn, tra cứu ngoài, hỏi AI Chat, hoặc đơn giản là bỏ qua và học tiếp. Điểm bắt đầu gặp vướng mắc: khi cách tự xoay sở đó không đủ để hiểu rõ nội dung, nhưng sinh viên không chủ động phản ánh với giảng viên.

**JTBD Hypothesis:**

Khi đang học một nội dung khó trên slide và không hiểu ngay, tôi muốn tìm ra cách hiểu nội dung đó mà không làm gián đoạn tiến độ học hoặc phải chủ động thừa nhận mình chưa hiểu, để có thể tiếp tục theo kịp bài học.

### 1.5 Pain

**Pain Hypothesis A (chọn để điều tra trước):**

Khi gặp nội dung khó trong bài giảng, giảng viên gặp khó khăn trong việc nhận diện đúng học viên và đúng nội dung cần hỗ trợ vì không có kênh tín hiệu nào phản ánh việc học viên đang vướng ở đâu, dẫn đến hỗ trợ bị chậm trễ hoặc bỏ sót, và học viên tích lũy lỗ hổng kiến thức.

**Pain Hypothesis B (cách giải thích cạnh tranh):**

Khi gặp nội dung khó, sinh viên có nhận ra mình chưa hiểu nhưng không chủ động phản ánh vì ngại giao tiếp hoặc cho rằng việc đó không đáng để hỏi, dẫn đến giảng viên không có cách nào biết để can thiệp dù có công cụ quan sát.

**Lý do chọn A để điều tra trước:** A là pain được xác nhận trực tiếp từ actor sở hữu pain chính (giảng viên) ở bước Actor. Tuy nhiên vì vòng này phỏng vấn sinh viên, nhóm dùng câu hỏi hành vi để kiểm chứng xem bằng chứng thu được nghiêng về A (thiếu kênh tín hiệu) hay B (có kênh nhưng SV không dùng vì tâm lý) — hai giả thuyết này dẫn tới hướng giải pháp khác nhau nên cần phân biệt rõ bằng evidence thay vì giả định.

### 1.6 Evidence

| Cần kiểm tra | Evidence làm nhóm tin hơn | Evidence làm nhóm nghi ngờ hoặc bác bỏ |
|---|---|---|
| Situation có thật | SV kể được một buổi học cụ thể gần đây có gặp nội dung khó | SV không nhớ được lần nào cụ thể, chỉ nói chung chung "thỉnh thoảng" |
| Pain có ý nghĩa | SV mô tả hậu quả rõ ràng (mất điểm, phải học lại, bị rối ở bài sau) | SV nói "cũng không sao, học tiếp thôi" mà không có hậu quả nào |
| Workaround tồn tại | SV kể workaround cụ thể đã dùng (hỏi bạn, hỏi AI Chat, tra Google) và công sức bỏ ra | SV không làm gì cả, hoặc không nhớ đã từng xử lý thế nào |
| Consequence tồn tại | Có ảnh hưởng quan sát được tới buổi học sau/điểm số | Không có ảnh hưởng nào nối tiếp, vấn đề tự biến mất |
| Pattern có lặp | SV xác nhận tình huống này xảy ra nhiều lần, không phải một lần duy nhất | Chỉ xảy ra đúng một lần, không mang tính đại diện |

**Problem Hypothesis mang sang Chặng 2:**

Giảng viên trong lớp học (đặc biệt mô hình hybrid) không có cách nào biết học viên nào đang gặp khó và ở nội dung nào, vì học viên gặp khó thường không chủ động phản ánh; điều này khiến hỗ trợ bị chậm trễ hoặc bỏ sót, và học viên tích lũy lỗ hổng kiến thức qua các buổi học tiếp theo.

**Điều gì phải đúng để giả thuyết đứng vững:** Sinh viên xác nhận có gặp khó khăn cụ thể trong lúc học nhưng phần lớn không chủ động báo với giảng viên; hậu quả (hổng kiến thức, ảnh hưởng buổi sau) là có thật và lặp lại, không phải trường hợp cá biệt.

**Điều gì có thể khiến nhóm sửa hoặc bác bỏ giả thuyết:** Nếu sinh viên cho thấy họ đã có kênh hiệu quả để báo khó khăn (hỏi trực tiếp, nhóm chat lớp...) và vẫn dùng đều đặn, thì pain không nằm ở "thiếu kênh phản ánh" mà có thể nằm ở chỗ khác (ví dụ giảng viên có nhận được nhưng không đủ thời gian xử lý). Nếu phần lớn SV nói không gặp khó khăn đáng kể hoặc hậu quả không rõ ràng, pain có thể không đủ nghiêm trọng để theo đuổi.

**Solution Parking Lot:**

| # | Hướng giải quyết có thể có | AI / Không sử dụng AI |
|---|---|---|
| 1 | Hệ thống AI phân tích tín hiệu hành vi và tạo Support Queue cho giảng viên (solution gốc) | AI |
| 2 | Nút "Tôi chưa hiểu" đơn giản trên mỗi slide, tổng hợp thành báo cáo cuối buổi cho giảng viên | Không dùng AI |
| 3 | Khảo sát nhanh cuối buổi (1-2 câu) gửi tự động, giảng viên xem kết quả tổng hợp | Không dùng AI |
| 4 | AI chatbot trả lời trực tiếp câu hỏi của sinh viên ngay trong lúc học, không cần đợi giảng viên | AI |
| 5 | Buổi ôn tập đầu giờ do trợ giảng/coach dẫn dắt dựa trên câu hỏi SV gửi trước qua form | Không dùng AI |

---

## 2. Conversation Guide phiên bản cuối

> Chưa cập nhật — sẽ điền sau khi hoàn thành buổi luyện phỏng vấn (Chặng 3) và họp sửa guide (Chặng 4).

## 3. Practice Reflection

1. **Câu hỏi nào đã giúp user kể một tình huống cụ thể?**
   > _(điền sau phỏng vấn)_

2. **Chỗ nào mình cần làm tốt hơn ở lần phỏng vấn thật?**
   > _(điền sau phỏng vấn)_

3. **Sau khi luyện, nhóm đã sửa Conversation Guide ở đâu và vì sao?**
   > _(điền sau phỏng vấn)_

## 4. AI Support Log


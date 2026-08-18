# Track 1- Day 17

## Case C: AI Support Radar

Bản phân tích cá nhân về bài tập trong ngày 17 của chương trình AI thực chiến

---
Cần đi ngược từ problem → pain → behavior → evidence → opportunity → solution.

## 1. Xác định stakeholder

| Stakeholder                                  | Vai trò                                      | Mức độ liên quan |
| -------------------------------------------- | -------------------------------------------- | ---------------- |
| **Học viên**                                 | Người đang học, tạo ra các tín hiệu hành vi  | Cao              |
| **Giảng viên**                               | Người phát hiện, đánh giá và hỗ trợ học viên | Cao              |
| **Trợ giảng / Teaching Assistant**           | Theo dõi, giải đáp và hỗ trợ học viên        | Trung bình       |
| **Learning Support / Academic Advisor**      | Theo dõi học viên có nguy cơ không đạt       | Trung bình       |
| **Instructional Designer / Course Designer** | Thiết kế nội dung và trải nghiệm học tập     | Thấp             |
| **Quản lý đào tạo / Program Manager**        | Chịu trách nhiệm outcome của khóa học        | Trung bình       |
| **LMS Administrator / Product Owner**        | Quản lý hệ thống và dữ liệu học tập          | Ít ảnh hưởng     |
| **Nhà trường / tổ chức đào tạo**             | Chịu trách nhiệm về chất lượng đào tạo       | Trung bình       |
| **Phụ huynh / đơn vị cử đi học**             | Có thể quan tâm đến kết quả học tập          | Thấp             |
| **IT / Data / AI team**                      | Xây dựng và vận hành solution                | Thấp             |

**Stakeholder nên phỏng vấn đầu tiên**  
Tôi sẽ ưu tiên:
> Học viên → Giảng viên → Trợ giảng → Quản lý đào tạo

Trong đó cần đặc biệt phỏng vấn học viên và giảng viên riêng biệt, vì họ có thể nhìn cùng một vấn đề theo hai hướng hoàn toàn khác nhau.

## 2. Ai trực tiếp trải nghiệm pain?

Primary pain owner: Giảng viên

Pain có khả năng tồn tại là:

> Giảng viên không biết chính xác học viên nào đang gặp khó khăn và khó khăn ở nội dung nào, đặc biệt trong lớp học đông hoặc học online.

Ví dụ:

> Không thể quan sát hết học viên.
> Một số học viên không chủ động hỏi.
> Điểm số chỉ cho biết kết quả, không cho biết quá trình dẫn đến kết quả.
> Học viên có thể làm đúng bài nhưng thực chất chưa hiểu.
> Khi phát hiện ra vấn đề thì đã muộn.
> Giảng viên không có đủ thời gian để kiểm tra từng người.

Nhưng có một điểm rất quan trọng:
> Học viên mới có thể là người trải nghiệm pain sâu hơn.

Ví dụ:

> "Tôi không hiểu phần này nhưng không biết hỏi ai."

hoặc:

> "Tôi không muốn giơ tay hỏi vì sợ mình là người duy nhất không hiểu."

Do đó cần phân biệt giữa Pain owner, Feature user và End beneficiary

## 3. Ai phải thay đổi hành vi để outcome xảy ra?

Đây là câu hỏi rất quan trọng đối với Case C.

> Solution này chỉ tạo ra outcome nếu giảng viên thay đổi hành vi.

Hiện tại, Giảng viên:

> Dạy → chờ học viên hỏi → xem điểm → phát hiện vấn đề → hỗ trợ.

Nếu AI Support Radar tồn tại, Giảng viên:

> Dạy → xem Support Queue → xác minh tín hiệu → quyết định có hỗ trợ hay không → can thiệp.

Do đó, behavior change chính của giảng viên là từ "Reactive support" sang "Proactive support".

Nhưng cũng có một behavior change thứ hai:
> Học viên phải chấp nhận việc hệ thống sử dụng tín hiệu học tập của họ để hỗ trợ.

Đây là vấn đề cần phỏng vấn vì có thể xuất hiện privacy/trust concern:
> "Tại sao hệ thống lại theo dõi tôi?"

## 4. Ai chịu hậu quả nếu problem không được giải quyết?

Có thể phân tầng như sau:

Học viên — hậu quả trực tiếp

- Không hiểu kiến thức nền.
- Tích lũy learning gap.
- Kết quả học tập giảm.
- Mất động lực.
- Bỏ học hoặc disengage.

Giảng viên — hậu quả vận hành

- Không biết ai cần hỗ trợ.
- Tốn thời gian tìm kiếm vấn đề.
- Phải xử lý khi vấn đề đã trở nên nghiêm trọng.
- Khó đảm bảo chất lượng lớp học.

Nhà trường / chương trình đào tạo

- Tỷ lệ hoàn thành thấp.
- Kết quả học tập thấp.
- Giảm chất lượng đào tạo.
- Tăng workload của giảng viên/support staff.

Về lâu dài Problem có thể tạo ra một vòng lặp:  
> Không phát hiện sớm → learning gap → kết quả kém → disengagement → cần nhiều support hơn.

## 5. Ai hưởng lợi gián tiếp?

Có thể gồm:

- Trợ giảng: giảm việc phải dò tìm thủ công người cần hỗ trợ.
- Learning Support: ưu tiên intervention.
- Course Designer: phát hiện module/chapter có vấn đề.
- Program Manager: có visibility về learning outcome.
- Nhà trường: cải thiện retention/completion.
- Các học viên khác: giảng viên có thêm thời gian dành cho lớp thay vì xử lý các case phát sinh muộn.

## 6. Người nhận feature có chắc là người sở hữu pain chính không?

Không chắc. Và đây chính là assumption cần kiểm chứng. Feature hiện tại được thiết kế cho: Giảng viên

Nhưng pain có thể thuộc về: Học viên

Ví dụ:  
Hypothesis A: Giảng viên không biết học viên nào đang gặp khó khăn. → Giảng viên là pain owner.  
Hypothesis B: Học viên gặp khó khăn nhưng không chủ động yêu cầu trợ giúp. → Học viên là pain owner.  
Hypothesis C: Nhà trường muốn giảm tỷ lệ học viên thất bại/bỏ học. → Program Manager / Institution là pain owner.  
Hypothesis D: Giảng viên biết học viên gặp vấn đề nhưng không có thời gian xử lý. → Pain nằm ở workflow của giảng viên.  

Do đó kết luận cá nhân là: không nên mặc định Case C là "AI dành cho giảng viên".
Nên kiểm chứng: Ai đang mất nhiều nhất vì problem này?

## 7. Ba tình huống cần đưa vào phỏng vấn

**Tình huống 1 — Học viên không hiểu nhưng không hỏi**  

Actor: Học viên  

Đang cố: Hoàn thành bài học và hiểu được nội dung khó.

Bằng cách hiện tại: Đọc lại slide → xem lại video → tìm Google → hỏi bạn → hoặc bỏ qua.

Rào cản:

- Không biết chính xác mình không hiểu ở đâu.
- Ngại hỏi giảng viên.
- Không muốn thừa nhận mình không hiểu.
- Không biết nguồn hỗ trợ nào đáng tin cậy.
- Không có feedback tức thời.

Câu hỏi: "Lần gần nhất bạn không hiểu một phần bài học, bạn đã làm gì?"

Sau đó tìm evidence:

- Có bao nhiêu lần xem lại?
- Có tìm tài liệu ngoài không?
- Có hỏi bạn bè?
- Có gửi câu hỏi cho giảng viên?
- Có bỏ qua không?
- Mất bao lâu để giải quyết?

**Tình huống 2 — Giảng viên muốn biết ai cần hỗ trợ**  

Actor: Giảng viên

Đang cố: Xác định học viên nào đang gặp khó khăn để hỗ trợ đúng người, đúng thời điểm.  

Bằng cách hiện tại: Xem điểm → đọc câu trả lời → quan sát lớp → chờ học viên hỏi → gửi survey/check-in.  

Rào cản:

- Lớp quá đông.
- Không có visibility về quá trình học.
- Dữ liệu nằm ở nhiều nơi.
- Không đủ thời gian kiểm tra từng học viên.
- Học viên không chủ động nói ra vấn đề.

Câu hỏi: "Lần gần nhất bạn phát hiện một học viên gặp vấn đề nhưng bạn không biết trước đó là khi nào?"

Sau đó tìm:

- Giảng viên phát hiện bằng cách nào?
- Mất bao lâu?
- Bao nhiêu học viên bị bỏ sót?
- Có sử dụng dữ liệu LMS không?
- Có workflow hỗ trợ hiện tại không?

**Tình huống 3 — Giảng viên có dữ liệu nhưng không biết phải làm gì**  

Actor: Giảng viên  

Đang cố: Quyết định học viên nào cần intervention và nên hỗ trợ như thế nào.

Bằng cách hiện tại: Dựa vào điểm thấp → kinh nghiệm cá nhân → câu hỏi của học viên → attendance → quan sát hành vi.

Rào cản:

- Dữ liệu chỉ phản ánh một phần vấn đề.
- Khó phân biệt "không hiểu" với "không tập trung".
- Có quá nhiều học viên.
- Không biết intervention nào phù hợp.
- Sợ đánh giá sai học viên.

Câu hỏi: "Bạn đã bao giờ chủ động liên hệ một học viên vì nghĩ họ đang gặp khó khăn nhưng sau đó phát hiện mình đoán sai chưa?"

Đây là câu hỏi rất giá trị. Nếu xảy ra thường xuyên, nó trực tiếp tạo justification cho: AI-generated evidence + recommended action

## 8. Từ pain → solution sẽ hình thành như thế nào?

Nếu phỏng vấn cho ra evidence như sau:

| Evidence                                         | Pain                                                 | Need                 |
| ------------------------------------------------ | ---------------------------------------------------- | -------------------- |
| Học viên xem lại cùng một phần nhiều lần         | Có thể đang gặp khó khăn nhưng không biết hỏi        | Detect struggle      |
| Học viên đánh dấu "Chưa hiểu" nhưng không hỏi GV | Support request không được chuyển thành intervention | Surface hidden need  |
| GV chỉ biết khi học viên làm bài sai             | Phát hiện quá muộn                                   | Early detection      |
| GV không thể kiểm tra 100–200 học viên           | Không có khả năng triage                             | Prioritization       |
| GV không tin dữ liệu đơn lẻ                      | Sợ false positive                                    | Evidence aggregation |
| GV biết ai yếu nhưng không biết nên làm gì       | Detection ≠ intervention                             | Recommended action   |

Khi đó mới có thể hình thành: AI Support Radar và từng thành phần của feature đều có provenance từ pain:

1. "Những học viên có thể cần hỗ trợ" ← Pain: GV không thể manually identify everyone.

2. "Phần nội dung gặp khó khăn" ← Pain: GV biết học viên có vấn đề nhưng không biết vấn đề nằm ở đâu.

3. "Các tín hiệu dẫn đến nhận định" ← Pain: GV không tin một prediction nếu không biết AI dựa vào đâu.

4. "Hành động hỗ trợ được đề xuất" ← Pain: Detection alone không giúp GV giảm workload.

## 9. 5 câu hỏi phỏng vấn

### Câu 1 — Recent incident

"Hãy kể cho tôi lần gần nhất bạn nhận ra một học viên đang gặp khó khăn trong quá trình học. Bạn phát hiện ra điều đó như thế nào?"

Mục tiêu: Discovery → hiện trạng → trigger → workflow.

### Câu 2 — Hidden problem

"Có trường hợp nào bạn nghĩ rằng một học viên đang gặp khó khăn nhưng họ không trực tiếp nói với bạn không? Bạn đã dựa vào dấu hiệu nào để nhận biết?"

Mục tiêu: Kiểm chứng assumption: Learning difficulty không được verbalize. Đồng thời tìm ra các signals mà con người hiện đang sử dụng.

### Câu 3 — Current workaround

"Khi bạn cần xác định học viên nào cần hỗ trợ, hiện tại bạn thường kiểm tra những thông tin hoặc dấu hiệu nào? Quy trình đó mất bao nhiêu thời gian và phần nào khó nhất?"

Mục tiêu: xác định pain của giảng viên.

### Câu 4 — Consequence / missed intervention

"Hãy kể một trường hợp bạn phát hiện ra vấn đề của học viên quá muộn. Điều gì đã xảy ra và nếu biết sớm hơn thì bạn có thể đã làm gì khác?"

Nếu interviewee không thể kể được một case thực tế, cần đặt dấu hỏi lớn về mức độ nghiêm trọng của problem.

### Câu 5 — Decision & trust

"Nếu hệ thống chỉ cho bạn một danh sách học viên có khả năng cần hỗ trợ, bạn cần biết những thông tin gì để quyết định có thực sự liên hệ với họ hay không?"

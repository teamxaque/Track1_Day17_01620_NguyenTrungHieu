# Track 1 - Day 17 - Team: G28

**Tên thành viên:**
| Họ và tên | Khóa | Mã sinh viên |
|---|---|---|
| Nguyễn Trung Hiếu | K4- Track 1 | 2A202601620 |
| Đặng Ngọc Anh | K4-Track 1 | 2A202601706 |  

**Case đã chọn**: Case C — AI Support Radar  
Sau mỗi phiên học, hệ thống phân tích các tín hiệu như di chuyển giữa slide, dừng lâu hoặc xem lại, highlight và ghi chú, đánh dấu “Chưa hiểu”, thay đổi câu trả lời, và nội dung trao đổi với AI Chat.

AI tạo một **Support Queue** cho giảng viên, gồm:
1. Những học viên có thể cần hỗ trợ.
2. Phần nội dung mà họ có thể đang gặp khó khăn.
3. Các tín hiệu dẫn đến nhận định đó.
4. Một hành động hỗ trợ được đề xuất.
Giảng viên xem lại và quyết định có liên hệ với học viên hay không.

# Chặng 1
## 1. Solution - Gỡ solution khỏi hình thức cụ thể
Câu hỏi dẫn dắt:

1. Câu nào trong directive đang mô tả giao diện, tên feature hoặc công nghệ?
> **AI Support Radar**: Đây là tên của feature, một thuật ngữ chỉ tính năng hoặc sản phẩm cụ thể. Ngoài ra, “radar” (công nghệ quét) có thể được hiểu theo nhiều cách, không chỉ giới hạn trong ngữ cảnh công nghệ thông tin.  
> **Support Queue**: Đây cũng là một thuật ngữ kỹ thuật, chỉ danh sách công việc hỗ trợ đang chờ xử lý.

2. Nếu bỏ tên nút, màn hình và AI action, khả năng cần tạo ra là gì?
> Bỏ đi những từ ngữ mang tính kỹ thuật, ta thấy bản chất của đề bài là “hỗ trợ học tập dựa trên hoạt động của người học và nội dung được học”.  
> Cần tạo ra một cơ chế có thể giúp giáo viên nhận diện được học viên nào cần trợ giúp. Học viên cần có kênh liên lạc khi cần trợ giúp


3. Nhóm có đang mặc định cách triển khai được giao là cách duy nhất không?
> Không. Nhóm xác định có nhiều cách triển khai khác.

4. Capability có thể được mô tả mà không dùng tên feature không?
>Có. "Tạo ra một hệ thống để hỗ trợ học tập dựa trên hoạt động của người học và nội dung được học".


**Solution directive:**  
**Capability trung tính:** Tạo ra một hệ thống hỗ trợ học tập.  

## 2. Change — Làm lộ chuỗi thay đổi được kỳ vọng
1. User sẽ biết hoặc làm được điều gì khác?
> Giảng viên biết được học viên nào có nguy cơ gặp khó khăn  
> Sinh viên nhận được sự hỗ trợ kịp thời từ giảng viên  


2. Hành vi nào phải thay đổi để outcome xảy ra?
> Sinh viên phải sử dụng ứng dụng vlearn để học thực sự: tương tác với slide bài giảng thật. Ví dụ: dừng lâu ở một slide, di chuyển nhanh qua một slide, highlight nội dung, ghi chú, đặt câu hỏi cho AI.  
> Giảng viên phải đọc và phản hồi lại danh sách các học viên cần hỗ trợ và các đề xuất hỗ trợ.  


3. Trạng thái hoặc kết quả nào được kỳ vọng thay đổi?
> Số lượng học viên cần hỗ trợ được giảm thiểu    
> Điểm đánh giá về sự trợ giúp của giảng viên tới đúng học viên được nâng cao  
> Số lượng sử dụng hệ thống học tập được tăng lên (số lượng sinh viên rời bỏ hệ thống giảm đi) 

4. Đâu là output team tạo ra, đâu là outcome team chỉ có thể ảnh hưởng?
> 

5. Nếu user không thay đổi hành vi, solution còn tạo được outcome không?
> Solution sẽ không tạo ra đúng outcome mong muốn.

**Các thay đổi được kỳ vọng:**  
1. Sinh viên tương tác nhiều hơn với bài giảng
2. Giảng viên phản hồi các yêu cầu hỗ trợ của sinh viên kịp thời hơn, đúng nội dung hơn. 
3. Tỷ lệ sinh viên hoàn thành môn học được nâng cao.

## 3. Actor — Xác định các nhóm người có liên quan
1. **Ai trực tiếp sử dụng solution?** Giảng viên  
2. **Ai trực tiếp trải nghiệm pain?** Giảng viên  
3. **Ai phải thay đổi hành vi để outcome xảy ra?** Sinh viên và Giảng viên  
4. **Ai chịu hậu quả nếu problem không được giải quyết?** Sinh viên và Giảng viên  
5. **Ai hưởng lợi gián tiếp?** Nhà quản lý giáo dục  
6. **Người nhận feature có chắc là người sở hữu pain chính không?** Có
**Actor nhóm chọn để điều tra trước:** Sinh viên  
**Vì sao chọn nhánh này thay vì actor khác:**  
- Sinh viên là đối tượng học tập trực tiếp, chịu ảnh hưởng lớn nhất bởi chất lượng hỗ trợ học tập. Việc tìm hiểu pain của sinh viên sẽ giúp xác định rõ các vấn đề cần giải quyết trong quá trình học tập.  
- Sinh viên cũng là người sử dụng trực tiếp solution, do đó hiểu biết của nhóm về sinh viên là hạn chế, cần phải điều tra thêm.  
- Sinh viên là người phải thay đổi hành vi để outcome xảy ra, do đó hiểu biết của nhóm về sinh viên là hạn chế, cần phải điều tra thêm.  
- Sinh viên là người chịu hậu quả nếu problem không được giải quyết, do đó hiểu biết của nhóm về sinh viên là hạn chế, cần phải điều tra thêm.  


## 4. Situation & Job — User đang cố làm gì trong tình huống nào?
- Giảng viên đang giảng dạy một lớp học có nhiều học viên nhưng không thể nắm bắt được có bao nhiêu học viên cần trợ giúp về nội dung trên slide bài giảng. Giảng viên cũng không biết được những nội dung cụ thể nào khiến học viên gặp khó khăn. 
- Giảng viên thường hỏi lại các sinh viên về nội dung bài cũ trong các buổi học tiếp theo.
- Điểm bắt đầu gặp vướng mắc: Khi không có ai phản ánh về các nội dung trong bài học cũ, giảng viên nghĩ rằng tất cả mọi người đều đã hiểu bài. Tuy nhiên, trên thực tế có những sinh viên đã không hiểu bài và gặp khó khăn trong quá trình học tập. Điều này dẫn đến việc sinh viên bị hổng kiến thức, ảnh hưởng đến kết quả học tập. 
- Khi vấn đề này sảy ra, giảng viên muốn có một cách để nhận diện được những học viên nào đang gặp khó khăn về bài giảng cũ, những nội dung nào khiến nhiều sinh viên bối rối nhất để tập trung giải đáp.

## 5. Pain — Viết các cách giải thích cạnh tranh
- Rào cản 1: Số lượng học viên cần trợ giúp quá đông trong cùng 1 thời điểm, khiến cho giảng viên không thể giải đáp hết các câu hỏi và nhu cầu hỗ trợ của sinh viên.  
- Rào cản 2: Không có sinh viên nào nêu ra cần sự hỗ trợ vì yếu tố tâm lý e ngại giao tiếp với giảng viên khi gặp khó khăn trong quá trình học.  
- Rào cản 3: Không có cách nào để biết được sinh viên gặp khó khăn ở đâu trong bài giảng, do đó không thể đưa ra giải pháp phù hợp.  

## 6. Evidence — Xác định điều cần tìm trước khi viết câu hỏi
- 

# Chặng 2
## Problem Hypothesis Brief:
Nhóm G28 đã xác định vấn đề của **AI Support Radar** như sau:

### 1. Bối cảnh và Khách hàng mục tiêu
- **Bối cảnh**: Giảng viên trong mô hình lớp học hybrid gặp khó khăn trong việc nhận diện và hỗ trợ kịp thời cho những học viên đang gặp vướng mắc, đặc biệt trong giai đoạn chuyển đổi sang học tập số hóa.
- **Khách hàng mục tiêu**: Giảng viên các lớp học hybrid, đặc biệt là giảng viên các môn học có đặc thù tương tác nhiều hoặc khối lượng kiến thức lớn.

### 2. Vấn đề đang gặp phải
- Giảng viên khó theo dõi và đánh giá mức độ hiểu bài của từng học viên trong lớp học hybrid.
- Các công cụ theo dõi hiện tại còn rời rạc, chưa tích hợp chặt chẽ với quy trình dạy học.
- Thiếu cơ chế cảnh báo sớm và đề xuất hỗ trợ cụ thể, dẫn đến việc hỗ trợ học viên đôi khi bị chậm trễ.

### 3. Đề xuất giải pháp ban đầu
- Xây dựng một hệ thống **AI Support Radar** tự động thu thập và phân tích tín hiệu học tập của sinh viên.
- Cảnh báo sớm cho giảng viên những học viên có nguy cơ gặp khó khăn.
- Cung cấp các đề xuất hỗ trợ cụ thể để giảng viên có thể can thiệp kịp thời.




## Conversation Guide phiên bản cuối: bản đã sửa sau khi luyện.

## Practice Reflection: ba câu trả lời ở Chặng 4.

## AI Support Log: AI đã giúp gì, có điểm nào sai/hời hợt và bạn đã tự sửa thế nào.
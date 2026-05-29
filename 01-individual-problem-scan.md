# 01 — Individual Problem Scan

## Scan rộng

Minh scan 10 problems, vượt mức tối thiểu 5.

| # | Lăng kính | Problem quan sát được | Ai đang đau? | Dấu hiệu thật |
|---|---|---|---|---|
| 1 | Pain từ người khác | Chưa làm quen với nền tảng mới, khó truy cập vào học liệu | Sinh viên mới | Nhiều bạn hỏi lại link/tài liệu, mất thời gian hỏi/gỡ lỗi/lọc nhiều nguồn |
| 2 | Tốn thời gian | Canteen quá đông | Tất cả sinh viên | Phải xếp hàng 15-20 phút mỗi giờ cao điểm, nhiều người than |
| 3 | Pain từ người khác | Thiếu trợ giảng/coach nên giải đáp, hỗ trợ không kịp thời hoặc quá tải | Sinh viên | Khi nhiều bạn cùng cần hỏi/lỗi, số lượng trợ giảng ít, phải chờ lâu mới được giúp; nhiều lúc trợ giảng bận/hết ca; nhiều vấn đề phải tự tìm cách giải quyết khiến tiến độ làm bài/lab bị ảnh hưởng |
| 4 | AI có thể tốt hơn / Lặp lại | Diễn giải chi tiết các assignment | Sinh viên, trợ giảng | Nhiều bạn cần giải thích kỹ lặp lại, tốn thời gian mỗi kỳ |
| 5 | Pain từ người khác | Chưa có kênh thống nhât, chính thức để kết nối sinh viên | Sinh viên | Chủ yếu kết nối qua group tự phát, thông tin phân tán, khó tìm bạn cùng lớp, cùng mối quan tâm |
| 6 | Pain từ người khác / AI có thể tốt hơn | Nhắc nhở deadline chưa hiệu quả, dễ bỏ lỡ bài nộp | Sinh viên | Có trường hợp bị trừ điểm hoặc xin nộp muộn do quên, thông báo bị trôi giữa kênh |
| 7 | Pain từ người khác / AI có thể tốt hơn | Giao diện hệ thống học tập/điểm danh/phản hồi chưa thân thiện | Sinh viên, nhất là ít dùng công nghệ | Nhiều bạn thao tác sai, gặp lỗi, phải hỏi hướng dẫn hoặc gửi sai/không biết feedback |

## Top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---|---|---|---|
| 1 | Chưa làm quen với nền tảng mới, khó truy cập vào học liệu | Nhiều người đau | Có thể một phần do cá nhân chủ động chưa đủ, hoặc đã có tài liệu nhưng trình bày/phân phối chưa hợp lý |
| 2 | Thiếu trợ giảng/coach nên giải đáp, hỗ trợ không kịp thời hoặc quá tải | Vấn đề này lặp lại nhiều, nhiều người đau | Quality improvement khó đo |
| 3 | Nhắc nhở deadline chưa hiệu quả, dễ bỏ lỡ bài nộp | Ảnh hưởng trực tiếp đến điểm số của sinh viên, quan trọng | Vấn đề phổ biến tới mức nào còn tùy từng lớp |


Problem 1 câu:
Sinh viên mới chưa làm quen với nền tảng, khó truy cập học liệu.

Actor:
Sinh viên mới nhập học

Thời điểm / bối cảnh:
Tuần đầu nhập học; khi nhận thông báo/tài liệu từ nhiều kênh

Current workflow 3-7 bước:
1. Nhận thông báo hoặc link tài liệu từ email/LMS/group chat.
2. Cố gắng truy cập các nền tảng khác nhau (LMS, cloud, group).
3. Nếu không tìm được đúng file hoặc bị lỗi, hỏi lại bạn bè/trao đổi nhóm.
4. Thử các link khác hoặc hỏi trợ giảng/thầy cô.
5. Đợi hỗ trợ, hoặc tự bỏ qua/không sử dụng tài liệu đó.

Bottleneck:
Thao tác tìm kiếm và truy cập đúng tài liệu (nhiều nguồn, dễ nhầm/lẫn)

Impact:
Mất thời gian, dễ bị thiếu tài liệu, chậm tiến độ học hoặc lỡ kiến thức quan trọng

Success metric:
- Giảm số lần/lượt hỏi lại hoặc nhờ trợ giúp về tài liệu
- Thời gian trung bình để truy cập đúng tài liệu < 5 phút
- 100% sinh viên lấy được đủ tài liệu đúng thời hạn

Non-AI alternative:
Chuẩn hóa 1 kênh tài liệu, hướng dẫn tập trung khi nhập học, checklist in giấy

AI hypothesis:
Dùng AI tìm kiếm/lọc học liệu theo truy vấn tự nhiên; AI gợi ý tài liệu phù hợp cho từng môn/học sinh

Quick gut:
[ ] No AI / process fix  
[ ] Rule  
[X] Workflow  
[ ] Agent  
[ ] Chưa biết  

### Draft current workflow

```text
CURRENT WORKFLOW (Tổng: ~20-40 phút)

[Nhận thông báo] (1 phút)
      ↓
[Truy cập nhiều nền tảng LMS/cloud/group] (5-10 phút)
      ↓
[Không tìm được/hỏng link?]——→[Hỏi bạn/nhóm] (5-10 phút chờ/lần hỏi)
      ↓                                  ↓
   [Tự mò/đợi hỗ trợ] (5-15 phút)    [Nhận hướng dẫn/trợ giúp] (5 phút)
      ↓
[Có/không tìm ra tài liệu]
```

### Draft future workflow

```text
FUTURE STATE (Tổng: ~3-5 phút)

[Nhận 1 thông báo tổng hợp] (1 phút)
      ↓
[Click vào portal học liệu duy nhất] (1 phút)
      ↓
[AI gợi ý tài liệu phù hợp cá nhân] (1 phút)
      ↓
[Nếu vẫn gặp lỗi, hỏi AI FAQ/chatbot] (1-2 phút)
      ↓
[Truy cập đúng tài liệu ngay]
```

Problem 2 câu:
Thiếu trợ giảng/coach nên giải đáp, hỗ trợ không kịp thời hoặc quá tải

Actor:
Sinh viên trong giờ học, làm lab, làm assignment

Thời điểm / bối cảnh:
Các phiên thực hành/lab, cao điểm deadline hoặc khi nhiều bạn gặp lỗi cùng lúc

Current workflow 3-7 bước:
1. Sinh viên làm bài/lab, assignment
2. Khi gặp vấn đề thì hỏi trợ giảng/coach hoặc group chat hỗ trợ
3. Chờ trợ giảng tới hỗ trợ trực tiếp hoặc nhắn trả lời
4. Nếu đông người hỏi cùng lúc thì phải tự mò hoặc chờ lâu
5. Nhiều lỗi nhỏ không được giải đáp kịp thời, ảnh hưởng đến tiến độ chung

Bottleneck:
Coach/trợ giảng không đủ, thời gian chờ hỗ trợ quá lâu

Impact:
- Dễ nản/gián đoạn học tập
- Sản phẩm/bài làm kém chất lượng
- Ảnh hưởng tinh thần và kết quả nhóm

Success metric:
- Tăng số lượt được giải đáp trực tiếp < 5 phút/lần hỏi
- Giảm tỷ lệ lỗi không được giải quyết trong buổi lab
- Sinh viên hài lòng với tốc độ hỗ trợ

Non-AI alternative:
Bố trí thêm trợ giảng/coach, chia ca trực rõ ràng, chuẩn hóa tài liệu FAQ

AI hypothesis:
AI assistant/FAQ tự động giải đáp các lỗi phổ biến, phân loại câu hỏi tự động, đề xuất hướng giải quyết real-time

Quick gut:
[ ] No AI / process fix  
[ ] Rule  
[ ] Workflow  
[X] Agent  
[ ] Chưa biết  

### Draft current workflow

```text
CURRENT WORKFLOW (Tổng: ~10-30 phút)

[Sinh viên làm lab/assignment] (Thời gian làm tuỳ bài)
         ↓
[Phát sinh vấn đề/lỗi] (—)
         ↓
[Hỏi trợ giảng/coach, nhắn group] (1 phút)
         ↓
    /               \
[Hỏi khi vắng/bận] (chờ 10–20 phút)  [Được giúp kịp] (2-5 phút)
  ↓                                   ↓
[Tự mò hoặc chờ lâu] (10–20 phút)  [Giải quyết nhanh] (1–2 phút)
  ↓
[Tiến độ bị ảnh hưởng]
```

### Draft future workflow

```text
FUTURE STATE (Tổng: ~2-6 phút)

[Sinh viên làm lab/assignment]
         ↓
[Gặp lỗi/thắc mắc]
         ↓
[Hỏi AI trợ lý (FAQ/bot hỗ trợ real-time)] (1 phút )
         ↓
/                       \
[AI giải quyết được] (1–2 phút)      [Câu hỏi phức tạp/ngoài danh mục]
          ↓                         ↓
     [Xử lý xong]                 [Trao cho trợ giảng/coach, ưu tiên] (3-5 phút)
          ↓                         ↓
    [Tiếp tục học/làm]            [Giải đáp nhanh cho các case đặc biệt]
```

Problem 3 câu:
Nhắc nhở deadline chưa hiệu quả, dễ bỏ lỡ bài nộp

Actor:
Sinh viên các lớp có nhiều deadline song song

Thời điểm / bối cảnh:
Trong học kỳ có nhiều assignment/milestone, thông báo trên nhiều nền tảng

Current workflow 3-7 bước:
1. Nhận thông báo deadline qua nhiều kênh khác nhau (mail, LMS, chat group)
2. Tự ghi vào sổ tay/app lịch hoặc chỉ nhớ trong đầu
3. Quá tải thông tin hoặc quên deadline vì thông báo bị trôi
4. Đến gần deadline hoặc quá hạn mới phát hiện
5. Xin gia hạn/nộp muộn hoặc bị trừ điểm

Bottleneck:
Không có hệ thống nhắc việc tập trung, dễ sót/thừa quá nhiều thông báo

Impact:
- Tỉ lệ nộp muộn tăng
- Lo lắng căng thẳng cho sinh viên
- Ảnh hưởng điểm số và đánh giá

Success metric:
- Giảm tỉ lệ sinh viên nộp muộn xuống <5%
- Sinh viên tự tin quản lý deadline, biết trước ít nhất 24h
- Thông báo tập trung, dễ theo dõi

Non-AI alternative:
Tập trung thông báo vào 1 kênh duy nhất, dán lịch ở phòng học, checklist giấy

AI hypothesis:
AI nhắc lịch thông minh tích hợp đa kênh, tự động tổng hợp và push nhắc trước deadline phù hợp bài từng cá nhân

Quick gut:
[ ] No AI / process fix  
[ ] Rule  
[X] Workflow  
[ ] Agent  
[ ] Chưa biết  

### Draft current workflow

```text
CURRENT WORKFLOW (Tổng: ~5-10 phút mỗi môn/tuần, nhưng dễ lỡ hạn)

[Nhận thông báo từ nhiều kênh] (2 phút)
      ↓
[Tự ghi lại hoặc nhớ trong đầu] (3 phút)
      ↓
[Thông báo bị trôi/quá tải]
      ↓
[Quên hoặc lỡ deadline] (mất thời gian xin lại/quản lý điểm)
      ↓
[Phải xin nộp muộn hoặc bị trừ điểm]
```

### Draft future workflow

```text
FUTURE STATE (Tổng: ~2 phút/môn mỗi tuần, rất khó lỡ hạn)

[Hệ thống deadline tập trung tự động] (—)
          ↓
[AI tổng hợp & gửi nhắc riêng] (tự động, 0 phút sinh viên thao tác)
          ↓
[Nhắc trước deadline (1-3 ngày) + hôm hạn chót] (30 giây xác nhận)
          ↓
[Sinh viên nhận thông báo, xác nhận đã xem] (1 phút)
          ↓
[Điền bài/nộp đúng hạn, nhắc lại nếu thiếu] (1 phút nộp)
---

# 02 — Group Problem Statement

## Group convergence

Nhóm 3-4 người, mỗi người share top 3. Tổng cộng khoảng 9-12 candidates.

| Cluster | Candidate examples | Pattern chung |
|---|---|---|
| Báo cáo / tổng hợp thông tin | Weekly Report, meeting recap, lab progress summary | Gom thông tin từ nhiều nguồn rồi viết lại cho người khác đọc |
| Tìm kiếm / hỏi đáp tài liệu | Slack Search, LMS Search, FAQ lab | Tìm đúng thông tin trong nhiều nguồn rời rạc |
| Review / feedback | Review PRD, check Problem Statement, review assignment | Đọc bản nháp và chỉ ra thiếu sót |
| Planning / follow-up | Action item tracking, deadline reminder | Sau cuộc họp/lab có nhiều việc bị rơi |

## Shortlist và score

| Candidate | Actor rõ | Workflow rõ | Pain có evidence | Impact đo được | Làm trong lab | So sánh R/W/A được | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Weekly Report | 5 | 5 | 4 | 5 | 5 | 5 | 5 | 34 |
| Slack Search | 4 | 4 | 4 | 4 | 3 | 4 | 4 | 27 |
| Review PRD | 4 | 5 | 3 | 3 | 5 | 4 | 4 | 28 |

Nhóm chọn: **Weekly Report**.

Vì sao chọn:

- Có workflow rõ nhất.
- Có baseline thời gian.
- Có thể validate nhanh với các PM khác.
- Có thể research các tool/pattern có sẵn.
- Có thể vẽ before/after rất rõ.

Vì sao không chọn các bài khác:

- Slack Search: impact rộng nhưng data access phức tạp, dễ trượt sang hệ thống search/agent quá lớn.
- Review PRD: workflow rõ nhưng quality metric khó thống nhất trong thời gian lab.

## Quick validation

Nhóm hỏi nhanh 3 PM/PO quen biết.

| Nguồn | Số người | Tín hiệu xác nhận | Tín hiệu phản bác | Nhóm sửa problem thế nào |
|---|---:|---|---|---|
| Quick interview | 3 | 2/3 người viết weekly/monthly update thủ công; đều đau ở phần narrative | 1 người nói dashboard đã đủ cho team của họ | Thu hẹp problem: không phải "report automation", mà là "draft narrative từ data có sẵn" |
| Mini poll trong lớp | 6 | 4/6 từng phải tổng hợp report/update từ nhiều nguồn | Một số report không cần AI, chỉ cần template | Thêm non-AI alternative: template + dashboard |

Insight sau validation:

```text
Pain thật không nằm ở việc "lấy số" đơn thuần. Pain nằm ở đoạn biến nhiều nguồn rời rạc thành narrative đủ rõ cho người khác ra quyết định.
```

## Research giải pháp

Nhóm tìm các hướng đã có sẵn, không giả định phải tự build từ đầu.

| Nguồn / tool / case | Link | Họ giải quyết phần nào? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| Atlassian Jira Reports | https://www.atlassian.com/software/jira/features/reports | Dashboard/report từ Jira data | Tốt cho số liệu structured | Không tự viết business narrative theo context Slack/Sheets | Rule/dashboard đủ cho bước lấy số, chưa đủ cho narrative |
| Slack AI | https://slack.com/help/articles/25076892548883-Guide-to-Slack-AI | Summary/search trong Slack | Tốt cho recap conversation | Chỉ là một nguồn, không gom toàn bộ Jira/Sheets/Docs | Có thể dùng như input cho workflow, không phải toàn bộ solution |
| Gemini in Drive | https://support.google.com/drive/answer/15141241 | Update/summarize nội dung file | Tốt cho tóm tắt tài liệu | Cần kiểm nguồn, không nên tự gửi output | AI draft cần người thật review |
| Fellow AI Meeting Notes | https://fellow.ai/features/ai | Meeting notes, action items, summaries | Tốt cho recap có cấu trúc | Không trực tiếp giải bài toán Jira/Sheets weekly report | Pattern tốt: AI draft, người thật review |

Research takeaway:

```text
Không nên build một agent tự chạy toàn bộ báo cáo ngay. Hướng hợp lý hơn là Workflow: tự động lấy/cấu trúc dữ liệu ở các bước rõ, dùng AI để draft narrative, PM review trước khi gửi.
```

## Workflow before/after

File nhóm nộp kèm:

```text
02-group-problem-statement-workflow.png/pdf/md
```

Nội dung workflow:

```text
CURRENT STATE — 7 bước, 90 phút

[1 Export Jira: 10']
→ [2 Lấy metrics từ Sheets: 10']
→ [3 Đọc Slack recap: 15']
→ [4 Tổng hợp vào Docs: 15']
→ [5 Viết narrative: 25']  <-- bottleneck
→ [6 Review + format: 10']
→ [7 Gửi email: 5']

FUTURE STATE — 5 bước, 21 phút

[1 Auto-pull Jira/Sheets: 2']  -- Rule/script
→ [2 AI cấu trúc input: 1']    -- Workflow step
→ [3 AI draft narrative: 1']   -- Workflow step
→ [4 PM review + edit: 15']    -- Human boundary
→ [5 PM gửi: 2']

Fallback:
AI draft sai hoặc nhạt → PM bỏ draft và tự viết lại.

Bottleneck mới:
PM review + edit. Đây là bottleneck chấp nhận được vì đó là điểm kiểm soát chất lượng.
```

Before/after impact:

| Metric | Trước | Sau kỳ vọng | Ghi chú |
|---|---:|---:|---|
| Tổng thời gian | 90 phút | Dưới 30 phút | Target chính |
| Số bước | 7 | 5 | Không chỉ giảm bước, mà giảm effort ở bước viết |
| Bước thủ công | 7/7 | 2/5 | PM vẫn review và gửi |
| Bottleneck chính | Viết narrative | Review/edit | Human boundary |
| Risk mới | Không có AI hallucination | Có hallucination risk | Cần review trước khi gửi |

## Problem Statement v0

| Field | Nội dung |
|---|---|
| **Actor** | Junior PM chịu trách nhiệm viết weekly report cho leadership. |
| **Workflow** | Mỗi tuần PM export Jira, lấy metrics từ Sheets, đọc Slack recap, tổng hợp vào Docs, viết narrative, review và gửi email. |
| **Bottleneck** | Bước viết narrative mất khoảng 25 phút vì PM phải tự biến raw data thành insight, highlight, risk và next action. |
| **Impact** | Tổng workflow mất khoảng 90 phút/tuần cho 1 PM; report dễ trễ deadline; leadership thiếu context trước sync. |
| **Success Metric** | Giảm tổng thời gian từ 90 phút xuống dưới 30 phút; không tăng số câu hỏi sửa/hỏi lại từ CEO/EM. |
| **Boundary** | Không tự gửi report; không tự bịa insight; không thay PM quyết định nội dung cuối; chỉ dùng data được cung cấp. |

## Rule / Workflow / Agent

| Mức | Phương án | Khi nào đủ | Rủi ro | Chọn? |
|---|---|---|---|---|
| **Rule** | Template report, auto-pull Jira/Sheets, fixed dashboard | Đủ nếu leadership chỉ cần số liệu | Không giải quyết narrative mỗi tuần khác nhau | Không chọn làm toàn bộ, nhưng dùng cho bước lấy số |
| **Workflow** | Script lấy data → AI cấu trúc → AI draft narrative → PM review | Hợp vì workflow tuyến tính, AI chỉ hỗ trợ vài bước ngôn ngữ | Draft sai/nhạt, cần PM review | Chọn |
| **Agent** | Agent tự lấy nhiều nguồn, phân tích, hỏi thêm, gửi report | Chỉ cần nếu workflow nhiều nhánh, nhiều tool, tự quyết bước tiếp theo | Quá rộng, nhiều permission/risk | Chưa chọn |

Mức chọn:

```text
Workflow.
```

Vì sao:

- Data collection có thể dùng rule/script.
- Narrative cần AI hỗ trợ ngôn ngữ và tổng hợp.
- PM vẫn review nên risk kiểm soát được.
- Chưa cần agent vì workflow không cần tự lập kế hoạch động.

## Problem Statement v1

| Field | Nội dung |
|---|---|
| **Actor** | Junior PM chịu trách nhiệm weekly report cho leadership. |
| **Workflow** | Export Jira → lấy metrics Sheets → đọc Slack → tổng hợp → viết narrative → review → gửi. |
| **Bottleneck** | Viết narrative từ raw data mất 25 phút và dễ trễ deadline. |
| **Impact** | Khoảng 90 phút/tuần/PM; report trễ làm leadership thiếu context. |
| **Success Metric** | Giảm tổng thời gian xuống dưới 30 phút; không tăng số câu hỏi sửa/hỏi lại từ leadership. |
| **Boundary** | AI không tự gửi report, không tự bịa số liệu, không thay PM approve. |
| **AI intervention point** | Sau khi data từ Jira/Sheets/Slack được gom lại, trước bước PM viết narrative. |
| **Mức chọn** | Workflow: rule/script lấy data, AI draft narrative, PM review. |
| **Rủi ro & người thật kiểm tra** | Risk: hallucination, bỏ sót insight, narrative nhạt. Người thật review: PM phải kiểm số liệu và edit trước khi gửi. |

## Final decision

Decision:

```text
Go với scope nhỏ.
```

Pilot nhỏ nhất:

- Dùng data mẫu từ 2 tuần report gần nhất.
- Chạy workflow bán thủ công: PM paste Jira/Sheets/Slack summary vào prompt chuẩn.
- AI draft narrative.
- PM đo thời gian edit và số lỗi phải sửa.

Exit / rollback:

- Nếu PM vẫn phải viết lại hơn 70% draft trong 2 tuần liên tiếp, hạ xuống template + dashboard.
- Nếu AI bịa số liệu hoặc trích sai nguồn, không cho dùng trực tiếp trong report.

Decision rationale:

- Problem rõ, workflow rõ, metric rõ.
- Có non-AI components.
- AI nằm ở một bước cụ thể, không ôm toàn bộ workflow.
- Human review rõ.

---

# 03 — Individual Reflection Example

## Đóng góp của Minh trong nhóm

| Hoạt động | Minh đã làm gì? | Kết quả |
|---|---|---|
| Scan cá nhân | Đưa ra 10 problems | Nhóm có nhiều candidate về reporting/workflow |
| Pitch | Pitch Weekly Report | Bài được vào shortlist |
| Challenge | Hỏi nhóm Slack Search có data access không | Nhóm loại bớt scope quá rộng |
| Workflow | Vẽ current/future workflow weekly report | Nhóm dùng làm workflow bản cuối |
| Research | Tìm Atlassian Jira Reports, Slack AI, Gemini Drive, Fellow | Nhóm thấy không cần build agent từ đầu |
| Rule / Workflow / Agent | Lập luận chọn Workflow, không chọn Agent | Nhóm thống nhất decision |

## Bảng dùng AI trong reflection

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai/hời hợt ở đâu? | Tôi sửa gì |
|---|---|---|---|---|
| Scan | Gợi ý thêm problems theo role PM | Giúp nhớ thêm Slack Search, PRD Review | Gợi ý vài ý quá rộng | Bỏ các ý không có workflow thật |
| Workflow | Nhờ AI chuyển mô tả thành Mermaid | Nhanh hơn khi vẽ flow | AI gộp bước viết narrative và review | Tách lại vì bottleneck nằm ở narrative |
| Research | Tìm tool tương tự | Gợi ý Jira, Slack AI, Gemini, Fellow | Có claim tiết kiệm thời gian không nguồn | Chỉ giữ link tool chính thức, không dùng số liệu không verify |
| Problem Statement | Nhờ AI phản biện field mơ hồ | Chỉ ra metric quality yếu | AI đề xuất agent quá sớm | Nhóm hạ về Workflow |

## Bài học của Minh

- Problem tốt không phải problem nghe "AI" nhất, mà là problem có workflow và metric rõ.
- Vẽ workflow giúp thấy phần nào rule đủ, phần nào AI mới có ích.
- Agent không phải đích đến mặc định. Trong case này, Workflow hợp lý hơn vì có đường đi cố định và có PM review.
- Research không phải để copy tool, mà để thấy pattern: nhiều sản phẩm tốt đều để AI draft, người thật review.

Nếu làm lại:

```text
Tôi sẽ validate với nhiều PM hơn trước khi chốt metric 90 phút → 30 phút, vì baseline hiện tại chủ yếu đến từ trải nghiệm của tôi.
```

---

*Ví dụ bản nộp — Day 02 Lab v2*

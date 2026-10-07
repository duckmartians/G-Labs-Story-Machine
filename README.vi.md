<h1 align="center">G-Labs Story Machine</h1>

<p align="center"><b>Ứng dụng desktop biến một chủ đề, một kịch bản hay một file phụ đề thành video phong cách phim tài liệu: AI viết và lên cảnh, G-Labs Studio tạo ảnh và video, còn bạn duyệt từng bước trước khi render bản cuối.</b></p>

<p align="center">
  <a href="README.md">English</a> ·
  <b>Tiếng Việt</b>
</p>

<p align="center">
  <a href="https://github.com/duckmartians/G-Labs-Story-Machine/releases/latest"><img alt="Tải về cho Windows" src="https://img.shields.io/badge/T%E1%BA%A3i%20v%E1%BB%81-Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white"></a>&nbsp;
  <a href="https://github.com/duckmartians/G-Labs-Story-Machine/releases/latest"><img alt="Tải về cho macOS (Apple Silicon)" src="https://img.shields.io/badge/T%E1%BA%A3i%20v%E1%BB%81-macOS%20Apple%20Silicon-000000?style=for-the-badge&logo=apple&logoColor=white"></a>&nbsp;
  <a href="https://github.com/duckmartians/G-Labs-Story-Machine/releases/latest"><img alt="Tải về cho macOS (Intel)" src="https://img.shields.io/badge/T%E1%BA%A3i%20v%E1%BB%81-macOS%20Intel-555555?style=for-the-badge&logo=apple&logoColor=white"></a>
</p>

---

## Cài đặt

### Bước 1 - Chọn đúng bản cho máy của bạn

Tải bản mới nhất từ **[Releases](https://github.com/duckmartians/G-Labs-Story-Machine/releases/latest)**, rồi chọn tệp theo đúng máy (`<version>` là số phiên bản, ví dụ `2.0.6`):

| Máy của bạn | Tải tệp | Ghi chú |
|---|---|---|
| 🪟 **Windows 10/11 (64-bit)** | [`StoryMachine-<version>-setup.exe`](https://github.com/duckmartians/G-Labs-Story-Machine/releases/latest) | Trình cài đặt cho mọi PC Windows |
| 🍎 **Mac chip Apple (M1/M2/M3/M4)** | [`StoryMachine-<version>-arm64.dmg`](https://github.com/duckmartians/G-Labs-Story-Machine/releases/latest) | macOS 12 trở lên |
| 🍎 **Mac chip Intel** | [`StoryMachine-<version>-intel.dmg`](https://github.com/duckmartians/G-Labs-Story-Machine/releases/latest) | Mac đời cũ |

**Không chắc Mac của bạn chip gì?** Bấm biểu tượng  ở góc trên bên trái → **About This Mac**:
- Có dòng **Chip** ghi "Apple M1 / M2 / M3…" → tải bản **arm64**.
- Có dòng **Processor** ghi "Intel…" → tải bản **intel**.

> Tải nhầm bản **Intel** cho máy chip Apple thì vẫn chạy được (qua Rosetta, chậm hơn); còn tải nhầm bản **arm64** cho máy Intel sẽ **không mở được**. Nên chọn đúng.

### Bước 2 - Cài đặt

<details open>
<summary><b>🪟 Trên Windows</b></summary>

1. Mở tệp **`StoryMachine-<version>-setup.exe`** vừa tải.
2. Nếu hiện bảng **"Windows protected your PC"** (SmartScreen): bấm **More info** → **Run anyway**. *(App chưa mua chứng chỉ ký của Microsoft nên bị cảnh báo - không phải virus.)*
3. Làm theo trình cài đặt - giữ thư mục mặc định hoặc chọn thư mục khác. Lối tắt trên Desktop và Start Menu được tạo sẵn.
4. Mở **G-Labs Story Machine** từ **Start Menu** hoặc lối tắt trên **Desktop**.

</details>

<details open>
<summary><b>🍎 Trên macOS</b></summary>

1. Mở tệp **`.dmg`** vừa tải, rồi **kéo biểu tượng G-Labs Story Machine thả vào thư mục Applications**.
2. Vào **Applications**, **bấm chuột phải** (hoặc giữ Control rồi bấm) lên **G-Labs Story Machine** → chọn **Open** → bấm **Open** lần nữa ở hộp xác nhận. *(App chưa được Apple ký nên phải mở kiểu này ở **lần đầu**; những lần sau mở bình thường như mọi app.)*
3. Nếu macOS báo **"bị hỏng / không thể mở"** hoặc không thấy nút Open, mở **Terminal** và dán lệnh sau rồi Enter:
   ```bash
   xattr -dr com.apple.quarantine "/Applications/G-Labs Story Machine.app"
   ```
   Sau đó mở lại app.

</details>

FFmpeg đã đóng gói sẵn trong cả hai bản - không cần cài thêm gì.

### Bước 3 - Đăng nhập (tặng kèm gói MAX của G-Labs)

**Story Machine không bán riêng.** App mở cho **tài khoản của bạn có gói MAX còn hạn**: đăng nhập Google bằng chính tài khoản đó, máy chủ bản quyền kiểm tra gói mỗi lần. Gói MAX mua qua G-Labs Studio, Auto Flow hay Auto Vibes đều là gói trên cùng tài khoản của bạn. Nếu tài khoản chưa có MAX, app hiện **"Cần gói MAX"** - gia hạn hoặc nâng cấp rồi bấm **Thử lại**.

- **Storyteller** mở cho mọi tài khoản MAX.
- Chế độ **Editor** và hướng kể chuyện **Thế giới động vật** mở riêng theo từng tài khoản. Khi chưa mở, thẻ Editor hiện **"Chưa mở"** và không có lựa chọn Thế giới động vật.
- App cần Internet để đăng nhập và nhận bộ prompt, và phải kiểm tra lại gói ít nhất mỗi **72 giờ**. Hết hạn gói thì app khoá lại; dự án trên máy vẫn giữ nguyên.

Ứng dụng **tự cập nhật**: nó kiểm tra GitHub Releases và tải bản mới ngay trong app - trên Windows nó chạy trình cài đặt mới, trên macOS nó mở tệp `.dmg` mới để bạn kéo vào Applications.

### Cần chuẩn bị thêm

Story Machine là bộ điều phối, không tự tạo ảnh/video/giọng. Trước dự án đầu tiên, bạn cần:

- **Một nhà cung cấp LLM** - Claude CLI, Antigravity CLI, Codex CLI (đã đăng nhập trên máy) hoặc 9Router.
- **[G-Labs Studio](https://github.com/duckmartians/G-Labs-Studio)** đang chạy với Webhook API - để tạo ảnh và video.
- **G-Labs Voiceover** hoặc **G-Labs Voice Studio** - để đọc lời bình (không cần nếu bạn bắt đầu từ file `.srt` hoặc nạp file thuyết minh của mình).

---

## Lần chạy đầu tiên

1. **Mở ứng dụng và đăng nhập bằng Google** với tài khoản của bạn có gói MAX.
2. **Chọn chế độ** ở màn hình đầu - **Storyteller** (video kể chuyện / tài liệu) hoặc **Editor** (cắt dựng video bất kỳ, nếu đã mở).
3. **Mở Cài đặt** (thanh bên trái) và nối công cụ: chọn nhà cung cấp LLM, rồi dán địa chỉ webhook + API key của G-Labs Studio (ảnh/video) và của Voiceover hoặc Voice Studio (giọng đọc).
4. **Đặt đề bài ở trang Thiết lập**: chọn cách bắt đầu (chủ đề, kịch bản, phụ đề hoặc storyboard), rồi tỉ lệ khung, thời lượng, ngôn ngữ đầu ra, giọng điệu và phong cách ảnh.
5. **Đi qua từng trang** - Cốt truyện → Phân tích → Tạo ảnh → Tạo video → Giọng đọc → Tối ưu SEO → Render. Ở mỗi trang bạn sửa, tạo lại hoặc nạp file của mình trước khi sang bước sau.
6. **Render** ra MP4 hoàn chỉnh (video hoặc slideshow), hoặc **Xuất CapCut** để chỉnh tay.

---

## Tính năng

![G-Labs Story Machine](docs/media/vi/images.webp)

- **Bốn cách bắt đầu** - từ **chủ đề** (AI tự nghiên cứu, viết cốt truyện và toàn bộ lời bình), từ **kịch bản** của bạn (tự chia câu và đọc thành giọng), từ **phụ đề** `.srt` (mốc thời gian của file quyết định từng cảnh, không cần tạo giọng), hoặc từ **storyboard** - kịch bản thoại, nhân vật nhất quán bằng ảnh tham chiếu.
- **Hai chế độ chạy** - **Chất lượng cao** (qua ảnh từng cảnh) và **Tạo nhanh** (thẳng chữ → video, bỏ bước ảnh; nhanh, tiết kiệm).
- **Mỗi bước một trang** - từng bước của quy trình là một trang riêng để bạn xem lại, sửa, tạo lại hoặc nạp ảnh/clip của mình trước khi đi tiếp.
- **Ba hướng dựng hình** - có nhân vật xuất hiện, minh hoạ không người, hoặc **phim tài liệu thế giới động vật** chỉ có động vật (khi đã mở).
- **Hơn 40 phong cách ảnh mẫu** - hoặc tự mô tả phong cách rồi lưu lại dùng sau.
- **Dịch & biên tập** - dịch hoặc trau chuốt kịch bản/phụ đề bằng LLM trước khi sản xuất, chuyển qua lại bản gốc ↔ bản dịch.
- **Giọng đọc, nhạc nền & phòng dựng** - thanh thời gian, tự hạ nhạc nền khi có lời, hiện/tắt dần, khớp video với giọng (giữ khung cuối, lặp hoặc làm chậm), phụ đề chèn vào hình; dựng video hoặc slideshow có lia/phóng, hoặc xuất draft CapCut.
- **Tối ưu SEO** - tiêu đề, mô tả, tag và ý tưởng ảnh bìa cho YouTube.
- **Điểm khôi phục** - quay về một trạng thái trước của dự án; trước khi quay về app tạo một điểm mới, nên thao tác này cũng lùi lại được.
- **11 ngôn ngữ giao diện** - English, Tiếng Việt, हिन्दी, Türkçe, Português, 简体中文, اردو, বাংলা, Русский, Español, ไทย.

---

## Các chế độ &amp; trang

Màn hình đầu có hai chế độ. Cả hai giữ nguyên khi đã mở, nên chuyển qua lại không mất việc đang làm; nút Home đưa bạn về màn chọn.

### 🎬 Storyteller - Thiết lập

![Thiết lập](docs/media/vi/setup.webp)

Chọn cách bắt đầu - **Tạo video từ chủ đề**, **từ kịch bản**, **từ phụ đề** hoặc **từ storyboard** - và chế độ chạy (**Chất lượng cao** hoặc **Tạo nhanh**). Sau đó đặt tỉ lệ khung, thời lượng, ngôn ngữ đầu ra, giọng điệu và phong cách ảnh. Các trang tiếp theo tuỳ cách bắt đầu:

| Bắt đầu từ | Các trang |
|---|---|
| Chủ đề | Thiết lập → Cốt truyện → Phân tích → Tạo ảnh → Tạo video → Giọng đọc → Tối ưu SEO → Render |
| Kịch bản | Thiết lập → Giọng đọc → Phân tích → Tạo ảnh → Tạo video → Tối ưu SEO → Render |
| Phụ đề (`.srt`) | Thiết lập → Phân tích → Tạo ảnh → Tạo video → Tối ưu SEO → Render |
| Storyboard | Thiết lập → Kịch bản → Thành phần → Phác thảo → Tạo ảnh → Tạo video → Tối ưu SEO → Render |

### 🖼 Phân tích &amp; Tạo ảnh

![Tạo ảnh](docs/media/vi/images.webp)

LLM chia câu chuyện thành cảnh, mỗi cảnh có thời lượng và prompt riêng; ảnh được gửi tạo qua webhook của G-Labs Studio. Từng cảnh bạn sửa prompt, tạo lại, hoặc nạp ảnh của mình.

### 🎥 Tạo video

![Tạo video](docs/media/vi/videos.webp)

Biến ảnh cảnh thành clip bằng model video của G-Labs Studio, mỗi cảnh có prompt chuyển động riêng. Chọn nhanh tất cả, vài cảnh đầu/cuối, ngẫu nhiên hoặc xen kẽ để chỉ tạo video cho một phần - phần còn lại vẫn render được dạng ảnh.

### 🎞 Giọng đọc, Tối ưu SEO &amp; Render

![Render](docs/media/vi/render.webp)

Giọng đọc lấy từ G-Labs Voiceover hoặc Voice Studio, hoặc nạp file thuyết minh có sẵn. Trang **Tối ưu SEO** gợi ý tiêu đề, mô tả, tag và ý tưởng ảnh bìa. Phòng **Render** có thanh thời gian, tự hạ nhạc nền, hiện/tắt dần, khớp video với giọng và phụ đề chèn vào hình; bấm **Dựng Video**, **Dựng Slideshow** có hiệu ứng lia/phóng, hoặc **Xuất CapCut**.

### 🧩 Storyboard (nằm trong Storyteller)

Bắt đầu từ một kịch bản thoại: app trích nhân vật, bối cảnh và đạo cụ, vẽ ảnh tham chiếu cho chúng (**Thành phần**), chia kịch bản thành từng khung hình (**Phác thảo**), rồi tạo ảnh và video từng khung nhất quán.

### ✂️ Editor *(mở riêng)*

Cắt dựng video bất kỳ: kéo thả hàng loạt, cắt-tách-đổi thứ tự trên timeline có sóng âm. Tự khớp clip theo câu phụ đề, khoảng lặng dò được hoặc lưới nhịp BPM; nhạc nền tự hạ dưới giọng đọc; ảnh có pan/zoom; phụ đề burn-in chỉnh được kiểu; render xếp hàng chờ.

---

## Nơi lưu dữ liệu

| Gì | macOS | Windows |
|---|---|---|
| Dự án, ảnh, video, bản render | `~/Documents/G-Labs Story Machine/output` | `%USERPROFILE%\Documents\G-Labs Story Machine\output` |
| Cài đặt, khoá (`.env`, `settings.json`), phiên đăng nhập | `~/Library/Application Support/G-Labs Story Machine` | `%APPDATA%\G-Labs Story Machine` |

Bạn có thể đổi thư mục lưu trong **Cài đặt → Thư mục lưu output**. Nội dung câu chuyện được gửi tới nhà cung cấp LLM bạn chọn; máy chủ bản quyền chỉ dùng để đăng nhập, kiểm tra gói và gửi bộ prompt.

---

## Khắc phục sự cố

**Đăng nhập xong hiện "Cần gói MAX"** - tài khoản chưa có gói MAX còn hạn. Gia hạn hoặc nâng cấp rồi bấm **Thử lại** (app kiểm tra lại với máy chủ).

**Thẻ Editor ghi "Chưa mở" / không có lựa chọn Thế giới động vật** - hai phần này mở riêng theo tài khoản; tài khoản của bạn chưa được mở.

**"Server không phản hồi - kiểm tra webhook đã chạy chưa"** - mở G-Labs Studio (và Voiceover / Voice Studio cho giọng đọc), bật webhook, rồi kiểm tra lại địa chỉ trong Cài đặt.

**"Webhook từ chối khoá API"** - chép lại API key từ trang Webhook API của G-Labs Studio vào Cài đặt.

**Một cảnh báo webhook không còn task** - webhook đã khởi động lại hoặc task hết hạn; bấm tạo lại ở cảnh đó.

**Windows chặn ở "Windows protected your PC"** - bấm **More info → Run anyway**. App chưa mua chứng chỉ ký của Microsoft nên bị cảnh báo, không phải virus.

**macOS báo ứng dụng bị hỏng / không mở được** - app chưa được Apple ký. Chuột phải → **Open** ở lần đầu, hoặc chạy `xattr -dr com.apple.quarantine "/Applications/G-Labs Story Machine.app"`.

**Một bản cập nhật không cài được** - tải bản mới nhất thủ công từ [Releases](https://github.com/duckmartians/G-Labs-Story-Machine/releases/latest).

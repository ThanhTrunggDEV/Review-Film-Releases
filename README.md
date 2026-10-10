# Review Film Studio — Bản cài đặt Windows

Repo public chứa **file cài đặt (.exe)** của **Review Film Studio (CTDev Tool)** — ứng dụng desktop tự động tạo video review phim dài 3–15 phút từ 1 video gốc: cắt cảnh highlight đúng luật **mỗi cảnh ≤ 14s, cách nhau ≥ 8s**, viết kịch bản bằng AI, thuyết minh **OmniVoice**, phụ đề đa ngôn ngữ và dựng hoàn chỉnh bằng FFmpeg.

> 👉 **Luôn tải bản mới nhất tại:** [Releases](../../releases/latest) — file `ReviewFilm-Setup-x.y.z.exe` ở mục **Assets**.
>
> Repo code nguồn là private. Repo này chỉ đăng installer để người dùng tải và để app tự kiểm tra cập nhật.

---

## ⬇️ Tải & cài đặt

1. Vào [trang Releases](../../releases/latest), kéo xuống mục **Assets**, tải file `ReviewFilm-Setup-x.y.z.exe` mới nhất.
2. Chạy file setup → cài đặt như phần mềm Windows thông thường (không cần quyền admin).
3. Mở app **Review Film Studio** từ Start Menu / Desktop.

## 🖥️ Yêu cầu hệ thống

| Mục | Yêu cầu |
|---|---|
| Hệ điều hành | Windows 10/11 64-bit |
| Ổ cứng trống | ≥ 15 GB (app + FFmpeg + model AI tải lần đầu) |
| RAM | ≥ 8 GB (khuyến nghị 16 GB) |
| GPU | Không bắt buộc. Có NVIDIA + driver CUDA mới thì render/voice nhanh hơn; không có sẽ tự chạy CPU |
| Mạng | Cần mạng lần đầu để tải FFmpeg + model AI và khi gọi LLM cloud |

## 🚀 Lần đầu mở app

1. App hiện **dialog first-run**: tự tải **FFmpeg** và **model AI** (face/STT/OmniVoice, ~9 GB, chỉ 1 lần) — có thanh tiến trình, bấm **Để sau** được nhưng render/tải video cần đủ tài nguyên.
2. **Kích hoạt license** theo hướng dẫn trong dialog (license khóa theo máy, hạn 1 năm).
3. Vào **Cài đặt** → nhập API key LLM (OpenAI/Gemini) hoặc dùng model local → bấm **Test kết nối**.

## 🔄 Cập nhật

- Mở app → **Cài đặt → tab Cập nhật** → **Kiểm tra bản mới**. App so version với repo này và hướng dẫn tải bản mới.
- Hoặc quay lại [trang Releases](../../releases) của repo này để tải tay.

## 📝 Lịch sử phiên bản

| Phiên bản | Điểm chính |
|---|---|
| **v0.2.0** (mới nhất) | Tab CTDev Tools (giới thiệu Downloader 4K, Voice & Sub); tùy chọn nền mờ dưới phụ đề chống đè sub gốc |
| v0.1.9 | Sub căn theo voice tới mức từ (hết lệch sub/voice); gate thời lượng output; QC thời lượng; tab Cập nhật riêng |
| v0.1.8 | Tùy chọn bản GPU (CUDA cu126); fix OmniVoice + tải video yt-dlp trên bản installer; tab Log hỗ trợ gửi lỗi |
| v0.1.7 | Fix detect CUDA, trạng thái Models sau first-run, tải video bằng link trên Windows |
| v0.1.5 | Tự động cập nhật qua repo public; log lỗi tải chi tiết |

Xem chi tiết từng bản trong [trang Releases](../../releases) (mỗi bản ghi rõ “Có gì mới”).

## 🆘 Hỗ trợ

- Gặp lỗi: mở app → **Cài đặt → tab Log** → **Sao chép log** rồi gửi kèm mô tả lỗi.
- Liên hệ trong app: **Facebook** `facebook.com/nguyen.thanh.trung.323291` · **Zalo** `0971632201`.

## ⚖️ Lưu ý bản quyền

App chỉ xử lý video do bạn cung cấp (file local hoặc link công khai, không bypass DRM/login) và yêu cầu tick **cam kết bản quyền** trước khi tạo job. Luật cắt 14s/8s + bình luận transformative chỉ **giảm rủi ro Content ID**, không đảm bảo miễn trừ bản quyền — luôn tuân thủ chính sách từng nền tảng.

# VietScribe

Ứng dụng macOS chuyển video/audio **tiếng Việt** thành văn bản. Chạy hoàn toàn trên máy, không gửi dữ liệu đi đâu.

Repo này chỉ chứa **bản cài**. Mã nguồn để ở repo riêng.

## Cài đặt (1 lệnh)

Mở **Terminal**, dán lệnh dưới đây rồi nhấn Enter:

```bash
curl -fsSL https://github.com/toanhhg123/vietscribe-releases/releases/latest/download/install.sh | bash
```

Lệnh sẽ tải bản mới nhất, chép vào **Applications** rồi mở app. Lần đầu mở, app tải model nhận dạng (~34MB).

Sau đó app **tự kiểm tra và cập nhật** bản mới mỗi ngày. Bạn cũng có thể vào menu **VietScribe → Kiểm tra cập nhật…** để kiểm tra ngay.

### Hoặc cài bằng file DMG

1. Tải [VietScribe.dmg](https://github.com/toanhhg123/vietscribe-releases/releases/latest/download/VietScribe.dmg).
2. Mở file DMG, kéo **VietScribe** vào **Applications**.
3. Lần đầu mở, macOS báo không xác minh được nhà phát triển (vì app chưa ký Apple Developer ID). Khi đó vào **System Settings → Privacy & Security**, kéo xuống, bấm **Open Anyway**. Việc này chỉ cần làm một lần.

## Yêu cầu

- Mac dùng chip Apple (M1 trở lên)
- macOS 14 (Sonoma) trở lên

## Cách dùng nhanh

1. Kéo video hoặc audio vào cửa sổ, hoặc bấm ⌘O.
2. Nhận dạng xong, **toàn bộ văn bản tự động được copy vào clipboard**, bạn chỉ việc dán. Muốn copy lại thì bấm ⇧⌘C.
3. Muốn có phụ đề thì vào ⌘E để xuất SRT, WebVTT hoặc TXT.

## Ghi công

- Model nhận dạng: [hynt/Zipformer-30M-RNNT-6000h](https://huggingface.co/hynt/Zipformer-30M-RNNT-6000h), license CC BY-NC-ND 4.0, **chỉ dùng phi thương mại**.
- Runtime: [sherpa-onnx](https://github.com/k2-fsa/sherpa-onnx) (Apache-2.0).
- Tự cập nhật: [Sparkle](https://sparkle-project.org) (MIT).

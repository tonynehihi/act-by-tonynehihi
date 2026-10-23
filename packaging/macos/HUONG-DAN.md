# Acrobat by Tonynehihi — Hướng dẫn cài đặt & sử dụng

Bản build cá nhân của Tony, dựa trên PdfCraft v0.8.0 (MIT/Apache-2.0) — app đọc, sắp xếp và bảo vệ PDF viết bằng Rust, chạy offline.

Đã rebrand:
- Tên app **"Acrobat by Tonynehihi"**, icon **AcT** phong cách Adobe (nền #EC1C24)
- Menu bar macOS: About / Hide / Quit đều hiện "Acrobat by Tonynehihi"
- About dialog gọn: "Acrobat by Tonynehihi — by Tony" + version
- Bundle ID mới: `com.tony.acrobat`

## Gỡ bản cũ / cài lại sạch

**Nếu mày đã build bản trước:**
```bash
# Xóa bản build cũ
rm -rf target/
# Xóa app đã cài (nếu đã kéo vào Applications)
rm -rf "/Applications/Acrobat by Tonynehihi.app"
rm -rf "/Applications/PdfCraft.app"
```

**Xóa sạch settings/cache (nếu muốn làm lại từ đầu):**
```bash
# CẨN THẬN: xóa là mất settings, sao lưu trước nếu cần
rm -rf ~/Library/Application\ Support/Acrobat by Tonynehihi
rm -rf ~/.config/pdfcraft
```

## Cài đặt (làm 1 lần)

**Bước 1** — Cài Xcode Command Line Tools (nếu chưa có):
```
xcode-select --install
```

**Bước 2** — Cài Rust (nếu chưa có):
```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```
Xong thì **đóng Terminal, mở lại**.

## Build & đóng gói

```bash
cd ~/Downloads/acrobat-by-tony-1.0
cargo build --release -p pdfcraft
packaging/macos/package.sh
```

File `.dmg` sẽ nằm trong `dist/`. Mở dmg, kéo app vào Applications là xong.

## Nếu macOS chặn mở app (Gatekeeper)

Chuột phải vào app → **Open** → bấm **Open** lần nữa. Chỉ cần làm 1 lần đầu.

*Bản 1.0 | By Tony*

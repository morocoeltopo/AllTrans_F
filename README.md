# AllTrans

[English](README_en.md)

AllTrans là một module Xposed/LSPosed dùng để dịch văn bản bên trong ứng dụng Android theo thời gian thực.

Nó hoạt động tương tự tính năng dịch trang web trong trình duyệt, nhưng áp dụng trực tiếp cho giao diện ứng dụng. Bạn chọn ngôn ngữ cần dịch, ngôn ngữ đích, bật dịch cho ứng dụng mong muốn, rồi mở lại ứng dụng để áp dụng bản dịch.

## Tổng quan

- Tên gói: `chanhnh.alltrans`
- Phiên bản: `2.0.0`
- Min Android SDK: `29`
- Compile/target SDK: `36`
- Dịch vụ dịch:
  - `Google Translate`
  - `Microsoft Translate`

Giao diện hiện có các ngôn ngữ:

- Tiếng Anh
- Tiếng Việt
- Tiếng Trung

Cài đặt dịch mặc định:
- Dịch vụ dịch: `Google Translate`
- Dịch từ: `Tự nhận diện`
- Dịch sang: `Tiếng Việt`

## Tính năng chính

- Cài đặt dịch Toàn cục và theo từng ứng dụng
- Dịch văn bản thông thường, gợi ý văn bản, thông báo và nội dung WebView
- Chế độ mạnh cho các ứng dụng khó dịch
- Bộ nhớ đệm bản dịch có thể xóa thủ công hoặc tự động đánh dấu xóa khi đổi dịch vụ dịch
- Ghi đè cài đặt toàn cục cho từng ứng dụng

## Cách sử dụng

1. Cài module trên thiết bị có môi trường tương thích Xposed/LSPosed.
2. Bật module cho các ứng dụng bạn muốn dịch.
3. Mở AllTrans.
4. Trong tab `Toàn cục`, chọn dịch vụ dịch và ngôn ngữ mặc định.
5. Trong tab `Ứng dụng`, bật dịch cho ứng dụng cần dịch.
6. Khởi động lại ứng dụng đó.

Nếu một ứng dụng cần cài đặt riêng:

1. Mở ứng dụng đó trong danh sách `Ứng dụng`.
2. Bật `Ghi đè cài đặt toàn cục`.
3. Tùy chỉnh dịch vụ dịch, ngôn ngữ nguồn, ngôn ngữ đích và các cài đặt nâng cao riêng cho ứng dụng đó.

## Build

Dự án sử dụng:

- Gradle Android application module
- Kotlin
- Java 17 toolchain

Build debug thông thường:

```bash
./gradlew :app:assembleDebug
```

## Lưu ý

- Nhiều game vẫn sẽ không dịch đúng do cách chúng hiển thị văn bản.
- Khi đổi dịch vụ dịch, AllTrans sẽ tự đánh dấu xóa bộ nhớ đệm bản dịch.
- Mặc định ứng dụng sẽ dịch từ ngôn ngữ tự động nhận diện sang tiếng Việt.

## Giấy phép

GPL-3.0-or-later.

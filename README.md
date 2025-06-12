Hướng dẫn cài đặt TailwindCSS thủ công

Bước 1: Tạo dự án - Tạo một folder trống để chứa dự án TailwindCSS của bạn. - Mở folder đó bằng Visual Studio Code (VS Code).

Bước 2: Cài đặt TailwindCSS - Mở Terminal trong VS Code (phím tắt: Ctrl + ~) và chạy lần lượt hai lệnh sau:
// npm install -D tailwindcss@3
// npx tailwindcss init
// npm install --save-dev tailwind-scrollbar@3 - Lệnh thứ hai sẽ tạo ra file tailwind.config.js.

Bước 3: Cấu hình đường dẫn file - Mở file tailwind.config.js, sửa lại phần content như sau:
// content: ["./src/**/*.{html,js}"],
// plugins: [require("tailwind-scrollbar")({ nocompatible: true })],

Bước 4: Tạo file CSS gốc - Tạo thư mục mới tên là src.
-Bên trong src, tạo file input.css và thêm nội dung sau:
// @tailwind base;
// @tailwind components;
// @tailwind utilities; - Nếu thấy cảnh báo (warning) thì bỏ qua, không sao cả.

Bước 5: Biên dịch CSS với Tailwind - Tiếp tục trong terminal, chạy lệnh sau để Tailwind biên dịch CSS:
// npx tailwindcss -i ./src/input.css -o ./src/output.css --watch - Lệnh này sẽ tạo file output.css chứa CSS đã biên dịch. Nếu là dự án tailwind thuần thì bạn cần chạy lệnh này mỗi khi muốn chạy giao diện trên web

Xong! Bây giờ hãy mở file bằng Live Server để thấy kết quả.

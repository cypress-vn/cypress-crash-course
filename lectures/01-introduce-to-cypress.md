# Bài giảng Buổi 1: Giới thiệu về Cypress

## Mục tiêu
- Hiểu vai trò của Cypress trong kiểm thử tự động.
- Cài đặt và cấu hình môi trường Cypress.
- Chạy thử nghiệm đầu tiên với Cypress Test Runner.


## Nội dung chi tiết

### 1. Tổng quan về kiểm thử tự động và Cypress
- **Kiểm thử tự động là gì?**
  - Khái niệm: Kiểm thử tự động hóa các tác vụ kiểm tra phần mềm.
  - Lợi ích: Tiết kiệm thời gian, tăng độ chính xác, tái sử dụng test case.
  - So sánh với kiểm thử thủ công.
- **Giới thiệu Cypress**
  - Cypress là gì? Công cụ kiểm thử E2E (End-to-End) cho ứng dụng web.
  - Ưu điểm: Dễ sử dụng, chạy trực tiếp trong trình duyệt, hỗ trợ debug mạnh mẽ.
  - So sánh với Selenium: Nhanh hơn, không cần driver riêng, tập trung vào trải nghiệm người dùng.
- **Ứng dụng thực tế của Cypress**
  - Kiểm thử giao diện người dùng (UI), API, và tích hợp CI/CD.

### 2. Cài đặt môi trường (30 phút)
- **Yêu cầu trước khi cài đặt**
  - Máy tính có Node.js (phiên bản 16 trở lên) và npm.
  - Trình duyệt: Chrome hoặc Firefox (khuyến nghị Chrome).
  - Công cụ chỉnh sửa code: VS Code hoặc bất kỳ IDE nào.
- **Hướng dẫn cài đặt Cypress**
  1. Tạo một thư mục dự án mới:
     ```bash
     mkdir cypress-demo
     cd cypress-demo
     ```
  2. Khởi tạo dự án Node.js:
     ```bash
     npm init -y
     ```
  3. Cài đặt Cypress:
     ```bash
     npm install cypress --save-dev
     ```
  4. Mở Cypress Test Runner:
     ```bash
     npx cypress open
     ```
- **Giải thích cấu trúc dự án**
  - `cypress/integration`: Nơi chứa các file test (`.spec.js`).
  - `cypress/fixtures`: Lưu trữ dữ liệu mẫu (JSON, CSV...).
  - `cypress/support`: Custom commands và cấu hình.
  - `cypress.config.js`: File cấu hình chính của Cypress.

### 3. Chạy thử nghiệm đầu tiên (45 phút)
- **Viết test case mẫu**
  - Tạo file `first-test.spec.js` trong thư mục `cypress/integration`.
  - Nội dung ví dụ:
    ```javascript
    describe('My First Test', () => {
      it('Visits a website and checks title', () => {
        cy.visit('https://example.com');
        cy.title().should('eq', 'Example Domain');
      });
    });
    ```
- **Giải thích code**
  - `describe`: Nhóm các test case liên quan.
  - `it`: Một test case cụ thể.
  - `cy.visit()`: Truy cập URL.
  - `cy.title()`: Lấy tiêu đề trang web.
  - `should('eq', ...)`: Kiểm tra điều kiện (assertion).
- **Chạy test**
  - Mở Cypress Test Runner: `npx cypress open`.
  - Chọn file `first-test.spec.js` để chạy.
  - Quan sát giao diện Test Runner: Xem kết quả, log, và snapshot.

### 4. Thực hành và thảo luận (15 phút)
- **Bài tập thực hành**
  - Viết một test case kiểm tra việc truy cập trang `https://www.google.com` và xác minh tiêu đề trang chứa từ "Google".
  - Chạy test và quan sát kết quả trong Test Runner.
- **Thảo luận**
  - Những lỗi thường gặp khi cài đặt (ví dụ: thiếu Node.js, lỗi mạng).
  - Cách sử dụng tài liệu chính thức của Cypress: [https://docs.cypress.io](https://docs.cypress.io).
  - Câu hỏi từ học viên.

## Tài liệu cần chuẩn bị
- Laptop đã cài Node.js, npm, và trình duyệt Chrome/Firefox.
- Tài liệu tham khảo: [Cypress Getting Started](https://docs.cypress.io/guides/getting-started/installing-cypress).
- Ứng dụng web mẫu: Sử dụng `https://example.com` hoặc `https://www.google.com`.

## Kết quả đầu ra
- Học viên hiểu được vai trò của Cypress và quy trình kiểm thử tự động.
- Cài đặt thành công môi trường Cypress.
- Chạy được test case đầu tiên và hiểu cách sử dụng Test Runner.
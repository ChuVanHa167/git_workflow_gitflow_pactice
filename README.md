# git_workflow_gitflow_pactice

## Giả sử dự án
Một công ty đang phát triển **website thương mại điện tử lớn**.
Dự án có nhiều lập trình viên và cần:
* phát triển nhiều tính năng song song
* có môi trường test trước khi release
* có khả năng sửa lỗi production nhanh
Nhóm quyết định sử dụng **Gitflow Workflow**.

## Các branch chính
Gitflow có 2 branch quan trọng:
main
dev
Ý nghĩa:
main → code production (code đang chạy thật)
dev → code đang phát triển

## Các branch phụ
feature/* → phát triển tính năng
release/* → chuẩn bị phát hành
hotfix/* → sửa lỗi production

## Cấu trúc branch
main
│
dev
├── feature/login
├── feature/product-page
└── feature/cart

Sau khi hoàn thành feature:
feature → merge → dev
Sau khi chuẩn bị phát hành:
dev → release/v1.0.0 → main
Nếu production có lỗi:
main → hotfix/v1.0.1 → main & dev

## Workflow tổng thể
main
↓
dev
↓
feature
↓
dev
↓
release
↓
main

Nếu có lỗi production:
main → hotfix → main & dev

## Mục đích repo
Repo này dùng để thực hành:
* tạo dev branch
* tạo feature branch
* merge feature → dev
* tạo release branch
* merge release → main
* tạo hotfix

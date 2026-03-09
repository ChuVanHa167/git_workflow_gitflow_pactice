# git_workflow_gitflow_pactice

_**Giả sử dự án**_
Một công ty đang phát triển _website thương mại điện tử lớn_.

_**Dự án có nhiều lập trình viên và cần:**_
* phát triển nhiều tính năng song song
* có môi trường test trước khi release
* có khả năng sửa lỗi production nhanh

Nhóm quyết định sử dụng **Gitflow Workflow**.

_**Các branch chính**_
main
dev

_**Ý nghĩa:**_
main → code production (code đang chạy thật)
dev → code đang phát triển

_**Các branch phụ**_
feature/* → phát triển tính năng
release/* → chuẩn bị phát hành
hotfix/* → sửa lỗi production

_**Cấu trúc branch**_
```
main
│
dev
├── feature/login
├── feature/product-page
└── feature/cart
```
_**Sau khi hoàn thành feature:**_
feature → merge → dev
_**Sau khi chuẩn bị phát hành:**_
dev → release/v1.0.0 → main
Nếu production có lỗi:
main → hotfix/v1.0.1 → main & dev

_**Workflow tổng thể**_
```
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
```
_**Nếu có lỗi production:**_
main → hotfix → main & dev
* tạo feature branch
* merge feature → dev
* tạo release branch
* merge release → main
* tạo hotfix

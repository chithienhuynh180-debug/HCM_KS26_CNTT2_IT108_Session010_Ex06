# Bài: Plain Text và Rich Text trong dự án GreenTech

## Phần 1. Phân tích

### Sai lầm của Nam

1. **Dùng file Rich Text (.docx) để lưu tài liệu trên GitHub.** File .docx là dạng nhị phân nén nên trình duyệt không xem trực tiếp được, các bạn trong nhóm không đọc được nội dung.
2. **Không biết Git chỉ so sánh tốt với văn bản thô.** Git so sánh theo từng dòng chữ. File .docx là nhị phân nên sửa 1 dấu phẩy cũng làm cả file thay đổi, Git báo Conflict toàn bộ và Git Diff không chỉ ra được dòng nào bị sửa.
3. **Không tính đến rủi ro hỏng file.** File .docx chỉ cần mất 1 byte khi tải lỗi mạng là hỏng hoàn toàn, không mở được.

### Tại sao Markdown an toàn và nhẹ hơn

| Tiêu chí | Word (.docx) | Markdown (.md) |
|----------|--------------|----------------|
| Bản chất | Rich Text, nhị phân | Plain Text, văn bản thô |
| Xem trên trình duyệt GitHub | Không | Có, tự render |
| Git Diff | Không dùng được | Chỉ ra đúng dòng sửa |
| Mất 1 byte | Hỏng cả file | Chỉ sai 1 ký tự, phần còn lại vẫn đọc được |
| Dung lượng | Nặng | Rất nhẹ |

## Phần 2. Hoàn thiện: file `gioi-thieu-greentech.md`

Cách làm trong StackEdit: mở StackEdit, dán nội dung từ Word vào, sửa thành cú pháp Markdown, rồi chọn Export to disk, As Markdown để lưu file .md.

````markdown
# GreenTech

## Giới thiệu dự án

**GreenTech** là dự án nhóm của sinh viên PTIT, ứng dụng công nghệ vào trang trại thông minh.

## Mục tiêu

- Theo dõi độ ẩm đất bằng cảm biến
- Tự động tưới cây
- Giúp nông dân tiết kiệm công sức

> Công nghệ xanh cho nông nghiệp bền vững.
````
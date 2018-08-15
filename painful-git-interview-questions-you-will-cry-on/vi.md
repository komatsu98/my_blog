# 11 Painful Git Interview Questions You Will Cry On

Theo những tóm tắt mới nhất của developer Stack Overflow, hơn 70% các developer sử dụng git, trở thành một trong những VCS được dùng nhiều nhất trên thế giới. Git được sử dụng phổ biến ở cả phát triển pen source và phần mềm thương mại, với nhiều lợi ích cho các cá nhân, nhóm và doanh nghiệp.

## Câu hỏi 1: Git fork là gì ? Sự khác nhau giữa fork, branch và clone là gì ?

* Một fork là một remote, một repository copy của phía server, khác từ gốc. Một fork không là một khái niệm Git thực sự, đó là một ý tưởng chính trị/xã hội. 
* Một clone không là một fork, một clone là một bản copy dưới local của một vài repository trên remote. Khi bạn cloen, bạn thực ra đang copy toàn bộ mã nguồn của repository, bao gồm tất cả lịch sử và các nhánh.
* Một nhánh (branch) là một cơ chế để xử lý các thay đổi với một repository riêng để sau đó merge chúng với các code còn lại. Một nhánh hiểu là một vài thứ nằm trong một repository. Về mặt khái niệm, nó đại diện cho một luồng phát triển.

## Câu hỏi 2: Sự khác nhau giữa một "pull request" và một "nhánh" là gì ?

Một **nhánh** chỉ là một phiên bản riêng của code
Một **pull request** là khi ai đó lấy về một repository, tạo chúng trên nhánh của họ, thực hiện mộ số thay đổi, sau đó cố gắng hợp nhất nhand đó vào (đẩy những thay đổi của họ vào repository code của người khác)

## Câu hỏi 3: Sự khác nhau giữa 'git pull' và 'git fetch' là gì ?

Theo thuật ngữ đơn giản nhất, `git pull` làm một `git fetch` được theo dõi bởi một `git merge`
* Khi bạn sử dụng `pull` , Git cố gắng để tự động làm các việc cho bạn. Đó là ngữ cảnh nhạy cảm, nên Git sẽ merge bất kỳ các commit nào được pull vào nhánh bạn đang làm việc hiện tại. `pull` tự động merge các commit mà không để bạn xem qua chúng trước khi merge. Nếu bạn không quản lý chặt các nhánh của bạn, bạn có thể thường xuyên gặp những xung đột (conflict).
* Khi bạn `fetch`, Git thu thập bất kỳ commit nào **từ nhánh mục tiêu không tồn tại trong nhánh hiện tại của bạn** và lưu chúng trong repository local của bạn. Điều này đặc biệt hữu ích nếu bạn cần cập nhật repository của mình, nhưng những thứ đang làm việc có thể bị hỏng nếu bạn cập nhật các file của mình. Để tích hợp các commit vào nhánh master, bạn sử dụng `merge`

## Câu hỏi 4: Làm thế nào để revert lại commit trước trong Git ?

Giả sử bạn có cái này, C là nơi con trỏ HEAD của bạn và F là trạng thái của các file của bạn.

```
   (F)
A-B-C
    ↑
  master
``` 


* Để nuke thay đổi trong commit 

```
git reset --hard HEAD~1
```


Bây B là HEAD. Bởi vì bạn đã sử dụng --hard, các file của bạn được reset để trạng thái về tại commit B
* Để huỷ bỏ commit nhưng vẫn giữ thay đổi của mình: 

```
git reset HEAD~1
```

Bây giờ chúng ta nói cho Git để di chuyển con trỏ HEAD quay trở lại một commit B và để các file như chính chúng và `git status` hiển thị các thay đổi đã được kiểm tra trong C

Khi bạn thực hiện `git status`, bạn sẽ thấy các file tương tự như là đã index trước đó.

## Câu hỏi 5: "git cherry-pick" là gì ?

Câu lệnh git `cherry-pick` thường được sử dụng để đưa ra các commit cụ thể từ một nhánh trong một repository trên một nhánh khác




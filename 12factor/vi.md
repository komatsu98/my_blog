##Giới thiệu
Trong thời đại hiện đại, phần mềm thông thường được phân phối như một dịch vụ, được gọi _web apps_ or _software-as-a-service_. 12 chuẩn ứng dụng là một phương pháp cho xây dựng các ứng dụng phần mềm như một dịch vụ:

* Sử dụng các định dạng khai báo cho cài đặt tự động, để tối thiểu hoá thời gian và chi phí cho các developer mới tham gia dự án.
* Có một **contract rõ ràng** với hệ điều hành cơ bản, cung cấp khả năng di động tối đã giữa các môi trường thực thi.
* Thích hợp cho việc triển khai trên **nền tảng đám mây** hiện đại, giảm bớt sự cần thiết cho các máy chủ và quản trị viên hệ thống.
* **Giảm thiểu sự khác nhau** giữa quá trình phát triển và sản phẩm, cho phép tiếp tục triển khai một các nhanh chóng nhất.
* Và có thể mở rộng quy mô mà không thay đổi nhiều các công cụ, kiến trúc hoặc các phát triển.

12 phương pháp này có thể áp dụng vào ứng dụng được viết trên mọi ngôn ngữ lập trình, và nó được sử dụng bất kỳ với sự kết hợp nào của các dịch vụ sao lưu (cơ sở dữ liệu, hàng đợi, bộ nhớ cache, ...)


## Background

Những người đóng góp cho tài liệu này đã được trực tiếp tham gia vào việc phát triển và triển khai hàng trăm ứng dụng, và gián tiếp thấy sự phát triển, vận hành và mở rộng của hàng trăm nghìn ứng dụng thông qua công việc của chúng tôi trên nền tảng Heroku

Tài liệu này tổng hợp tất cả các kinh nghiệm và sự theo dõi của chúng tôi về nhiều ứng dụng phần mềm giống như dịch vụ trong thực tế. Nó là 2 khía cạnh chính về ý tưởng thực hiện cho phát triển ứng dụng, đặc biệt tập trung vào sự linh hoạt của sự phát triển hữu cơ của ứng dụng theo thời gian, sự linh hoạt của sự cộng tác giữa các developer làm việc trên codebase của ứng dụng và tránh lãng phí chi phí phần mềm.

Mục đích của chúng tôi là nâng cao nhận thức về một số vấn đề hệ thống mà chúng tôi đã thấy trong quá trình phát triển các ứng dụng hiện đại, để cung cấp từ vựng chung cho việc thảo luận những vấn đề này, và cung cấp một tập hợp các khái niệm giải pháp cho những vấn đề với các thuật ngữ kèm theo. Định dạng này là được lấy từ cuốn sác của Marlin Fowler [Patterns of Enterprise Application Architecture and Refactoring](https://books.google.com/books/about/Patterns_of_enterprise_application_archi.html?id=FyWZt5DdvFkC)

## Ai nên đọc tài liệu này ?

Mọi developer xây dựng các ứng dụng mà chạy như một dịch vụ. Các kỹ sư người triển khai hoặc quản lý các ứng dụng như vậy

## 12 phương pháp luận
### I. Codebase
Một codebase được theo dõi trong mọi mọi sửa đổi, và các lần triển khai
### II. Dependencies
Khai báo rõng ràng và độc lập giữa các phụ thuộc
### III. Config
Lưu trữ cấu hình trong môi trường
### IV. Backing services
Treat backing services as attached resources
### V. Build, release, run
Các giai đoạn xây dựng và chạy hoàn toàn riêng biệt
### VI. Processes
Thực thi ứng dụng dưới một hoặc nhiều tiến trình
### VII. Port binding
Export services via port binding
### VIII. Concurrency
Mở rộng quy mô thông qua mô hình process
### IX. Disposability
Maximize robustness with fast startup and graceful shutdown
Tối đa hoá sức mạnh với việc khởi động nhanh và tắt dễ dàng.
### X. Dev/prod parity
Giữ các bản phát triển, staging và sản phẩn càng giống nhau càng tốt
### XI. Logs
Coi các log như luồng sự kiện
### XII. Admin processes
Run admin/management tasks as one-off processes
Chạy tác vụ admin/quản lý giống như các tiến trình một lần
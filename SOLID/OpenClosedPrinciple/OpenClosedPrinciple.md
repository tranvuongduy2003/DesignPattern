# Open/Closed Principle

***"Các class nên open để mở rộng nhưng closed để sửa đổi."***

Ý chính của nguyên tắc này là giữ cho code hiện có không bị *breaking* khi bạn thêm các tính năng mới.

Một class được coi là *open* nếu bạn có thể mở rộng nó, tạo ra một class con và thực hiện bất cứ điều gì bạn muốn, thêm các method hoặc field mới, ghi đè hành vi cơ bản, v.v. Một số ngôn ngữ lập trình cho phép bạn giới hạn việc mở rộng thêm một class bằng các từ khóa đặc biệt như `final`. Sau đó, class sẽ không còn *open* nữa. Đồng thời, class được coi là *closed* nếu nó đã sẵn sàng 100% để được sử dụng bởi các class khác, interface của nó *được định nghĩa rõ ràng và sẽ không thay đổi trong tương lai*.

Khi lần đầu tôi học về nguyên tắc này, tôi đã thấy bối rối vì hai từ *"open"* và *"closed"* nghe có vẻ mâu thuẫn nhau. Nhưng theo nguyên tắc này, một class có thể vừa *open* (cho phép mở rộng) và vừa *closed* (không cho phép sửa đổi) cùng lúc.

Nếu một class đã được phát triển, kiểm thử, đánh giá và được sử dụng trong một framework hoặc ứng dụng nào đó, việc thay đổi code của nó có thể rất rủi ro. Thay vì sửa đổi trực tiếp code của class, bạn có thể tạo một class con và *override* các phần của class gốc mà bạn muốn thay đổi hành vi. Bằng cách này, bạn đạt được mục tiêu của mình mà không làm *breaking* bất kỳ thành phần nào đang sử dụng class gốc.

Nguyên tắc này không nhằm áp dụng cho mọi thay đổi của một class. Nếu bạn biết có lỗi trong class, chỉ cần sửa nó; không cần tạo class con chỉ để khắc phục lỗi. Một class con không nên chịu trách nhiệm cho các vấn đề của class cha.
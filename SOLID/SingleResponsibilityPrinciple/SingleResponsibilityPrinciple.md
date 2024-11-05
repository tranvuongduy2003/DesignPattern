# Single Responsibility Principle

***"Một class chỉ nên có một lý do để thay đổi"***

Hãy cố gắng thiết kế mỗi class chỉ chịu trách nhiệm cho một chức năng cụ thể của phần mềm và đảm bảo rằng chức năng đó được hoàn toàn đóng gói (hay ẩn bên trong) trong class.

Mục tiêu chính của nguyên tắc này là *giảm độ phức tạp*. Bạn không cần phải thiết kế quá phức tạp cho một chương trình chỉ có khoảng 200 dòng code. Chỉ cần làm cho vài method *trở nên dễ hiểu và rõ ràng* là đủ.

Khi chương trình của bạn ngày càng lớn và phức tạp, các class có thể trở nên quá đồ sộ khiến bạn không thể nhớ hết chi tiết của chúng. Điều này làm cho việc tìm kiếm chậm lại; đôi khi bạn phải duyệt qua toàn bộ các class, thậm chí là cả chương trình, để tìm một đoạn code cụ thể. Số lượng thành phần trong chương trình quá nhiều khiến bạn khó ghi nhớ và cảm thấy mất kiểm soát mã nguồn.

Còn nữa: nếu một class làm quá nhiều việc, bạn sẽ phải thay đổi từng method hoặc property mỗi khi có một trong những method hoặc property đó thay đổi. Khi làm như vậy, bạn có nguy cơ làm hỏng các phần khác của class mà bạn thậm chí không định thay đổi.

Nếu bạn cảm thấy khó tập trung vào từng phần cụ thể của chương trình, hãy nhớ đến *Single Responsibility Principle* và cân nhắc xem có nên chia nhỏ một số class thành các phần nhỏ hơn không.
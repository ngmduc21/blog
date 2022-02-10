---
title: "Hiểu về Blockchain - Chương 1: Cơ bản về Blockchain"
date: 2022-02-10
categories: Blockchain
---
Blockchain là một “sổ cái” bất biến và có thể chia sẻ giúp cho quá trình ghi lại các giao dịch và theo dõi tài sản trong một mạng lưới doanh nghiệp. “Tài sản” có thể là vật hữu hình (nhà, xe, đất đai, tiền mặt) hoặc vô hình (sở hữu trí tuệ, bằng sáng chế, bản quyền, thương hiệu...). Nói nôm na, tất cả những thứ mang giá trị đều có thể được theo dõi và giao dịch trên một mạng Blockchain, giảm thiểu rủi ro và chi phí cho các bên liên quan.
<!-- excerpt-end -->
## Những thiếu sót của hệ thống giao dịch ngày nay

Trong lịch sử, các phương tiện của niềm tin chẳng hạn như tiền xu, tiền giấy, phiếu séc và hệ thông ngân hàng đã thực hiện việc trao đổi giá trị và bảo vệ người bán và người mua. Các phát minh ngày nay (chẳng hạn điện thoại, hệ thống thẻ tín dụng, Internet và điện thoại di động) đã cải thiện sự tiện lợi, nhanh chóng, hiệu quả và thu hẹp khoảng cách giữa người bán và người mua.

Mặc dù vậy, các giao dịch hiện nay vẫn còn bộc lộ nhiều khuyết điểm như sau:

- Tiền mặt chỉ hữu dụng với những giao dịch nội địa và thường là với giá trị nhỏ.
- Thời gian để giao dịch thành công đến việc chấp thuận trao đổi thường khá lâu.
- Sự tham gia của các bên thứ 3, bên trung gian làm giảm tính hiệu quả trong giao dịch.
- Lừa đảo, tấn công mạng và những lỗi nhỏ có thể làm tăng thêm chi phí và sự phức tạp trong hoạt động kinh doanh. Tất cả những bên liên quan trong mạng lưới doanh nghiệp có thể đối mặt với rủi ro nếu hệ thống trung tâm bị xâm phạm - chẳng hạn như ngân hàng.
- Để tham gia vào các tổ chức tín dụng, người bán lẫn người mua đều phải trả một chi phí cao, liên qua đến các thủ tục giấy tờ phúc tạp và thời gian xét duyệt hồ sơ rất tốn thời gian.
- Một nửa số người trên thế giới không có quyền mở tài khoản ngân hàng, việc đòi hỏi một hệ thống thanh toán song song có thể thực hiện các giao dịch là điều cần thiết.
- Việc hạn chế về tính minh bạch và thông tin không nhất quán làm cản trở sự luân chuyển hiệu quả của hàng hoá.

Khối lượng các giao dịch trên toàn thế giới đang tăng theo cấp số nhân và chắc chắn sẽ làm tăng mức độ phức tạp, lỗ hổng, rủi ro và chi phí của các hệ thống giao dịch hiện tại. Sự phát triển của thương mại điện tử, ngân hàng trực tuyến, các ứng dụng mua hàng cùng với bối cảnh xã hội ngày nay đã thúc đẩy sự tăng trưởng của khối lượng giao dịch. Khối lượng giao dịch sẽ còn bùng nổ với sự phát triển của IoT - các đồ vật tự hành. Để giải quyết những thách thức này, thế giới cần một hệ thống thanh toán nhanh hơn với các cơ chế để thiết lập uy tín, không yêu cầu thiết bị chuyên dụng, không có các khoản phí hàng tháng và cung cấp một giải pháp sổ sách minh bạch và đáng tin cậy.

## Cách mạng hoá mạng lưới kinh doanh truyền thống

Đối với việc ghi lại các giao dịch và theo dõi tài sản theo cách truyền thống, những người trong cùng một mạng sẽ giữ “sổ cái” riêng của họ và các sổ cái khác. Với cách làm truyền thống này sẽ tốn khá nhiều chi phí bởi vì nó liên quan đến các bên trung gian - sẽ mất phí cho các dịch vụ của họ. Ngoài ra nếu hệ thống trung tâm (ví dụ ngân hàng) bị xâm nhập hoặc tấn công mạng, nó sẽ gây ra hậu quả và thiệt hại rất khó lường. 

Hiện nay các mạng lưới doanh nghiệp đang chuyển dần sang sử dụng blockchain. Kiến trúc blockchain cung cấp cho người sử dụng khả năng chia sẻ sổ cái, nơi mà thông tin sẽ được cập nhật thông qua peer-to-peer - có nghĩa là mỗi người tham gia vào blockchain (còn gọi là node) đóng vai trò như một “publisher” và một “subscriber”.

Mỗi node có thể nhận cà gửi các giao dịch đến những node khác, và dữ liệu sẽ được đồng bộ trên toàn mạng khi nó được truyền đi.

Một mạng blockchain sẽ có những đặc điểm sau:

- Tính đồng thuận: Để một giao dịch có hiệu lực, tất cả những người tham gia phải đồng ý về tính hợp lệ của nó.
- Tính truy vết nguồn gốc: Người tham gia sẽ biết tài sản đó đến từ đâu và quyền sở hữu của nó đã thay đổi như thế nào theo thời gian.
- Tính bất biến: Không người tham gia nào có thể giả mạo một giao dịch sau khi nó đã được ghi vào sổ cái. Nếu một giao dịch bị lỗi, một giao dịch mới phải được sử dụng để sửa lỗi và cả 2 giao dịch đều được ghi nhận.
- Tính hợp nhất: Một sổ cái duy nhất sẽ cung cấp một nơi duy nhất để xác định quyền sở hữu tài sản hoặc việc hoàn thành giao dịch.

## Khám phá một ứng dụng blockchain

Các công ty cho thuê ô tô luôn muốn việc thuê một chiếc xe trở nên thật dễ dàng, nhưng trong thực tế việc đó khá phức tạp. Một thách thức với mạng lưới cho thuê oto ngày nay phải đối mặt là mặc dùng chuỗi cung ứng về vật lý cơ bản là khả thi, nhưng các hệ thống hỗ trợ thì đang bị phân mảnh. Mỗi đơn vị cung ứng xe ô tô đều đang sử dụng một sổ cái của riêng mình, có thể mất khá nhiều thời gian để công ty cho thuê có thể đồng bộ hoá dữ liệu từ các đơn vị khác nhau.

![before_blockchain](/blog/assets/post04/before_blockchain.png)

Nếu sử dụng một sổ cái chính trên một mạng blockchain, tất cả những tham gia đã được uỷ quyền đều có thể truy cập, giám sát và phân tích tình trạng của chiếc xe bất kể nó đang ở đâu trong vòng đời của nó.

![after_blockchain](/blog/assets/post04/after_blockchain.png)

Với blockchain, người sử dụng sẽ có thể:

1. Cơ quan quản lý tạo vào điền thông tin đăng ký cho phương tiện mới trên blockchain và chuyển quyền sở hữu phương tiện cho nhà sản xuất.
2. Nhà sản xuất thêm kiểu dáng, mẫu mã và ID của xe vào biểu mẫu với các tham số được chấp thuận bởi hệ thống Smart Contract.
3. Các đại lý có thể xem tình trạng tồn hàng. Quyền sở hữu xe có thể được chuyển từ nhà sản xuất sang đại lý sau khi Smart Contract được thực hiện để xác thực giao dịch mua bán.
4. Công ty cho thuê xe có thể xem hàng tồn kho của đại lý. Quyền sở hữu xe có thể chuyển từ đại lý sang công ty cho thuê xe sau khi Smart Contract được thực hiện.
5. Công ty cho thuê có thể xem những chiếc xe nào có thể cho thuê và hoàn thành các hình thức cần thiết để bắt đầu cho thuê.
6. Quá trình cho thuê tiếp tục diễn ra với nhiều người thuê cho đến khi công ty cho thuê quyết định cho chiếc xe “nghỉ hưu”. Tại thời điểm này, quyền sở hữu của chiếc xe sẽ được chuyển cho người xử lý phế liệu sau khi Smart Contract được thực hiện và họ có quyền định đoạt chiếc xe đó.

## Rút ra những lợi ích kinh doanh từ việc sử dụng Blockchain

Đối với doanh nghiệp, blockchain mang lại những lợi ích như:

- Tiết kiệm thời gian: những giao dịch phức tạp trước đây phải được thực hiện bởi nhiều bên trong nhiều ngày, nay được rút ngắn chỉ còn vài phút. Việc giải quyết giao dịch nhanh hơn vì không yêu cầu xác minh từ cơ quan thứ 3.
- Tiết kiệm chi phí
- Bảo mật tốt hơn
- Quyền riêng tư chặt chẽ hơn
- Cải thiện khả năng kiểm toán
- Tăng hiệu quả hoạt động

## Xây dựng lòng tin với Blockchain

Blockchain nâng cao sự tin tưởng trên mạng kinh doanh. Nó đặc biệt có giá trị trong việc tăng mới độ tin cậy giữa những người tha gia mạng lưới vì nó luôn cung cấp bằng chứng trên mỗi giao dịch; và vì mỗi giao dịch không thể bị giả mạo và được ký bởi những đối tác có liên quan nên có thể giảm thiểu những hành vi tham nhũng. Việc tự kiểm soát này có thể giảm bớt sự phụ thuộc vào các biện pháp bảo vệ và chế tài của pháp luật trong kinh doanh. 

Blockchain xây dựng lòng tin trên thông qua những đặc điểm sau:

- Tính phân tán và bền vững: sổ cái được chia sẻ, cập nhật với mọi giao dịch và được sao chép có chọn lọc giữa những người tham gia trong thời gian gần thực. Bởi vì nó không được sở hữu hoặc kiểm soát bởi bất kỳ tổ chức duy nhất nào, sự tồn tại liên tục của nền tảng Blockchain
- Tính bảo mật, riêng tư và không thể xoá được: tính bảo mật được duy trình thông qua các kỹ thuật cryptography và/hoặc kỹ thuật phân vùng dữ liệu để cung cấp cho người tham gia khả năng hiển thị có chọn lọc vào sổ cái; cả giao dịch và danh tính của các bên giao dịch có thể được che giấu. Sau khi các điều kiện được đồng thuận, người tham gia không thể giải mạo hồ sơ giao dịch.
- Tính minh bạch: vì những người tham gia giao dịch có quyền truy cập vào các bản ghi giống nhau, họ có thể xác thực giao dịch và xác minh danh tính hoặc quyền sở hữu mà không cần bên trung gian thứ 3. Các giao dịch đều được ghi lại thời gian, theo thứ tự và có thể xác minh trong thời gian gần thực.
- Tính đồng thuận trong giao dịch: Tất cả những người tham gia mạng đều đồng thuận rằng giao dịch là hợp lệ. Điều này đạt được thông qua việc sử dụng các thuật toán đồng thuận. Mỗi mạng blockchain có thể thiết lập các điều kiện mà theo đó một giao dịch hoặc trao đổi tài sản có thể thực thi.
- Tính sắp xếp và linh hoạt: các ràng buộc kinh doanh và Smart Contract có thể được tích hợp vào nền tảng, các mạng Blockchain có thể phát triển hơn và khi hoàn chỉnh, chúng có thể hỗ trợ các quy trình kinh doanh đầu cuối và rất nhiều hoạt động khác.
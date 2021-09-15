---
title: "Cookie Introduction"
date: 2021-09-07
categories: Network
---
Tìm hiểu cơ bản, phân loại theo phương pháp mô hình hóa và hiểu được vai trò của Cookie - một thành phần vô cùng quan trọng trong thế giới Internet.
<!-- excerpt-end -->
# Bắt đầu với Cookies

![](https://lh3.googleusercontent.com/-VSjWMWxIdXk/X4mbK2WD9RI/AAAAAAAAAwQ/SDhUh5Oas2455ozQ7DpnDIf5dDtQxI0bQCLcBGAsYHQ/w462-h169/Screen%2BShot%2B2020-10-16%2Bat%2B20.05.51.png)
 
Bạn đã từng thấy những thông báo như này khi truy cập vào những website thương mại điện tử?  
Đúng rồi đó, khi truy cập vào đó, chúng sẽ lưu lại một dãy thông tin gồm những chữ và số, nhằm biết bạn là ai để lần sau bạn vào, chiếc áo phông bạn đang chọn vẫn đang nằm trong giỏ hàng. Và sự vi diệu đó nhờ 1 thứ khá nhỏ bé - Bánh Quy (Cookie).

# Cookies là gì? Có mấy loại cookies và chúng khác nhau thế nào?
Về cơ bản có hai loại bánh... à nhầm, 2 loại cookie: First-Party Cookie (Cookie bên thứ nhất) và Third-Party Cookie (Cookie bên thứ ba). Từ giờ về sau mình sẽ gọi tóm tắt là Cookie T1 và Cookie T3 để đọc cho đỡ mệt nha. Từ góc độ kỹ thuật, không có sự khác biệt thực sự giữa hai loại cookie. Cả hai đều chứa các phần thông tin giống nhau và có thể thực hiện các chức năng giống nhau.

Tuy nhiên, sự khác biệt thực sự giữa các loại cookie liên quan đến cách chúng được tạo ra và sau đó được sử dụng, điều này thường phụ thuộc vào ngữ cảnh cũng như điều kiện sử dụng trang web đó. Có những lợi ích khác nhau của việc tạo cookie của bên thứ nhất so với bên thứ ba.

-   Cookie T1 được lưu trữ bởi domain (trang web) mà bạn đang truy cập trực tiếp. Chúng cho phép chủ sở hữu trang web thu thập dữ liệu phân tích, ghi nhớ cài đặt ngôn ngữ và thực hiện các chức năng hữu ích khác giúp cung cấp trải nghiệm người dùng tốt nhất. Đó cũng là lý do vì sao một khi bạn set ngôn ngữ trang web là Tiếng Việt thì lần sau nó không dám hiện Eng-Lích nữa!

-   Cookie T3 được tạo bởi những domains khác với domain mà bạn đang truy cập trực tiếp, do đó nên nó có tên là bên thứ ba. Chúng được sử dụng để theo dõi trên nhiều trang web, nhắm mục tiêu lại và phân phát quảng cáo.

Vậy bạn có thắc mắc sao không có cả Cookie T2 (second-party Cookie) không? Cookies T2 là cookie được chuyển từ một công ty (công ty đã tạo ra cookie của bên thứ nhất) sang một công ty khác thông qua một số hình thức đối tác dữ liệu. Ví dụ: một hãng vận chuyển hành khách có thể bán cookie T1 (và dữ liệu bên thứ nhất khác như tên, địa chỉ email, v.v.) cho một chuỗi khách sạn để sử dụng cho việc target advertising (quảng cáo mục tiêu). Vậy là khi bạn đi du lịch Đà Lạt, tự nhiên điện thoại bạn xuất hiện toàn những khách sạn, homestay hay dịch vụ vui chơi ở Đà Lạt là nhờ Cookies T2 đó.

Về mặt kỹ thuật, cookie T1 và cookie T3 giống nhau về mặt dữ liệu. Điều khác biệt là cách các trang web tạo và sử dụng chúng. Bảng sau sẽ so sánh một cách trực quan hơn giữa 2 thằng này:

![](https://lh3.googleusercontent.com/-hFqc6d1jXHk/X7nsJCqCEJI/AAAAAAAAAxU/ucIVUuDqrdg3b5BhaakfOhC0mcJuZOSMwCLcBGAsYHQ/w639-h331/Screen%2BShot%2B2020-11-22%2Bat%2B11.42.03.png)
  

Ngoài cookie T1 được tạo bởi trang web đang truy cập (mottrangwebnaodo.com), cookie T3 cũng được tạo bởi ad.doubleclick.net. Đó là lý do vì sao URL cookie T3 (ad.doubleclick.net) thường không khớp với tên miền trang web bạn đang truy cập (mottrangwebnaodo.com). Cookie do nhà cung cấp quảng cáo bên thứ ba để lại, do đó nó có tên là cookie của bên thứ ba.

  

Cookie T3 là thứ làm "điên đảo" thế giới ngày nay, cùng tìm hiểu sâu hơn về thằng này nhé!

# Vậy Cookie T3 được tạo ra như thế nào?

Bây giờ bạn có đang thắc mắc làm cách nào mà ad.doubleclick.net hoặc bất kỳ bên thứ ba nào khác có thể tạo cookie nếu người dùng đang ở trên một trang web khác nhau tại một thời điểm nhất định?

  

Để cookie T3 được tạo ra, một request (yêu cầu) cần được gửi từ trang web đến máy chủ của bên thứ ba. File được yêu cầu khác nhau tùy thuộc vào mục đích sử dụng, nhưng nó có thể là một quảng cáo hoặc một tracking pixel (một dạng "gián điệp" theo dõi hành vi của bạn trên website đó), hoàn toàn vô hình đối với chúng ta.

  

Ví dụ: nếu bên thứ ba là một dịch vụ quảng cáo của DoubleClick (một dịch vụ quảng cáo của Google), thì cookies request sẽ phục vụ việc quảng cáo - quảng cáo mà chúng ta thường nhìn thấy. DoubleClick Markup là thực thể có thể cho phép cookie của bên thứ ba có thể lưu trữ và hoạt động. Đây là một ví dụ của một markup được nhúng vào trong trang web:

  
```html
_<a href="ad.doubleclick.net/muc_dich_quang_cao" target="_blank" rel="noopener"> <img src = "ad.doubleclick.net/noi_dung_quang_cao "> </a>_
```
  

Khi trang web load lên, markup ở trên sẽ load và một request sẽ được gửi đến  _ad.doubleclick.net/noi_dung_quang_cao_  để truy xuất hình ảnh và gán cookie cho người dùng trong cùng một thời gian. Các bên thứ ba khác nhau có thể yêu cầu các loại file khác nhau từ web server của họ và gửi chúng trở lại trình duyệt.

# Ví dụ một vài cookie T3 mà chúng ta thường thấy

## Các nút "chia sẻ qua:..."

![](https://lh3.googleusercontent.com/-ZAnzMn9xOYk/X7nwDc9Kc9I/AAAAAAAAAxw/E56SSo72MIkXPPz3d3zhZqdL9zHPNyHuACLcBGAsYHQ/Screen%2BShot%2B2020-11-22%2Bat%2B11.58.47.png)
  
Hầu hết các plugin mạng xã hội cho phép người dùng login, share và like nội dung trên các trang web của bên thứ ba - nơi cookie được đặt trên nó.

Bằng cách này, các trang web MXH có thể theo dõi các trang web bạn truy cập và gửi cho bạn các quảng cáo có liên quan khi bạn quay lại các trang web MXH này. Ngay cả khi bạn chưa đăng nhập vào tài khoản của mình, các cookie này vẫn sẽ theo dõi bạn bằng cách xác định cookie của bạn và so sánh các cặp cookies với nhau và thậm chí đôi khi xác định thiết bị bạn đang truy cập để nhận dạng bạn.

## Chat trong trang web

![](https://lh3.googleusercontent.com/-3YO2X6PaFgk/X7nxFwH--7I/AAAAAAAAAx8/gXF1oHwXhA81CaGQk1eKt4iCJLU9uL4-QCLcBGAsYHQ/Screen%2BShot%2B2020-11-22%2Bat%2B12.03.12.png)

  
Cửa sổ pop-up chat hoạt động theo cách tương tự như các nút chia sẻ qua MXH. Pop-up chat plugin sẽ để lại cookie trong trình duyệt của bạn để nâng cao trải nghiệm người dùng.

Ví dụ: vì pop-up chat có thể nhận dạng bạn, nên lần sau khi bạn bật pop-up chat lên, nó sẽ ghi nhớ tên của bạn và tất cả lịch sử trò chuyện. Tất nhiên, dữ liệu này sẽ bị xóa khi bạn xóa cookie của mình hoặc khi chúng hết hạn.

  

Ok, hít thở sâu nhé, mình đi sâu một chút nữa...

# Trình duyệt của chúng ta xử lý cookie T1 và cookie T3 như thế nào?

## Cookie T1

Cookie T1, như mình đã nói rất nhiều ở trên, được tạo trực tiếp bởi trang web bất cứ khi nào người dùng truy cập trang web. Nói chung, hầu hết các trình duyệt chấp nhận cookie của bên thứ nhất theo mặc định, vì vai trò chính của chúng là cho phép tùy chỉnh và cải thiện trải nghiệm người dùng.

  

Ví dụ, khi bạn truy cập vào các trang web bán hàng đơn thuần, cookie T1 sẽ giúp ta lưu lại những vật phẩm đã đưa vào giỏ hàng để lần truy cập sau không phải mắc công chọn lại nữa và nó được lưu trong chính thiết bị của bạn. Trang web sẽ quyết định thu thập và lưu trữ thông tin nào.

  

Hạn chế lớn của cookie của bên thứ nhất là chúng chỉ có thể được đọc khi người dùng đang truy cập trang web đó. Điều này khiến chúng trở nên vô dụng cho các mục đích quảng cáo trên các trang web khác.

  

## Cookie T3

Cookie T3 (còn được gọi là tracking cookies hoặc trackers) được tạo bởi “các bên” ngoài trang web mà người dùng hiện đang truy cập, giúp các nhà cung cấp dịch vụ quảng cáo phân tích và theo dõi chúng ta.

Thử ví dụ nhé:

  

Khi bạn truy cập muong14.com và đọc báo, muong14.com sẽ tạo một cookie T1 và lưu nó vào máy tính của bạn. Bởi vì muong14.com (giống như hầu hết các báo mạng) sử dụng quảng cáo trực tuyến như một cách để kiếm tiền từ nội dung của họ, các quảng cáo bạn thấy trên muong14.com cũng sẽ tạo một cookie (ví dụ: tên miền ads.google.com) và lưu nó vào máy tính của bạn .

  

Vì những cookie này không được tạo bởi muong14.com, chúng được phân loại là cookie T3.

  

Một trang web có thể sử dụng một số trackers (hoặc cookie T3) của bên thứ ba khác nhau để thu thập thông tin người dùng. Thông tin này có thể bao gồm dữ liệu như hành vi của người dùng trên trang web, vị trí và loại thiết bị - được truyền từ trang web. Nó cũng có thể theo dõi nội dung người dùng xem trên trang web đó và những thứ họ nhấp vào (ví dụ: sản phẩm và quảng cáo). Nhà quảng cáo sử dụng chúng để hiển thị quảng cáo cho người dùng khi họ truy cập các trang web khác nhau.

  

Ví dụ: nếu người dùng truy cập shopee.com và nhấp vào một cái áo khoác, các trackers của bên thứ ba sẽ thu thập và phân tích thông tin về người dùng đó và hoạt động của họ trên shopee.com. Sau đó, nếu người dùng đó rời khỏi shopee.com và truy cập vào một trang web khác, chẳng hạn như muong14.com, thì người dùng đó có thể được hiển thị quảng cáo cho chính sản phẩm đó hoặc sản phẩm tương tự (chẳng hạn một cái áo khoác nhưng có thêm cái mũ ?!)

  

Cách thức hoạt động là cả shopee.com và muong14.com đều tải một đoạn mã từ máy chủ quảng cáo (ví dụ: ad.doubleclick.net). Khi người dùng điều hướng đến một trong hai trang web, đoạn mã được tải từ ad.doubleclick.net là từ một miền khác với URL trong trình duyệt của người dùng, vì vậy cookie được đặt trong ad.doubleclick.net được coi là cookie T3.

  

Cookie có thể được thiết lập và đọc bởi web server hoặc bởi một đoạn JavaScript chạy trên trang web. Phần mềm như Ghostery hoặc AdBlock Plus có thể chặn các tập lệnh này.

  

Ok phức tạp thêm một xíu nhé...

  

# Cookie T1 nhưng được sử dụng trong tình huống và mục đích của Cookie T3

Một số cookie T1 có thể được sử dụng để theo dõi người dùng theo cách tương tự như cookie T3 trong các tình huống cụ thể.

  

Ví dụ, các login box (widget, plugin) vào các trang xã hội như Facebook có thể được đặt trên các trang web khác nhau để giúp chúng ta comment hoặc “like” nội dung ngay trên đó. Chức năng này sử dụng cookie của bên thứ nhất trong ngữ cảnh của bên thứ ba; bởi vì người dùng tương tác với login plugin của MXH (như khi truy cập vào domain của MXH đó), plugin MXH có thể để lại cookie của bên thứ nhất. Sau đó, cookie T1 cứ như vậy được sử dụng trong ngữ cảnh của cookie T3 và có thể tracking trên nhiều trang web khác. Tuy nhiên, một số trình duyệt internet như Safari có các phương pháp chặn điều này (từ Safari 11 trở đi).

  

# Ngăn chặn Theo dõi Thông minh (Intelligent Tracking Prevention - ITP) của Apple

Apple là công ty vô cùng quan tâm đến sự bảo mật của người dùng. Ngăn chặn theo dõi thông minh (ITP) là một tính năng được Apple đưa vào làm mặc định trong Safari và trong iOS 11 trở đi. Nó thay đổi cách trình duyệt Apple xử lý cookie T1, khác với hầu hết các trình duyệt khác.

  

Phiên bản mới nhất của nó, ITP 2.0, phát hiện theo dõi trên nhiều trang web và phân vùng (hoặc cô lập) cookie T1, khiến trang web không thể sử dụng cookie T1 trong ngữ cảnh của cookie T3 cho mục đích theo dõi hoặc phân tích. Một số chuyên gia nói rằng bằng cách đưa ra các quy tắc nghiêm ngặt như vậy để đối phó với cookie T3, Apple đã phá hoại mô hình kinh tế hiện tại của Internet.

  

Các phiên bản trước của ITP của Apple (1.0 và 1.1) cho phép đọc và sử dụng cookie trong “ngữ cảnh của bên thứ ba”, miễn là người dùng truy cập trực tiếp vào trang web đó trong 24 giờ đầu tiên. Điều đó đã mang lại một lợi thế không công bằng cho Facebook và Google, vì việc thanh lọc trong 24 giờ không có tác dụng đối với họ như trên các trang web khác vì người dùng truy cập các trang web này thường xuyên và hiếm khi đăng xuất. Với ITP 2.0, điều này không còn khả thi nữa.

  

Mozilla đã làm theo điều đó và Firefox Phiên bản 50 trở hiện cung cấp chức năng “thông minh” giống Safari để chặn các cookie theo dõi không mong muốn của bên thứ ba. Biểu tượng lá chắn màu xám xuất hiện trên thanh địa chỉ khi Firefox chặn các trackers.

![](https://lh3.googleusercontent.com/-CABrMDKIkLY/X7n6u-I3znI/AAAAAAAAAyY/DwHCtMA2cJUYchYeY-VEufePvibC5M1nQCLcBGAsYHQ/Screen%2BShot%2B2020-11-22%2Bat%2B12.44.21.png)

  

# Làm sao để tắt Cookie T3?

Cookie của bên thứ ba bị chặn khi người dùng thực hiện một hoặc nhiều thao tác sau:

  

-   Duyệt web ở chế độ riêng tư hoặc ẩn danh.
-   Sử dụng Safari làm trình duyệt web trên các thiết bị di động của Apple, vì nó mặc định chặn cookie T3.
-   Thay đổi cài đặt cookie và tracking trong cài đặt trình duyệt (đối với những trình duyệt khác).
-   Sử dụng Tor.
-   Cài đặt trình chặn quảng cáo hoặc các tiện ích bổ sung tương tự (Ghostery, Pivacy Badger, ...).

Mình mong rằng qua bài viết trên các bạn đã có cái nhìn chi tiết và đầy đủ cũng như hiểu rõ hơn cách Cookie hoạt động và là một nhân tố vô cùng quan trọng - một vấn đề lớn của bảo mật Internet ngày nay. Chúc các bạn duyệt web an toàn!

## Cơ chế hoạt động của internet

  * Internet hoạt động khá phức tạp nhưng có thể hiểu rằng Internet là một mạng lưới cáp vật lý toàn cầu. Có thể bao gồm dây đồng điện thoại, cáp TV, cáp quang. Ngay cả các kết nối không dây như Wifi, 3G, 4G, 5G cũng đều dựa vào các loại cáp vật lý này để truy cập vào internet.
  * Khi truy cập vào 1 trang web, máy tính sẽ gửi yêu cầu qua đường dây này tới máy chủ. Trong đó máy chủ chính là nơi lưu trữ các trang web và hoạt động như ổ cứng của máy tính mà bạn đang sử dụng hàng ngày. Khi bạn có lệnh yêu cầu thì máy chủ sẽ truy xuất trang web và đưa ra dữ liệu chính xác trở lại máy tính của bạn.

---
## Giải thích protocol của http và https

1. **HTTP**
    *  HTTP (Hypertext Transfer Protocol) là giao thức truyền tải siêu văn bản. Đây là giao thức tiêu chuẩn cho World Wide Web (www) để truyền tải dữ liệu dưới dạng văn bản, âm thanh, hình ảnh, video từ Web Server tới trình duyệt web của người dùng và ngược lại.
2. **HTTPS**
    * HTTPS (Hypertext Transfer Protocol Secure) là giao thức truyền tải siêu văn bản an toàn. Thực chất, đây chính là giao thức HTTP nhưng tích hợp thêm Chứng chỉ bảo mật SSL nhằm mã hóa các thông điệp giao tiếp để tăng tính bảo mật. Có thể hiểu, HTTPS là phiên bản HTTP an toàn, bảo mật hơn.
  HTTPS hoạt động tương tự như HTTP, tuy nhiên được bổ sung thêm chứng chỉ SSL (Secure Sockets Layer – tầng ổ bảo mật) hoặc TLS (Transport Layer Security – bảo mật tầng truyền tải). Hiện tại, đây là các tiêu chuẩn bảo mật hàng đầu cho hàng triệu website trên toàn thế giới.

---
## Cơ chế hoạt động của browser và sự khác nhau giữa các browser

1. **Cơ chế hoạt động của browser**
    * Endering engine sẽ bắt đầu nhận được nội dung của tài liệu yêu cầu từ lớp networking, thường sẽ thực hiện trong khối 8kB. Sau đó tiến hành rendering.
    Engine sẽ bắt đầu phân tích cú pháp tài liệu HTML và chuyển đổi các elements sang các nút DOM trong một cây gọi là "content tree". Engine sẽ phân tích dữ liệu "style", cả trong các tệp CSS bên ngoài tài liệu HTML và style được được viết bên trong tài liệu HTML. Kết thúc quá trình này sẽ tạo một cây khác gọi là render tree.
    Render tree có hình chữ nhật với các thuộc tính trực quan như màu sắc và kích thước. Các hình chữ nhật nằm đúng thứ tự được hiển thị trên màn hình.
    Sau khi xây dựng render tree nó đi qua một "layout" process. Điều này có nghĩa là đưa cho mỗi nút tọa độ chính xác nơi nó sẽ xuất hiện trên màn hình. Giai đoạn tiếp theo là painting–the render, tại đây mỗi nút sẽ được vẽ bằng cách sử dụng lớp UI backend.
    Đây là một quá trình dần dần. Để có trải nghiệm người dùng tốt hơn, công cụ hiển thị hình ảnh (rendering engine) sẽ cố gắng hiển thị nội dung trên màn hình càng sớm càng tốt. Nó sẽ không chờ cho đến khi tất cả HTML được phân tách cú pháp hoàn thành rồi mới bắt đầu xây dựng và bố trí render tree. Các phần của nội dung sẽ được phân tích cú pháp và hiển thị, trong khi quá trình tiếp tục với phần còn lại của nội dung tiếp tục đến từ mạng (network). 
2. **Sự khác nhau giữa các browser**
   1. **Google Chrome**
      * Về tốc độ, có thể nói ít có trình duyệt web nào lại có tốc độ xử lý nhanh như thế. Tất cả là nhờ một công cụ JavaScript mạnh mẽ và công cụ redenring WebKit mã nguồn mở.
      * Giao diện sử dụng cực đơn giản và thân thiện với người dùng với những tính năng như mở được cùng một lúc nhiều tab mà không bị lag, có thể lưu trữ thông tin người dùng nếu họ muốn, có thể cài đặt một số Add-on mà người dùng cần,... Quan trọng hơn là nó tương thích với mọi phần mềm ứng dụng cho máy tính, đặc biệt là phần mềm download IDM.
      * Bên cạnh đó, chế độ Incognito cho phép người sử dụng duyệt tư nhân thông qua việc vô hiệu ghi lịch sử, giảm theo dõi và loại bỏ các cookies theo dõi.
      * Sandboxing Chrome giúp ngăn chặn các phần mềm độc hại tự động cài trên máy tính của bạn hoặc ảnh hưởng đến các tab trình duyệt khác. Đồng thời, Google Chrome cũng thường xuyên cập nhật tự động các tính năng bảo mật nên an toàn và hiệu quả.

   2. **Mozilla Firefox**
       * Giống Chrome, Mozilla Firefox cũng có giao diện sử dụng đơn giản, có thể mở cùng một lúc nhiều tab. Hộp URL có tính năng trực tiếp tìm kiếm Google cũng như dự đoán/ tính năng lịch sử (gọi là Awesome Bar tự động).
       *  Tốc độ load mạng của Firefox dường như có phần không bằng với Chrome. Tuy nhiên, với nền tảng JagerMonkey JavaScript, việc tăng tốc độ cũng như cung cấp đồ họa của Firefox cũng khá ấn tượng. Cụ thể, Firefox có thể quản lý video phức tạp và nội dung trang web bằng cách sử dụng Direct2D layer-based và hệ thống đồ họa Driect3D.
       * Firefox là trình duyệt đầu tiên giới thiệu một tính năng duyệt web riêng tư, cho phép người dùng sử dụng internet nặc danh và an toàn. Điều này giảm tối thiểu cơ hội một người dùng bất kỳ có thể ăn cắp nhận dạng của bạn hoặc tìm kiếm thông tin bí mật.
   3. **Trình duyệt Web Cốc Cốc hay còn gọi là Cờ Rôm +**
       * Dễ dàng bắt link tải phim, nhạc, video: Trong khi việc download các bản nhạc, video, phim ở trong lớn như MP3.zing.vn, hay Youtube càng ngày càng thắt chặt và khắt khe làm cho người sử dụng chỉ có thể nghe và xem trực tuyến. Nhưng tất cả đã thay đổi khi họ chuyến sang dùng Cốc Cốc. Họ dễ dàng bắt link tự động, ngay cả link chất lượng cao như full HD hay FLV, mặt khác, sự tương thích giữa phần mềm download và Cốc Cốc còn giúp bạn tải nhanh gấp 8 lần so với bình thường.
       *  Đây cũng là lý do nó chưa phổ biến lắm trong mắt bạn bè quốc tế vì Cốc Cốc tập trung đáp ứng nhu cầu người Việt nhiều hơn như nâng cao năng lực phân giải các tên miền, cho phép tự động thêm dấu và sửa lỗi chính tả khi bạn viết sai.
       * Ngoài ra, nó còn có bộ tích ứng hỗ trợ tra từ điển Anh - Việt, vì vậy, bạn sẽ không mất công vào google dịch nữa.
   4. **Trình duyệt Web Microsoft Edge**
       * Microsoft Edge là trình duyệt web phổ biến mặc định trên hệ điều hành Windows 10. Edge ghi điểm bởi khả năng lướt web cực nhanh và độ tương tác với Cortana khá tốt. Đặc biệt, đây là công cụ thay thế cho các trình đọc file đuổi *.pdf. 
       * Hỗ trợ những tiện ích mở rộng tương tự như Google Chrome.
   5. **Trình duyệt Web Safari**
       * Opera là trình duyệt web đã từng rất nổi tiếng trên các thiết bị di động. Thật buồn vì hiện nay, Opera chỉ chiếm khoảng 1% thị trường trình duyệt web. Giao diện của Opera khá gần gũi với người dùng có kết hợp với chế độ đọc offline. Tuy tốc độ của trình duyệt Opera không mạnh mẽ giống như Chrome, nhưng lại có được sự ổn định. 
       * Hỗ trợ những tiện ích mở rộng tương tự như Google Chrome.
   6. **Trình duyệt Web Safari**
       * Safari là một trình duyệt website mặc định trên các thiết bị của Apple. Safari đã từng có sẵn cho Windows nhưng Apple đã ngừng sử dụng nó vài năm trước. Tuy nhiên giờ đây người dùng có thể sức thử nghiệm trình duyệt này trên các hệ điều hành không giống. 
       Safari phân phối cho người dùng tốc độ duyệt web khá tốt. Đi kèm là giao diện mới lạ và các tiện ích riêng biệt. 
   
   

---
## Cơ chế hoạt động của DNS và domain

  1. **Cơ chế hoạt động của DNS:**
     *  Domain Name System hoạt động từng bước theo cấu trúc của nó. Bước đầu là một truy vấn để lấy thông tin được gọi là “DNS query”.
      * Đầu tiên, DNS server sẽ tìm thông tin phân giải trong file hosts – tức file text trong hệ điều hành, chịu trách nhiệm chuyển hostname thành IP.
     * Nếu không thấy thông tin, nó sẽ quay về tìm trong cache – bộ nhớ tạm của phần cứng hay phần mềm. Nơi phổ biến nhất thường lưu thông tin này chính là bộ nhớ tạm của trình duyệt và bộ nhớ tạm ISP (Internet Service Providers. Nếu không nhận được thông tin, bạn sẽ thấy mã bị lỗi hiện lên.
  2. **Cơ chế hoạt động của DOMAIN:**
     * Khi nhập một domain name vào thanh URL của trình duyệt web, lúc này nó sẽ gửi yêu cầu truy cập đến một mạng lưới máy chủ toàn cầu hình thành nên hệ thống domain (DNS). Sau đó các máy chủ toàn cầu này sẽ tìm kiếm các máy chủ có tên được liên kết với domain và chuyển tiếp yêu cầu đến các máy chủ tên đó.
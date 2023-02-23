# HTTP-Tasks
*HTTP Protocol (HyperText Transfer Protocol)

 -HTTP là gì:
- Sử dụng Port 80
- Là giao thức tiêu chuẩn cho WWW (World Wide Web) để truyển tải dữ liệu dưới dạng văn bản, âm thanh, hình ảnh, video từ Web Server tới trình duyệt web của người dùng và ngược lại.HTTP cũng có thể được sử dụng để tìm nạp các phần của các doc nhằm cập nhật các trang web theo yêu cầu.
- Là nền tảng của bất kỳ sự trao đổi dữ liệu nào trên Web và cũng là giao thức giữa client (thường là các trình duyệt hay bất kỳ loại thiết bị, chương trình nào) và server (thường là các máy tính trên đám mây)

![image](https://user-images.githubusercontent.com/115911041/220407614-e3f3f4ed-d46d-4ea0-af97-6a7e228efa00.png)

 -Cấu trúc và hoạt động của HTTP:
- Dựa trên cấu trúc Client – Server. Client và Server giao tiếp với nhau bằng cách trao đổi các message độc lập (trái ngược với 1 luồng dữ liệu). Các message được gửi bởi client, thông thường là 1 trình duyệt web, được gọi là các yêu cầu và message được gửi bởi server như 1 sự trả lời, được gọi là phản hồi.

  VD: Khi bạn truy cập một trang web qua giao thức HTTP, trình duyệt sẽ thực hiện các phiên kết nối đến server của trang web đó thông qua địa chỉ IP do hệ thống phân giải tên miền DNS cung cấp. Máy chủ sau khi nhận lệnh, sẽ trả về lệnh tương ứng giúp hiển thị website, bao gồm các nội dung như: văn bản, ảnh, video, âm thanh,…
  
  ![image](https://user-images.githubusercontent.com/115911041/220512810-71afc293-6b15-401a-b006-e2d43ec39ad9.png)

 -Điểm yếu:
- Các thông tin được gửi đi qua giao thức HTTP (bao gồm địa chỉ IP, các thông tin mà bạn nhập vào website…) cũng không hề được mã hóa và bảo mật. Đây chính là kẽ hở mà nhiều hacker đã lợi dụng để đánh cắp thông tin người dùng, thường được gọi là tấn công sniffing. 
   
*HTTP Requests

- HTTP Request hiểu một cách đơn giản là các thông tin sẽ được gửi từ khách hàng (client) lên server. Server sẽ có nhiệm vụ tìm và xử lý các loại dữ liệu, thông tin, client mong muốn. HTTP Request có thể tồn tại dưới file text hoặc dưới dạng XML hoặc dạng Json. 
 
 ![image](https://user-images.githubusercontent.com/115911041/220544766-f3afe55a-eaad-40c1-a396-4ac7f600081b.png)
 
  -Cấu trúc HTTP Request:
 
 - ![image](https://user-images.githubusercontent.com/115911041/220554196-992ed92a-d27e-4cf1-8e25-fce4ae7127bf.png) 

 +Request line: đây là dòng đầu tiên của HTTP Request, với ba loại chính là method (phương thức), path (đường dẫn) hay URL và HTTP version (phiên bản giao thức). Cụ thể:

  - Phương thức (method) gồm nhiều loại nhưng phổ biến nhất là GET và POST. Trong đó, phương thức GET có tác dụng dùng để yêu cầu các tài nguyên cung cấp trong URL.
  - Đường dẫn (path) có tác dụng định danh các nguồn tài nguyên được yêu cầu bởi khách hàng, người dùng và bắt buộc phải có dấu “/”.
  - Phiên bản giao thức (HTTP version): Đây là phiên bản HTTP khách hàng dùng khá nhiều, trong đó phổ biến nhất là HTTP/1.0 hay HTTP/1.1.
  
 +Request header giúp client có thể gửi yêu cầu lên server. Mỗi yêu cầu sẽ kèm theo các thông số, và các thông số đó được gọi là Header Parameters. Trình duyệt và server sẽ dựa vào các thông số header này để trả dữ liệu và hiển thị dữ liệu cho phù hợp.Tương tự một HTTP Request, header sẽ phân biệt chữ thường và chữ hoa, theo sau đó là dấu “.” và một giá trị.Các thông số mà các bạn có thể gặp khá thường xuyên như:

  - User-Agent: cho phép server xác định ứng dụng, hệ điều hành, nhà cung cấp và phiên bản.
  - Connection: kiểm soát kết nối mạng. Nói cách khác, cho phép dừng hoặc tiếp tục kết nối sau khi server thực hiện xong yêu cầu.
  - Cache-Control: chỉ định chính sách bộ nhớ đệm của trình duyệt.
  - Accept-Language: cho biết tất cả các ngôn ngữ (tự nhiên) mà client có thể hiểu được.
  
  +Request body cho phép client gừi đến yêu cầu bổ sung cần server thực hiện như: tạo mới hoặc cập nhật dữ liệu mà không thể truyền trên Header Parameters.Thường được sử dụng trong các phương thức Post, Put, Patch.
 
*HTTP Responses
 
- HTTP Response được gọi là “thông báo phản hồi HTTP“. Đây là kết quả server trả về cho client.

![image](https://user-images.githubusercontent.com/115911041/220646314-f023597b-f0e5-46e6-99fd-b0c88351b347.png)

  -Nguyên lí hoạt động HTTP response:
  
  - Khi truy cập 1 địa chỉ abcdxyz.com, kết quả trả về (response) chính là giao diện của website và các thông tin của header.

  -Cấu trúc của HTTP response:
  
  - Sau khi nhận và phiên dịch thông báo yêu cầu, một Server gửi tín hiệu phản hồi với một thông báo phản hồi HTTP với cú pháp như sau:
  
  ![image](https://user-images.githubusercontent.com/115911041/220648862-c30de896-442b-45ea-98a6-440dba32cc29.png)
     
   HTTP-version: phiên bản HTTP cao nhất mà server hỗ trợ.
   
   Status-Code: mã kết quả trả về.
   
   Reason-Phrase: mô tả về Status-Code.
   
   Có thể giải thích như sau
   
   ![image](https://user-images.githubusercontent.com/115911041/220649247-771889f9-41c1-4b9c-84cd-a467798d18fb.png)
   
   -HTTP response status codes: Cho biết liệu một yêu cầu HTTP cụ thể đã được hoàn tất thành công hay chưa. Các câu trả lời được nhóm thành năm loại:

      - Informational responses (100 – 199)
      - Successful responses (200 – 299)
      - Redirection messages (300 – 399)
      - Client error responses (400 – 499)
      - Server error responses (500 – 599)
    
*URL (Uniform Resource Location)

- Là địa chỉ của tài nguyên duy nhất ở trên ưeb.Mỗi URL chỉ hợp lệ đến 1 tài nguyên duy nhất.Các tài nguyên đó có thể là trang HTML, tài liệu CSS, hình ảnh,..


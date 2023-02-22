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

 +Request line là dòng đầu tiên trong HTTP request. Nó bao gồm 3 phần:

  - Phương thức HTTP được sử dụng
  - URI( Uniform Resource Identifier) giúp xác định các tài nguyên mà client yêu cầu.
  - Phiên bản của giao thức HTTP
  
 +Request header giúp client có thể gửi yêu cầu lên server. Mỗi yêu cầu sẽ kèm theo các thông số, và các thông số đó được gọi là Header Parameters. Trình duyệt và server sẽ dựa vào các thông số header này để trả dữ liệu và hiển thị dữ liệu cho phù hợp.Các thông số mà các bạn có thể gặp khá thường xuyên như:

  - User-Agent: cho phép server xác định ứng dụng, hệ điều hành, nhà cung cấp và phiên bản.
  - Connection: kiểm soát kết nối mạng. Nói cách khác, cho phép dừng hoặc tiếp tục kết nối sau khi server thực hiện xong yêu cầu.
  - Cache-Control: chỉ định chính sách bộ nhớ đệm của trình duyệt.
  - Accept-Language: cho biết tất cả các ngôn ngữ (tự nhiên) mà client có thể hiểu được.
  
  +Request body cho phép client gừi đến yêu cầu bổ sung cần server thực hiện như: tạo mới hoặc cập nhật dữ liệu mà không thể truyền trên Header Parameters.Thường được sử dụng trong các phương thức Post, Put, Patch.
   
  -Một vài phương thức HTTP Request:
  
   - GET: Phương thức này dùng để truy cập dữ liệu từ máy chủ cụ thể.
   - HEAD: Phương thức không có thông báo trong nội dung, dùng khi đánh giá tính khả dụng của API tại điểm cuối.
   - POST: Phương thức này khá phổ biến, dùng khi muốn gửi thông tin đến máy chủ, cập nhật tài nguyên. Thông tin lưu trữ ở phần thân của HTTP Request sẽ được sử dụng.
   - PUT: Tài nguyên được cập nhật và truyền tải tuy nhiên các yêu cầu PUT sẽ không cố định, kết quả không đổi dù là bạn có yêu cầu PUT nhiều lần.
   - DELETE: Người dùng có thể xóa một tài nguyên nào đó trên máy chủ.
   - PATCH: PATCH cập nhật thông tin từ máy chủ, có áp dụng sửa lỗi một phần.
   - TRACE: Phương thức TRACE là cách để kiểm tra sự lặp lại theo đường dẫn của tài nguyên đích, dùng để chạy các thử nghiệm gỡ lỗi và thực hiện thao tác chẩn đoán trên API.
   -  CONNECT: CONNECT có tác dụng tạo kết nối đến máy chủ thông qua HTTP và tham số URL.
 

*HTTP Responses
 
 

  



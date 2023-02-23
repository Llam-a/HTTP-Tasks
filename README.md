# HTTP-Tasks
#HTTP Protocol (HyperText Transfer Protocol)

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
   
#HTTP Requests

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
 
#HTTP Responses
 
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
    
#URL (Uniform Resource )

- Mỗi website đều có 1 địa chỉ IP riêng gồm 1 dãy số dài và khó nhớ nên để thuận tiện cho việc truy cập, địa chỉ IP này được chuyển thành ngôn ngữ có thể dễ nhớ thành các URL

- Địa chỉ dạng chữ này được gọi là đường dẫn URL. Nhiệm vụ của URL là sẽ đưa người truy cập đến đúng website cần tìm.

VD:
    
     - https://developer.mozilla.org
     
     - https://developer.mozilla.org/en-US/docs/Learn/
    
     - https://developer.mozilla.org/en-US/search?q=URL

- Có 2 loại URL: 

  + URL động: Đây là URL có thể thay đổi. Thông thường, các diễn đàn hoặc website thiết kế mã nguồn mở sẽ dùng URL động. URL động bị đánh giá là không thân thiện với công cụ tìm kiếm.

  + URL tĩnh: Đây là URL không thể thay đổi. So với URL động, URL tĩnh được xếp hạng tốt hơn trong công cụ tìm kiếm, được index nhanh hơn.

 -Cấu trúc của URL:

  ![image](https://user-images.githubusercontent.com/115911041/220884591-1b39148f-d51f-4e73-9272-9726d5989081.png)

+Scheme:

  ![image](https://user-images.githubusercontent.com/115911041/220884663-1a1dfbb3-11dc-4c2f-8120-5949d46ced77.png)

  - Scheme đại diện cho phương thức mà trình duyệt web của bạn dùng để giao tiếp với server. Nhìn vào scheme, bạn sẽ biết được cách thức truyền tải dữ liệu giữa trình duyệt và server. Các loại scheme mà bạn sẽ thường gặp bao gồm:

  - HTTP: xác định các hành động của máy chủ với thao tác của người dùng trên trình duyệt web bằng các lệnh nhất định. HTTP sẽ sử dụng Port 80 để giao tiếp.
  - HTTPS: sử dụng SSL (Secure Socket Layer) để đảm bảo truyền dữ liệu an toàn giữa web server và trình duyệt website. HTTPS sẽ sử dụng port 433 để truyền dữ liệu.

+Authority (nhà cung cấp):

  ![image](https://user-images.githubusercontent.com/115911041/220884730-848a6f06-9e00-415a-b9d5-5432da617dc6.png)

  - Được phân tách khỏi scheme bằng kí tự ://. Authority bao gồm cả miền (ví dụ: www.example.com) và cổng (80), được phân tách bằng dấu hai chấm:

    - Miền cho biết máy chủ Web nào đang được yêu cầu. Thông thường, đây là một tên miền, nhưng địa chỉ IP cũng có thể được sử dụng (nhưng điều này rất hiếm vì nó kém tiện lợi hơn nhiều).
    
    - Port cho biết cổng được sử dụng để truy cập tài nguyên trên máy chủ web. Nó thường được bỏ qua nếu máy chủ web sử dụng các Port tiêu chuẩn của giao thức HTTP (80 cho HTTP và 443 cho HTTPS) để cấp quyền truy cập vào tài nguyên của nó. Nếu không thì nó là bắt buộc.

+Path to resource:

  ![image](https://user-images.githubusercontent.com/115911041/220884778-b060fe7a-524a-49ff-b558-1bbf2b992b92.png)

  `/path/to/myfile.html` là đường dẫn đến tài nguyên của web sever. 

+Parameters(tham số):

  ![image](https://user-images.githubusercontent.com/115911041/220884846-f6fedb36-563d-4ecb-80ed-fdb59f138a51.png)

  `?key1=value1&key2=value2` là tham số được bổ sung cho máy chủ web. Các tham số đó là danh sách key/value được phân tách bằng kí hiệu `&`.Máy chử web có thể sử dụng tham số để thực hiện công việc bổ sung trước khi trả lại tài nguyên

+Anchor:

 ![image](https://user-images.githubusercontent.com/115911041/220884915-2e073e1a-5185-4d05-b689-f9386dd37629.png)

  `#SomewhereInTheDocument` Anchor link là sử dụng để nói về một liên kết trỏ đến một vùng nào đó được chỉ định trên một trang, nó khác với Anchor text. Anchor Text chỉ một từ hay một cụm từ khóa có chứa liên kết.Dấu `#`, còn được gọi là mã định danh phân đoạn, không bao giờ được gửi đền máy chủ cùng với yêu cầu.
  
#HTTP Headers:

- Requesst Headers:

Accept Fields: Để chỉ định loại phản hồi nào được server chấp nhận thì các trường sau đây được sử dụng:

Accept

Trường này thông báo cho server loại dữ liệu nào có thể được trả về.

Trường Accept trong request HTTP có thể được sử dụng để chỉ định các loại MIME nhất định được client chấp nhận. Cú pháp chung như sau:

`<>Accept: <MIME_type>/<MIME_subtype> ;q=value`

Nhiều loại phương tiện có thể được phân tách bằng dấu phẩy. Giá trị tùy chọn q biểu thị mức chất lượng trên thang điểm từ 0 đến 1. Ví dụ:

`Accept: text/plain; q = 0,5, text/html, text/x-dvi; q = 0.8, Text/x-c`

Các chỉ thị có sẵn:

client hỗ trợ chính xác một loại MIME, chẳng hạn như văn bản/html:

`<MIME_type>/<MIME_subtype>`

MIME không có loại phụ được chỉ định. image/* khớp với image/png, image/svg, image/gif và tất cả các loại hình ảnh khác: /*.

`<MIME_type>/*`

Bất kỳ loại MIME nào:
`*/*`

Mỗi giá trị được sử dụng được đưa vào một thứ tự ưu tiên được biểu thị bằng cách sử dụng giá trị chất lượng tương đối được gọi là trọng số:

`;q= (trọng số hệ số q)`

Accept-Charset

Trường này được sử dụng trong các HTTP Header để chỉ định bộ ký tự nào mà client chấp nhận cho phản hồi.

Accept-Charset: character-set

Nếu một số bộ ký tự được chỉ định, hãy nhập chúng cách nhau bằng dấu phẩy. Ví dụ:

`Accept-Charset: iso-8859-5, Unicode-1-1; q = 0,8`

Accept-Encoding

Trường này giới hạn các thuật toán mã hóa được chấp nhận trong phản hồi. Cú pháp:

Accept-Encoding: encodings

Ví dụ:

    Accept-Encoding: gzip

    Accept-Encoding: *

    Accept-Encoding: gzip;q=0.7

    Accept-Language`

Trường header Accept-Language cho server biết ngôn ngữ mà con người có thể đọc được mà server dự kiến sẽ trả về. Đây là một dấu hiệu và không nhất thiết phải được kiểm soát hoàn toàn bởi người dùng. Server phải luôn tránh ghi đè lựa chọn rõ ràng của người dùng. Cú pháp là:

`Accept-Language: <language>; q=qvalue`

Nhiều ngôn ngữ có thể được phân tách bằng dấu phẩy. Ví dụ:

`Accept-Language: en-US; q=0.9`

Có thể tra cứu các giá trị được phép trong RFC 1766.
Authorization

Trường Authorization được sử dụng trong HTTP Header để xác thực tác nhân người dùng với server. Cú pháp như sau:

`Authorization:<type> <credentials>`

Cookie

header request HTTP Cookie chứa các cookie HTTP được lưu trữ trong các cặp tên/giá trị được server gửi trước đó bằng header Set-Cookie. Hành vi này có thể bị chặn bởi các trình duyệt để không có cookie nào được truyền đến server.

`Cookie: name1=value1; name2=value2; name3=value3`

Expect

Trường header request HTTP Mong đợi chỉ định các kỳ vọng của client mà server phải đáp ứng để request được xử lý đúng cách.

Cú pháp chung như sau:

`Expect : 100-continue`

From

Trường From của HTTP Header chứa địa chỉ email của người dùng kiểm soát ứng dụng khách request. Ví dụ:

`From: bkhost@example.com`

Trường From có thể được sử dụng trong các HTTP Header cho mục đích ghi nhật ký.

Host
Trường server được sử dụng trong các HTTP Header để chỉ định server internet và số cổng cho tài nguyên được request. Cú pháp là:

`Host: host:port`

Nếu số cổng bị thiếu, điều này có nghĩa là cổng mặc định 80.

If Fields

Các trường sau đây được sử dụng để chỉ định các điều kiện nhất định theo đó các tệp được request sẽ được trả về.

If-Match

Trường header này nhắc server chỉ gửi tệp được request nếu nó khớp với các thẻ thực thể được chỉ định. Cú pháp là:

`If-Match: entity-tag`

Ví dụ:

`If-Match: "*"`

Dấu hoa thị (*) cho biết có thể gửi bất kỳ tệp nào.

If-Modified-Since

If-Modified-Since được chỉ định trong HTTP Header, tài nguyên được request sẽ chỉ được server phân phối nếu nó đã được thay đổi kể từ ngày được chỉ định. Nếu không, sẽ không có giao hàng và trang sẽ được tải từ bộ đệm của trình duyệt. Cú pháp:

`If-Modified-Since: HTTP date`

Ví dụ:

`If-Modified-Since: Sat, 13 Oct 2017 15:16:27 GMT`

If-None-Match

Trường này nhắc server chỉ gửi tệp được request nếu nó không khớp với bất kỳ thẻ thực thể nào được chỉ định. Cú pháp là:

`If-None-Match: entity-tag`

Ví dụ:

`If-None-Match: "xyzzy"`

`If-None-Match: *`

If-Range

Trường header If-Range được sử dụng trong các HTTP Header để chỉ request một phần nội dung bị thiếu nếu nội dung chưa được thay đổi và toàn bộ nội dung nếu một thay đổi đã được thực hiện đối với nó. Cú pháp như sau:

`If-Range: entity-tag/HTTP date`

Có thể sử dụng thẻ thực thể hoặc ngày:

`If-Range: Sat, 13 Oct 2017 15:16:27 GMT`

Nếu nội dung chưa được thay đổi, server sẽ trả về phạm vi byte được chỉ định bởi header phạm vi. Nếu không, toàn bộ tài liệu mới được trả lại.

If-Unmodified-Since

Cú pháp chung là:

`If-Unmodified-Since: HTTP date`

Trường này được sử dụng giống như trường If-Modified-Since field.

Proxy-Authorization

Trường header Proxy-Authorization cho phép client xác định chính nó hoặc người dùng với proxy. Cú pháp:

`Proxy-Authorization: <type> <credentials>`

Range

Trường header Phạm vi chỉ định các phạm vi phụ của nội dung được request. Cú pháp là:

`Range: bytes-unit=first-byte-pos "-" [last-byte-pos]`

Các giá trị “first-byte-pos” và “last-byte-pos” chỉ định byte đầu tiên và byte cuối cùng của nội dung được bao gồm nhưng không nhất thiết phải được chỉ định cả hai. Nhiều khu vực nội dung có thể được phân tách bằng dấu phẩy.

Referrer

Trường header Người giới thiệu cho phép khách hàng chỉ định địa chỉ (URL) của tài nguyên mà URL được request từ đó. Cú pháp chung như sau:

`Referer: URL`

Ví dụ:

`Referer: http://www.example.com`

User-Agent

Trường header này gửi thông tin về client đến server. Ví dụ, cú pháp có thể như sau:

`User-Agent: <product>/<product version> <comment>`

- Response Headers:

Acess-Control-Allow: cho biết liệu phản hồi có thể được chia sẻ với requesting code từ nguồn gốc đã cho hay không.

Cache-Control: Chuyển các cache xác định tới trình duyệt

Etag: 

Exprise

Location

Pragma

Sever

Set-Cookie

WWW-Authenticate

X-Frame-Options

*Cookies

Một phần quan trọng của HTTP mà hầu hết các ứng dụng web dựa và. Thông thường, chúng có thể sử dụng để khai thác các lỗ hổng. Các cơ chế cookie cho phép máy chủ gửi các mục dữ liệu đến khách hàng, khách hàng lưu trữ và gửi lại cho máy chủ. Không giống như các loại parameters khác(tham số), cookie tiếp tục được gửi lại trong mỗi yêu cầu tiếp theo mà không có bất kỳ yêu cầu cụ thể nào hành động theo yêu cầu của ứng dụng hoặc người dùng.

`Set-Cookie: tracking=tI8rk7joMx44S2Uu85nSWc`

*HTTPS (Hypertext Transfer Protocol Secure)

Sử dụng Port 443

Là giao thức truyền tải siêu văn bản an toàn. Thực chất, đây chính là giao thức HTTP nhưng tích hợp thêm Chứng chỉ bảo mật SSL nhằm mã hóa các thông điệp giao tiếp để tăng tính bảo mật. Có thể hiểu, HTTPS là phiên bản HTTP an toàn, bảo mật hơn.

HTTPS hoạt động tương tự như HTTP, tuy nhiên được bổ sung thêm chứng chỉ SSL (Secure Sockets Layer – tầng ổ bảo mật) hoặc TLS (Transport Layer Security – bảo mật tầng truyền tải). Hiện tại, đây là các tiêu chuẩn bảo mật hàng đầu cho hàng triệu website trên toàn thế giới.

#HTTP Proxies

Proxy được hiểu đơn giản là sợi dây liên kết giữa người truy cập Internet và Internet, dùng để thực hiện chuyển tiếp thông tin và kiểm soát sự an toàn cho người dùng. Có thể nói, cách thức hoạt động của Proxy như một tường lửa (firewall), hoặc là một bộ lọc truy cập web.

Có 2 sự khác biệt trong cách thức hoạt động của HTTP khi một proxy đang được sử dụng:

  - Khi một trình duyệt đưa ra yêu cầu không được mã hóa HTTP tới một máy chủ proxy đầy đủ vào yêu cầu, bao gồm tiền tố giao thức http://, sever's hostname, và số pory nếu những điều này không chính xác. Các máy chủ proxy trích xuất hostname, port và sử dụng chúng để điều hướng yêu cầu đến đúng máy chủ web.

  - Khi một HTTPS đang được sử dụng, trình duyệt không thể thực hiện bắt tay với SSL với máy chủ proxy, vì điều này sẽ phá vỡ đường hấm an toàn và để lại thông tin liên lạc dễ bị tấn công đánh chặn.Kể từ đây, trình duyệt phải sử dụng proxy làm chuyển tiếp cấp TCP thuần túy, chuyển tiếp tất cả dữ liệu mạng theo cả hai hướng giữa trình duyệt và máy chủ web đích mà trình duyệt thực hiện bắt tay SSL như bình thường. Để thiết lập chuyển tiếp này, trình duyệt tạo một yêu cầu HTTP tới máy chủ proxy bằng phương thức CONNECT và chỉ định tên máy chủ và số cổng làm URL. Nếu proxy cho phép yêu cầu, nó trả về phản hồi HTTP với trạng thái 200, giữ kết nối TCPmở và từ thời điểm đó trở đi hoạt động như một chuyển tiếp cấp TCP tới máy chủ web.


#HTTP Authentication

Giao thưc HTTP bao gồm các cơ chế riêng để xác thực người dùng bằng cách sử dụng các lược đố xác thực khác nhau, bao gồm:

- Basic: là một cơ chế xác thực đơn giản gửi thông tin đăng nhập của người dùng dưới dạng chuỗi được mã hóa Base64 trong tiêu đề yêu cầu với mỗi thông báo.

- NTLM:  là một bộ giao thức bảo mật của Microsoft nhằm cung cấp tính năng xác thực, tính toàn vẹn và tính bảo mật cho người dùng. NTLM là sự kế thừa của giao thức xác thực trong Microsoft LAN Manager, một sản phẩm cũ của Microsoft.

- Digest: là một trong những phương thức đã thỏa thuận mà máy chủ web có thể sử dụng để thương lượng thông tin xác thực, chẳng hạn như tên người dùng hoặc mật khẩu, với trình duyệt web của người dùng. Điều này có thể được sử dụng để xác nhận danh tính của người dùng trước khi gửi thông tin nhạy cảm, chẳng hạn như lịch sử giao dịch ngân hàng trực tuyến.

#HTTP Method:

`GET`

Phương thức `GET` yêu cầu biểu diễn tài nguyên đã chỉ định. Các yêu cầu sử dụng `GET` chỉ nên truy xuất dữ liệu.

`HEAD`

Phương thức `HEAD` yêu cầu một phản hồi giống với yêu cầu `GET`, nhưng không có phần thân phản hồi.

`POST`

Phương thức `POST` gửi một thực thể tới tài nguyên đã chỉ định, thường gây ra thay đổi về trạng thái hoặc tác dụng phụ trên máy chủ.

`PUT`

Phương thức `PUT` thay thế tất cả các biểu diễn hiện tại của tài nguyên đích bằng tải trọng yêu cầu

`METHOD`

Phương thức `DELETE` xóa tài nguyên đã chỉ định.

`CONNECT`

Phương thức `CONNECT` thiết lập một đường hầm tới máy chủ được xác định bởi tài nguyên.

`OPTIONS`

Phương thức `OPTIONS` mô tả các tùy chọn giao tiếp cho tài nguyên.

`TRACE`

Phương thức `TRACE` thực hiện kiểm tra vòng lặp thông báo dọc theo đường dẫn đến tài nguyên.

`PATCH`

Phương thức `PATCH` áp dụng các sửa đổi một phần cho tài nguyên.










# 1. Bảo mật dữ liệu, phân quyền và những điều cần biết
Trong kỷ nguyên số, dữ liệu được xem là tài sản quý giá của mọi doanh nghiệp. Việc bảo vệ và quản lý dữ liệu hiệu quả không chỉ là vấn đề công nghệ, kỹ thuật mà còn liên quan chặt chẽ đến con người và quy trình. Bài viết này sẽ đi sâu vào những khía cạnh quan trọng của bảo mật dữ liệu, phân quyền và tầm quan trọng của quản trị dữ liệu (data governance) trong việc đảm bảo an toàn thông tin cho doanh nghiệp.

## 1.1. Bảo mật dữ liệu: Nhiều lớp phòng thủ
Bảo mật dữ liệu không chỉ đơn thuần là việc cài đặt phần mềm diệt virus hay tường lửa. Đó là một hệ thống nhiều lớp,bao gồm:

- Bảo mật vật lý: Đảm bảo an toàn cho trung tâm dữ liệu, máy chủ, thiết bị lưu trữ.
- Bảo mật mạng: Kiểm soát truy cập, phát hiện và ngăn chặn xâm nhập trái phép.
- Bảo mật ứng dụng: Xác thực người dùng, phân quyền truy cập, mã hóa dữ liệu.
Bảo mật dữ liệu: Mã hóa dữ liệu nhạy cảm, sao lưu và phục hồi dữ liệu.

## 1.2. Phân quyền: Nguyên tắc "Chỉ biết những gì cần biết"
Phân quyền là việc cấp quyền truy cập dữ liệu cho người dùng dựa trên vai trò và trách nhiệm của họ. Nguyên tắc "Chỉ biết những gì cần biết" giúp giảm thiểu rủi ro rò rỉ dữ liệu và đảm bảo tính toàn vẹn của thông tin.

Để dễ hình dung, bạn có thể nghĩ về nguyên tắc này thông qua những ví dụ sau:

- Nhân viên kinh doanh chỉ được phép xem các bảng dữ liệu, report, dashboard về số liệu bán hàng, không được phép truy cập vào dữ liệu của tài chính, pháp lý, nhân sự...
- Giám đốc vùng có thể được truy cập vào mọi dữ liệu về kinh doanh, chi phí, vận hành của vùng mà người đó quản lý, nhưng không được xem các vùng khác và không xem được số liệu tổng của cả nước
Hiện nay đa số các công cụ data warehouse, công cụ làm report, dashboard đều sẽ có những chức năng phân quyền để hỗ trợ bạn hiện thực hóa nguyên tắc này

## 1.3. Quản trị dữ liệu: Vấn đề của con người và quy trình
Quản trị dữ liệu (data governance) là một hệ thống các chính sách, quy trình và quy định nhằm đảm bảo dữ liệu được quản lý và sử dụng một cách có trách nhiệm. Data governance không chỉ liên quan đến công nghệ mà còn đòi hỏi sự tham gia của tất cả các bộ phận trong doanh nghiệp.

Một số ví dụ rất nhỏ của các hoạt động liên quan tới data governance:
- **Lập nhóm quản lý dữ liệu**: Tưởng tượng như lập một đội bóng đá, mỗi người trong đội đến từ các phòng ban khác nhau trong công ty. Đội này có nhiệm vụ đưa ra các quyết định quan trọng về cách quản lý dữ liệu.
- **Soạn bộ quy tắc quản lý dữ liệu**: Giống như luật lệ trong một trò chơi, bộ quy tắc này nói rõ cách thu thập, lưu trữ,sử dụng và chia sẻ dữ liệu. Ví dụ, có quy định cụ thể về cách xử lý thông tin cá nhân của khách hàng.
- **Chỉ định người quản lý dữ liệu**: Cũng giống như mỗi đồ vật trong nhà có người giữ gìn, mỗi loại dữ liệu sẽ có một người chịu trách nhiệm đảm bảo dữ liệu đó chính xác, đáng tin cậy và an toàn.
- **Kiểm tra việc quản lý dữ liệu**: Thỉnh thoảng, sẽ có người kiểm tra xem mọi người có tuân thủ bộ quy tắc quản lý dữ liệu hay không, giống như trọng tài trong một trận đấu vậy.
- **Đào tạo nhân viên**: Tổ chức các buổi học để mọi người hiểu rõ tầm quan trọng của việc quản lý dữ liệu đúng cách và cách thực hiện nó, giống như huấn luyện các cầu thủ trước khi ra sân.

## 1.4. Yếu tố con người: Mắt xích quan trọng
Con người là yếu tố quan trọng nhất trong bảo mật dữ liệu. Nhân viên cần được đào tạo về các chính sách bảo mật, nhận thức được tầm quan trọng của việc bảo vệ dữ liệu và biết cách phòng tránh các cuộc tấn công mạng. Cũng liên quan tới chính sách data governance, bạn cũng cần chú ý đến việc quản lý dữ liệu để tránh việc dữ liệu bị rò rỉ ra bên ngoài, bị rò rỉ cho đối thủ.

## Kết bài
Tóm lại, có những điều quan trọng sau khi đọc bài này:
- **Đánh giá rủi ro**: Thường xuyên đánh giá rủi ro bảo mật và cập nhật các biện pháp phòng ngừa.
- **Giám sát**: Liên tục giám sát hệ thống để phát hiện sớm các dấu hiệu bất thường.
- **Phản ứng sự cố**: Xây dựng kế hoạch ứng phó sự cố để giảm thiểu thiệt hại khi xảy ra sự cố bảo mật.
- **Tuân thủ**: Tuân thủ các quy định về bảo mật dữ liệu.

Bảo vệ dữ liệu là trách nhiệm của tất cả mọi người trong doanh nghiệp. Bằng cách áp dụng các biện pháp bảo mật toàn diện, phân quyền hợp lý và xây dựng một hệ thống quản trị dữ liệu hiệu quả, doanh nghiệp có thể bảo vệ tài sản quý giá của mình và xây dựng niềm tin với khách hàng và đối tác.

# 2. Data Automation và rút ngắn thời
Khi bạn đang ở level này, khả năng cao là bạn đã hiểu lý do vì sao mình cần số, cách dùng số như thế nào cho hoạt động kinh doanh của mình, và data quan trọng như thế nào trong việc vận hành doanh nghiệp. Chúc mừng bạn!

Tới level này, chúng mình muốn truyền tải thêm cho bạn một thông tin nữa, đó là làm sao để có thể tự động hóa việc trích xuất, thu thập dữ liệu, vì đến cuối cùng thì cái gì làm tay mãi cũng chán, cái gì phụ thuộc con người thì luôn có thể bị sai sót.

## 2.1. Data automation là gì?
Mình sẽ mượn định nghĩa của Databricks như sau:

*Tự động hóa dữ liệu là một **kỹ thuật quản lý dữ liệu** ngày càng phổ biến. Tự động hóa dữ liệu cho phép một tổ chức **thu thập, tải lên, chuyển đổi, lưu trữ, xử lý và phân tích dữ liệu** bằng cách sử dụng các công nghệ mà không cần sự can thiệp thủ công của con người.*

Nói cách khác, data automation cho phép bạn sử dụng data một cách hiệu quả, nhanh chóng thông qua các công nghệ, công cụ tự động, giảm sự can thiệp thủ công (ví dụ: phải tải file Excel số liệu từ sàn thương mại điện tử mỗi ngày).

## 2.2. Ưu điểm của data automation
### Giảm sự can thiệp của con người
Không còn phải đi tải về các file Excel, CSV từ những hệ thống vận hành, hệ thống quảng cáo nữa, dữ liệu sẽ được tự động đưa vào hệ thống phân tích và sẵn sàng cho bạn sử dụng. Ngoài ra, khâu chuẩn bị số liệu thường tốn nhiều thời gian và nhàm chán, loại bỏ được khâu này sẽ giúp nhân viên có thêm thời gian để làm những việc tạo ra giá trị cao hơn.

### Tăng tính chính xác
Do không cần người xử lý thủ công mỗi lần mỗi khác, mọi thứ đã được quy trình hóa, tự động hóa, nên cứ đưa dữ liệu đầu vào là hệ thống sẽ tự đưa ra kết quả cuối cùng, giảm rủi ro do con người thao tác. Thêm vào đó, hạn chế được tình trạng chỉnh sửa dữ liệu trái phép nhằm phục vụ cho mục đích xấu.

### Giảm thời gian có dữ liệu
Dữ liệu sẽ được cung cấp cho bạn chính xác, kịp thời, nhanh chóng để ra quyết định với độ trễ ít nhất có thể. Không còn phải đợi 1 tuần, 1 ngày để biết được hiệu quả hoạt động của tổ chức, mà có thể chỉ là 1 tiếng, hay thậm chí vài phút.

## 2.3. Một số ví dụ của data automation
### ETL (Extract - Transform - Load)
Một phương pháp thường được dùng để tự động hóa dữ liệu là **ETL** (Extract - Transform - Load), thường dùng để thu thập dữ liệu tự động. Phương pháp này đã bắt đầu từ hàng chục năm nay, và hiện tại có thêm những biến thể mới như ELT (Extract - Load - Transform) khi năng xử lý của máy tính ngày càng mạnh mẽ hơn và dung lượng lưu trữ ngày càng rẻ hơn.

Một luồng ETL thường sẽ được hẹn giờ để bắt đầu chạy, ví dụ:
- 7h sáng mỗi ngày, trích xuất dữ liệu từ API của Facebook Ads và đưa dữ liệu về data warehouse của công ty.
- Cứ 15 phút một lần, trích xuất dữ liệu từ database của hệ thống CRM và đưa vào data warehouse để đưa lên báo cáo kết quả hoạt động kinh doanh

### Streaming data
Ngày nay khi dữ liệu sinh ra ngày càng lớn, có thể phát sinh theo thời gian thực rất nhanh, nên người ta còn thêm một kỹ thuật nữa gọi là Streaming. Phương pháp này cho phép công ty lấy dữ liệu từ các nguồn theo một luồng liên tục, và dữ liệu sẽ sẵn sàng để sử dụng sau chỉ vài phút, thậm chí vài giây, cho phép việc ra quyết định nhanh chóng hơn. Tuy nhiên, streaming cũng phức tạp hơn về mặt công nghệ và có thể sẽ tốn chi phí hơn.

### Triggered data
Đây là một kỹ thuật mà dữ liệu sẽ được cập nhật, thay đổi dựa theo một thay đổi khác từ một nguồn nào đó. Ví dụ: khi khách hàng chuyển trạng thái thành "Khách hàng thân thiết", hãy gửi một dữ liệu để cập nhật thêm tiền thường +500.000.

Thông thường, triggered data đã được tích hợp trong một hệ thống, một quy trình xử lý rồi, nhưng nó cũng có thể được tích hợp từ các hệ thống bên ngoài để thực hiện thêm nhiều chức năng mở rộng.

## 2.4. Những thách thức của data automation
### Thêm chi phí đầu tư cho một hệ thống data automation
Các hệ thống công nghệ giúp cho việc tự động hóa luồng dữ liệu chắc chắn sẽ là một khoản tiền mà các doanh nghiệp phải chi ra. Để khoản đầu tư này trở nên hiệu quả, sẽ cần có kiến thức để ứng dụng nó, nếu không thì hệ thống đó trở nên lãng phí. Dễ thấy nhất là hệ thống đã xong, báo cáo đã lên, nhưng lại không khớp với nhu cầu thực tế nên không ai sử dụng được.

Nhưng ngược lại, nếu ứng dụng thành công, thì nó giúp giải phóng nhân viên khỏi việc làm thủ công, lấy lại nhiều giờ công và tăng năng suất, đồng thời bổ sung khả năng ra quyết định nhanh chóng.

### Thay đổi về nhân sự trong tổ chức
Khi việc tự động hóa dữ liệu đã triển khai xong, có thể một số nhân viên chuyên đi trích xuất dữ liệu sẽ không còn phải làm việc đó nữa. Các tổ chức thường sẽ bố trí lại công việc phù hợp cho họ, nhưng cũng có những trường hợp mọi thứ đã tự động hóa nên không còn việc để họ làm. Hãy luôn nghĩ đến việc tổ chức lại cơ cấu nhân sự để có thể tối ưu hơn về chi phí, về trải nghiệm của nhân viên khi đã triển khai hệ thống data automation.

### Cần phải học thêm nhiều kỹ năng, công cụ mới
Giống mọi hệ thống máy tính, hệ thống công nghệ mới trong môi trường doanh nghiệp, sẽ luôn cần học lại một thứ gì đó, hoặc nhiều thứ, để có thể vận hành hệ thống trơn tru. Ví dụ: một tổ chức trước giờ chỉ toàn sử dụng Excel để xem báo cáo, giờ phải học lại cách sử dụng PowerBI hay Looker Studio để trình bày và xem dashboard. Một tổ chức trước giờ chỉ toàn làm báo cáo với file Excel, một số nhân sự có thể phải học thêm SQL để có thể truy xuất dữ liệu một cách hiệu quả.

# 3. Ra quyết định với data như thế nào cho đúng
**Ra quyết định với dữ liệu: Nghệ thuật biến số thành cơ hội!**
Dù bạn là nhà lãnh đạo doanh nghiệp, nhà quản lý, hay thậm chí là một cá nhân đang tìm cách cải thiện cuộc sống, dữ liệu đều có thể là "kim chỉ nam" giúp bạn đạt được mục tiêu. Tuy nhiên, dữ liệu không tự nói lên điều gì. Chúng ta cần biết cách lắng nghe, phân tích và diễn giải để khai thác hết tiềm năng của chúng.

## 3.1. Xác định rõ mục tiêu: Từ mong muốn đến hành động cụ thể
Mục tiêu không chỉ đơn thuần là đích đến, mà còn là động lực thúc đẩy chúng ta hành động. Ví dụ, một doanh nghiệp bán lẻ không chỉ muốn "tăng doanh thu", mà còn cần xác định rõ: tăng trưởng 20% trong quý tới, tập trung vào dòng sản phẩm mới, thông qua các kênh bán hàng trực tuyến. Mục tiêu càng rõ ràng, càng dễ dàng xác định những dữ liệu cần thiết để đo lường và đánh giá hiệu quả.

## 3.2. Sử dụng đúng số liệu: Chọn lọc thông tin, tối ưu hóa hiệu quả
Tương tự như việc bác sĩ cần những xét nghiệm phù hợp để chẩn đoán bệnh, nhà quản lý cũng cần những số liệu phù hợp để đưa ra quyết định chính xác. Ví dụ, để đánh giá sự hài lòng của khách hàng, không chỉ dựa vào số lượng đơn hàng, mà còn cần xem xét các chỉ số như tỷ lệ khách hàng quay lại, điểm đánh giá trung bình, nội dung phản hồi...

Tuy nhiên, cũng cần giới hạn lại các chỉ số ở một quy mô nhất định. Đôi khi chỉ 1 chỉ số thôi đã nói lên vấn đề, trong khi nếu bạn chọn 10 chỉ số để giải quyết vấn đề thì lại khiến mọi thứ rối tung lên và khó tập trung vào việc phân tích, cải thiện hiệu quả.

Một sai lầm thường thấy là trong một dashboard, bạn yêu cầu nhân viên phân tích đưa vào quá nhiều số liệu, có thể lên đến 20, 30 chỉ số. Đây là một ví dụ của một dashboard không hiệu quả, vì khi sử dụng bạn sẽ rối, ham xem nhiều số lại nhưng không tập trung.

## 3.3. Thà không có số, còn hơn dùng dữ liệu sai: Chất lượng hơn số lượng
Dữ liệu sai lệch giống như một tấm bản đồ mờ ảo, có thể dẫn chúng ta đi lạc đường. Ví dụ, nếu dựa vào dữ liệu nhân khẩu học không chính xác, một chiến dịch quảng cáo có thể nhắm đến sai đối tượng, gây lãng phí ngân sách và không đạt được hiệu quả mong muốn. Hay một sai sót về dữ liệu doanh thu của cửa hàng theo vùng có thể khiến bạn ra quyết định sai trong việc chọn chỗ để đầu tư mở rộng trong năm mới.

Thế nên hãy luôn cẩn thiện, kiểm tra kỹ số liệu trước khi cung cấp cho người khác, hoặc trước khi bạn sử dụng.

## 3.4. Luôn nhìn vào bối cảnh: Đọc hiểu câu chuyện đằng sau con số
Giống như một bức tranh, dữ liệu chỉ có ý nghĩa khi đặt trong bối cảnh cụ thể. Ví dụ, tỷ lệ nhân viên nghỉ việc tăng cao có thể là dấu hiệu của một môi trường làm việc độc hại, nhưng cũng có thể là kết quả của việc tái cấu trúc công ty hoặc sự thay đổi trong ngành.

Hoặc bạn nhận thấy doanh thu của một ngày nào đó bỗng nhiên tăng vọt, nhưng khoan hãy vội mừng, đôi khi đó là kết quả của việc sàn thương mại điện tử chạy quảng cáo, họ có một ngày đôi (ví dụ: 11/11) đang diễn ra, chứ không hẳn là do bạn tác động.

Việc hiểu rõ bối cảnh xảy phát sinh ra số liệu đó sẽ giúp bạn ra quyết định chính xác hơn, thay vì chỉ dựa vào 1 chấm dữ liệu vô hồn.

## 3.5. Data chỉ là công cụ hỗ trợ: Kết hợp giữa khoa học và nghệ thuật
Một bản nhạc hay không chỉ cần những nốt nhạc chính xác, mà còn cần sự sáng tạo và cảm xúc của người nghệ sĩ. Tương tự, dữ liệu chỉ là một phần của quá trình ra quyết định. Chúng ta cần kết hợp giữa phân tích logic và trực giác để đưa ra những lựa chọn tốt nhất. Vì cuối cùng thì đây là việc kinh doanh, nó không chỉ là một cách đo đếm khoa học mà còn phải dựa vào yếu tố thị trường, con người, bối cảnh, pháp luật, những thứ mà chỉ 1 con số không thể nói lên hết mọi chuyện.

Đây cũng là lý do mà các hệ thống data thường được gọi là decision-support system (DSS), dịch ra có nghĩa là: Hệ thống hỗ trợ ra quyết định.

Trong thời đại số hóa, dữ liệu là một tài sản vô giá. Tuy nhiên, giá trị của dữ liệu không nằm ở số lượng, mà nằm ở cách chúng ta sử dụng chúng. Bằng cách áp dụng những nguyên tắc trên, bạn có thể biến dữ liệu thành "người bạn đồng hành" đáng tin cậy, giúp bạn vượt qua những thách thức và đạt được thành công.
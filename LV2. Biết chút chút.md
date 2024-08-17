# 1. CSDL, Bảng, Quan hệ và SQL
Cơ sở dữ liệu (Database) là một tập hợp các dữ liệu có tổ chức, được lưu trữ và truy xuất bằng các hệ thống máy tính. Dữ liệu trong cơ sở dữ liệu thường được lưu trữ trong các bảng (Tables) và được liên kết với nhau thông qua các mối quan hệ (Relationships).

## 1.1. Database là gì?

### 1.1.1. Cơ Sở Dữ Liệu (Database)
Cơ sở dữ liệu là một kho lưu trữ dữ liệu có cấu trúc. Mục tiêu chính của cơ sở dữ liệu là cung cấp cách lưu trữ và truy xuất dữ liệu hiệu quả.

*Ví Dụ: Hệ thống quản lý sinh viên cần cơ sở dữ liệu để lưu thông tin về sinh viên, lớp học, môn học, điểm của từng mônHệ thống quản lý đơn hàng phải dùng cơ sở dữ liệu để lưu trữ đơn hàng, sản phẩm, khách hàng, tồn kho...*

Trong giới hạn của chương trình Data Literacy, chúng ta sẽ tìm hiểu chủ yếu là về cơ sở dữ liệu quan hệ (relational database) vì nó được dùng phổ biến trên toàn toán thế giới để lưu trữ các thông tin về kinh doanh.

### 1.1.2. Hệ quản trị cơ sở dữ liệu (Database Management System - DBMS)
Hệ quản trị cơ sở dữ liệu (Database Management System - DBMS) là một phần mềm được sử dụng để quản lý các cơ sở dữ liệu. DBMS cung cấp một giao diện giữa người dùng và cơ sở dữ liệu, cho phép người dùng truy cập, thao tác và quản lý dữ liệu một cách hiệu quả.

Các Chức Năng Chính của DBMS
- Quản lý Dữ liệu: Tạo, đọc, cập nhật và xóa dữ liệu trong cơ sở dữ liệu.
- Kiểm soát Truy cập: Quản lý quyền truy cập của người dùng vào dữ liệu.
- Quản lý Giao dịch: Đảm bảo tính toàn vẹn và nhất quán của dữ liệu khi có nhiều giao dịch diễn ra đồng thời.
- Sao lưu và Phục hồi: Cung cấp các cơ chế để sao lưu và khôi phục dữ liệu trong trường hợp xảy ra sự cố.

Ví Dụ về Các Hệ Quản Trị Cơ Sở Dữ Liệu Phổ Biến
- MySQL: Hệ quản trị cơ sở dữ liệu mã nguồn mở phổ biến cho các ứng dụng web.
- PostgreSQL: Hệ quản trị cơ sở dữ liệu mã nguồn mở mạnh mẽ với nhiều tính năng tiên tiến.
- Oracle Database: Hệ quản trị cơ sở dữ liệu thương mại mạnh mẽ và bảo mật cao, thường dùng trong lĩnh vực tài chính, ngân hàng.
- Microsoft SQL Server: Hệ quản trị cơ sở dữ liệu của Microsoft với tích hợp tốt trong môi trường Windows.

### 1.1.3. Bảng (Table)
Một bảng trong cơ sở dữ liệu là một cấu trúc bao gồm các hàng (rows) và cột (columns), trong đó mỗi hàng đại diện cho một bản ghi (record) và mỗi cột đại diện cho một trường dữ liệu (field).

Ví Dụ:

- **Bảng Sinh Viên**
![image](https://github.com/user-attachments/assets/3dd4d453-1d6a-4f51-b465-9bc32508bc9e)

- **Bảng Sản phẩm**
![image](https://github.com/user-attachments/assets/586d8079-6ac2-4cb9-b9d3-feadb43268f7)

- **Bảng Đơn Hàng**
![image](https://github.com/user-attachments/assets/9174f93b-f2d3-4ece-995f-3aaf712f17f2)

### 1.1.4. Quan Hệ (Relationship)
Quan hệ trong cơ sở dữ liệu đề cập đến cách các bảng liên kết với nhau. Các loại quan hệ phổ biến bao gồm:

- One-to-One (1-1): Một hàng trong bảng này liên kết với một hàng trong bảng khác.
- One-to-Many (1-N): Một hàng trong bảng này liên kết với nhiều hàng trong bảng khác.
- Many-to-Many (N-N): Nhiều hàng trong bảng này liên kết với nhiều hàng trong bảng khác.

Ví Dụ quan hệ giữa bảng Sinh Viên và bảng Lớp Học:
- Một sinh viên có thể học nhiều lớp.
- Một lớp có thể có nhiều sinh viên.
![image](https://github.com/user-attachments/assets/23a801dc-b678-40a3-8d28-9d4c9c74148e)


## 1.2. SQL (Structured Query Language)
SQL là ngôn ngữ chuẩn để quản lý và thao tác cơ sở dữ liệu quan hệ. SQL cho phép bạn thực hiện các thao tác như:

- **SELECT**: Truy vấn dữ liệu từ một bảng.
- **INSERT**: Thêm dữ liệu mới vào một bảng.
- **UPDATE**: Cập nhật dữ liệu trong một bảng.
- **DELETE**: Xóa dữ liệu từ một bảng.

Ví dụ: Đây là câu SQL SELECT để Lấy danh sách các sinh viên, bao gồm tên và lớp học, của toàn trường từ xưa đến nay
```sql
SELECT SinhVien.Ten, LopHoc.TenLop
FROM SinhVien
INNER JOIN LopHoc ON SinhVien.LopID = LopHoc.ID;
```

Trong khuôn khổ của dự án Data Literacy, chúng tôi chỉ giới thiệu sơ lược về khái niệm để bạn biết được SQL là gì. Việc học SQL rất dễ dàng, như học công thức Excel vậy và hiện nay nhiều website online có cung cấp khóa học SQL miễn phí rất dễ đăng ký và học.

### 1.2.1. Phép JOIN
Phép JOIN trong SQL được sử dụng để kết hợp các hàng từ hai hoặc nhiều bảng dựa trên một điều kiện liên quan giữa chúng. Các loại JOIN phổ biến bao gồm:

- **INNER JOIN**: Trả về các bản ghi có giá trị tương ứng trong cả hai bảng.
- **LEFT JOIN (LEFT OUTER JOIN)**: Trả về tất cả các bản ghi từ bảng bên trái và các bản ghi khớp từ bảng bên phải.
- **RIGHT JOIN (RIGHT OUTER JOIN)**: Trả về tất cả các bản ghi từ bảng bên phải và các bản ghi khớp từ bảng bên trái.
- **FULL JOIN (FULL OUTER JOIN)**: Trả về tất cả các bản ghi khi có một sự khớp trong bảng bên trái hoặc bảng bên phải.
![image](https://github.com/user-attachments/assets/7a4b4e2c-4839-43ae-995b-66fc50f19a45)
![image](https://github.com/user-attachments/assets/5cff96fa-f0b7-433e-ab50-bf2447de31a2)

### 1.2.2. Dùng SQL với điều kiện (WHERE)
Mệnh đề WHERE trong SQL được sử dụng để lọc các bản ghi trả về bởi một truy vấn SQL, chỉ chọn các bản ghi thỏa mãn điều kiện chỉ định.

Ví Dụ: Lấy tất cả sinh viên có tuổi trên 20
```sql
SELECT * FROM SinhVien WHERE Tuoi > 20;
```
Một ví dụ khác: Lấy danh sách đơn hàng được các sinh viên trên 20 tuổi mua, bao gồm chi tiết đơn và tên sinh viên đã mua, tên sản phẩm
```sql
SELECT DonHang.MaDonHang, SinhVien.Ten, SanPham.TenSanPham
FROM DonHang
INNER JOIN SinhVien ON DonHang.SinhVienID = SinhVien.ID
INNER JOIN SanPham ON DonHang.SanPhamID = SanPham.ID
WHERE SinhVien.Tuoi > 20;
```

### 1.1.3. Dùng SQL để tổng hợp dữ liệu (Aggregation)
SQL không chỉ dùng để lấy danh sách, mà nó còn có khả năng cộng trừ nhân chia và làm các phép tính phức tạp như lấy ngược lại X dòng, lấy ngược lại dữ liệu 1 năm, tính trung bình, thậm chí một số database hiện đại còn cho phép chạy các thuật toán AI chỉ bằng SQL mà thôi.

Các phép aggregration phổ biến là SUM, AVG (tính giá trị trung bình), COUNT (đếm dòng), COUNT DISTINCT (đếm dòng duy nhất).

Ví dụ: Tính số tiền mà các bạn sinh viên trên 20 tuổi đã mua trong cửa hàng của trường:
```sql
SELECT SUM(DonHang.SoTien)
FROM DonHang
INNER JOIN SinhVien ON DonHang.SinhVienID = SinhVien.ID
INNER JOIN SanPham ON DonHang.SanPhamID = SanPham.ID
WHERE SinhVien.Tuoi > 20;
```

Ví dụ 2: Tính số tiền mà các bạn sinh viên trên 20 tuổi đã mua trong cửa hàng của trường:, lần này chia theo từng sản phẩm
```sql
SELECT SanPham.TenSanPham, SUM(DonHang.SoTien)
FROM DonHang
INNER JOIN SinhVien ON DonHang.SinhVienID = SinhVien.ID
INNER JOIN SanPham ON DonHang.SanPhamID = SanPham.ID
WHERE SinhVien.Tuoi > 20
GROUP BY SanPham.TenSanPham;
```

## 1.3. Kết Luận
Hiểu biết cơ bản về cơ sở dữ liệu, bảng, quan hệ và SQL là rất cần thiết cho việc làm việc với các hệ thống quản lý dữ liệu. SQL cung cấp một bộ công cụ mạnh mẽ để truy cập và thao tác dữ liệu trong các cơ sở dữ liệu quan hệ.

Ngoài ra, SQL còn là một kỹ năng mà ngày càng nhiều công ty yêu cầu bạn có, không chỉ khi bạn đi làm việc về data mà kể cả khi bạn làm các việc vận hành, quảng cáo, marketing, truyền thông... SQL cũng chỉ là công cụ, giống như Excel có các hàm tính toán và công thức, thì các database / data warehouse sẽ dùng SQL để lấy số, tính toán số.

Cũng may là SQL tương đối "universal", nên bạn chỉ cần học 1 lần cho 1 database, các hệ thống khác sẽ gần giống nên bạn không cần phải học lại.

# 2. Data warehouse và tổng hợp dữ liệu
Dữ liệu của các doanh nghiệp hiện nay thường nằm ở nhiều hệ thống, nhiều dịch vụ khác nhau, lý do là không bao giờ có 1 hệ thống có thể thỏa mãn mọi yêu cầu của mọi doanh nghiệp. Nhất là trong thời buổi này mọi thứ đều số hóa hoặc đều lên online, và không tổ chức nào dễ dàng chia sẻ dữ liệu với nhau, nên việc dữ liệu rời rạc là chuyện hoàn toàn dễ hiểu.

## 2.1. Sự rời rạc của dữ liệu trong doanh nghiệp
Trong thuật ngữ của lĩnh vực data có một từ gọi là "**data silo**", hay còn gọi là sự rời rạc của dữ liệu. Nó phản ánh đúng việc rời rạc, tách rời của các hệ thống hiện đại ngày nay. Ngay cả các tổ chức rất lớn, với hệ thống ERP quản lý được rất nhiều phòng ban và chức năng, nhưng vẫn sẽ gặp tình trạng data silo, vì đơn giản là ERP cũng không thể bao gồm hết mọi việc vận hành của một doanh nghiệp hiện đại, mà có thể bạn sẽ có thêm dữ liệu từ các nền tảng quảng cáo, dữ liệu từ bên thứ 3 cung cấp, dữ liệu offline, dữ liệu từ đối tác. **Đây là lý do về mặt technical, kỹ thuật.**

Nhưng data silo được hình thành không chỉ từ sự tách rời của hệ thống, **mà có thể còn do bản thân cấu trúc doanh nghiệp, hoặc văn hóa doanh nghiệp, cũng có sự tách rời**. Sẽ không hiếm các công ty giao cho mỗi phòng ban một ngân sách riêng và họ có thể tự chọn các cách giải quyết vấn đề riêng, không liên thông giữa các phòng ban. Mỗi team tự phát triển một cách làm việc, phân tích dữ liệu riêng nhau, và không sẵn sàng chia sẻ dữ liệu hay thông tin cho nhau. Các "silo" này cũng được hình thành quanh các phòng ban.

## 2.2. Data silo có thể khiến các vấn đề sau xảy ra
- Dữ liệu bị trùng lặp giữa các hệ thống, không biết đâu là dữ liệu đúng nhất
- Dữ liệu không nhất quán giữa các hệ thống, ví dụ cùng là sản phẩm Áo thun Babycute màu đỏ size M nhưng ở hệ thống bán hàng thì đang lưu tên "Áo thun Babycute đỏ M", trong khi hệ thống quản lý kho thì lại lưu "Áo thu BBCUT màu đỏ size M" nên nếu chỉ dùng tên để thống nhất thì dễ sai. Thường thì người ta sẽ dùng thêm mã vạch hoặc mã SKU để thống nhất
- Khi cần sử dụng dữ liệu, không thể gom chung lại một nơi để phân tích, đánh giá
- Mỗi phòng ban hiểu dữ liệu một cách khác nhau, không thống nhất về định nghĩa và cách tính toán
- Khi cần truy cập dữ liệu thuộc phòng ban khác rất khó khăn, tuy đã có thẩm quyền để truy xuất
- Dữ liệu không đồng nhất về định dạng, khiến việc tính toán liên phòng ban, liên hệ thống trở nên khó khăn
- Nếu dữ liệu liên quan tới khách hàng, có thể sẽ không tuân thủ đúng các quy định về Bảo mật dữ liệu cá nhân nhạy cảm
- Việc phối hợp, cộng tác làm việc giữa các team trở nên khó khăn, kéo dài và có thể gây bực mình cho nhân viên

Để giải quyết tình trạng này, các doanh nghiệp có nhiều cách, nhưng đây sẽ là những cách phổ biến và có thể áp dụng không chỉ 1 mà nhiều cách cùng lúc:
- Tích hợp hệ thống (system integration): các doanh nghiệp sẽ thông qua các đường như API mà mỗi hệ thống mở ra để đưa dữ liệu từ hệ thống này sang hệ thống khác. Trên thị trường có các công ty và các dịch vụ chuyên làm việc này. Ngoài ra người ta cũng có thể tích hợp ở tầng database (cơ sở dữ liệu) nếu hệ thống cho phép.
- Xây dựng hệ thống master data: Tạo ra một chỗ quản lý dữ liệu gốc, chung với nhau, gọi là "source of truth", là dữ liệu đúng nhất và gốc nhất. Từ source of truth, dữ liệu sẽ được đồng bộ hoặc nhập thủ công vào các hệ thống khác nhau. Các đối tượng master data thường thấy sẽ là Sản phẩm, Cửa hàng, Nhân viên...
- Xây dựng văn hóa chia sẻ dữ liệu ở mức cần thiết: trong nhiều trường hợp, mọi thứ có thể chỉ cần giải quyết ở mặt con người và giao tiếp, vì thực ra data silo xuất hiện do các phòng ban không hiểu nhau chứ về mặt hệ thống thì có thể giải quyết dễ dàng.

Đây chỉ là 3 ví dụ cơ bản, ngoài ra còn nhiều cách khác nữa nhé.

## 2.3. Data warehouse và cách nó giải quyết vấn đề của data silo
Data warehouse là một loại cơ sở dữ liệu (database) nhưng được tối ưu cho việc xử lý, phân tích, tổng hợp dữ liệu. Nó là một loại database đặc thù, và người ta hay gọi nó là OLAP database (Online Analytics Processing).

Ở tầng kiến trúc, một database chuyên dùng cho vận hành (OLTP) như Postgres, MySQL, SQL Server có thể sẽ gặp vấn đề khi xử lý dữ liệu rất lớn, nhưng với data warehouse thì vài tỉ dòng không phải là chuyện to tát. Thậm chí tốc độ thu thập dữ liệu 1 tỉ dòng / ngày cũng là một lượng dữ liệu mà data warehouse xem là "không quá lớn".

Một vài giải pháp data warehouse nổi tiếng hiện nay trên thị trường có thể kể đến như:

- Bộ ba cloud lớn: Google BigQuery, Amazon Redshift, Microsoft Azure Synapse
- Các hệ thống cho doanh nghiệp: Oracle Autonomous Data Warehouse, SAP BW4/HANA, IBM Db2 Warehouse

Ngoài ra, một số doanh nghiệp có thể dùng chính các hệ thống OLTP để làm data warehouse. Ở quy mô nhỏ, việc này hợp lý, nhưng khi lượng dữ liệu lớn, việc scale hệ thống sẽ phức tạp hơn, và đôi khi đắt tiền hơn xài cloud.

## 2.4. Data warehouse có lợi ích gì cho việc giải quyết sự rời rạc của dữ liệu?
Về mặt kỹ thuật, data warehouse là một giải pháp để giải quyết vấn đề tách rời dữ liệu của doanh nghiệp. **Data warehouse (kho dữ liệu) sẽ chứa mọi dữ liệu của công ty vào một nơi duy nhất**, từ đó tháo bỏ rào cản của data và loại bỏ sự "silo" của dữ liệu.

Vì mọi thứ đã nằm chung một nơi, việc truy xuất, sử dụng, thậm chí ghép dữ liệu từ nhiều nguồn khác nhau lại trở nên dễ dàng. Tất nhiên, data warehouse cũng có đầy đủ khả năng phân quyền để đảm bảo mỗi người dùng được phép truy cập đúng và đủ dữ liệu cần thiết cho công việc của mình.

**Một ví dụ cụ thể**: khi dữ liệu về quảng cáo Google Ads, Facebook Ads, TikTok Ads đã được gom về data warehouse của doanh nghiệp, bạn có thể cộng chi phí chạy ads mỗi ngày của từng nền tảng để ra số tổng một cách tự động, hoặc bạn cộng số lượt conversion để biết tổng số tiền mình chi ra có hiệu quả hay không, kênh Facebook hay Google hay TikTok hiệu quả hơn, từ đó ra quyết định tiếp theo cho việc chạy quảng cáo.

**Một ví dụ khác về vận hành**: Một doanh nghiệp bán lẻ có hệ thống ERP, hệ thống bán hàng và hệ thống ecommerce riêng nhau. Để có được bức tranh toàn cảnh về tất cả mọi nghiệp vụ bán hàng, dữ liệu sẽ được tổng hợp hết về data warehouse để dựng thành các dashboard doanh thu, chi phí, chia theo từng kênh. Thông tin khách hàng cũng được gom chung về data warehouse để không bị thất lạc.

Ngày xưa, data warehouse chủ yếu dùng cho mục đích phân tích, báo cáo và xây dựng dashboard. Ngày nay, data warehouse không chỉ dừng ở đó, nó còn là một nguồn dữ liệu để tiếp tục đưa vào các hệ thống vận hành sau khi dữ liệu đã tổng hợp xong, hoặc tích hợp với hệ thống bên thứ 3 để phục vụ cho một số mục đích kinh doanh cụ thể.

Để đưa dữ liệu từ các hệ thống vào data warehouse, người ta thường dùng các quy trình gọi là ETL hoặc ELT, đây cũng là một phương pháp tích hợp hệ thống (tích hợp dữ liệu từ các nguồn bên ngoài vào trong data warehouse). ETL và ELT sẽ được chia sẻ với các bạn trong một bài viết riêng.

# 3. Doanh nghiệp tận dụng data để tối ưu hóa việc kinh doanh như thế nào?
## Phần 1: Doanh nghiệp tận dụng data để tối ưu hóa việc kinh doanh như thế nào?
Khi nhắc đến việc phân tích dữ liệu để phục vụ cho việc kinh doanh, nhiều người cho rằng việc này chỉ phù hợp với những công ty lớn với hệ thống cơ sở dữ liệu hoàn chỉnh và nguồn nhân lực dồi dào. Tuy nhiên trong thực tế, ngay cả những công ty vừa và nhỏ hay các công ty start-up đều có thể tận dụng dữ liệu của mình để tối ưu hóa hoạt động kinh doanh, đưa ra quyết định sáng suốt và gia tăng lợi thế cạnh tranh của doanh nghiệp mình, miễn data đó hợp lý, đủ nhiều và đủ chính xác.

### Cách doanh nghiệp dùng data
Data trong doanh nghiệp có thể được vận dụng để giải quyết 2 bài toán chính:

- Tối ưu hóa quy trình kinh doanh (ví dụ: giảm thiểu thời gian sản xuất hàng, giảm tỉ lệ hàng lỗi, tăng năng suất cuộc gọi của nhân viên telesale...)
- Tối ưu hóa hiệu quả kinh doanh (ví dụ: tăng doanh thu, giảm chi phí, mở rộng chi nhánh, mở rộng tệp khách hàng...)

Để giải quyết những bài toán kinh doanh đó, doanh nghiệp sẽ sử dụng data như một "bằng chứng" để chứng minh là hướng giải quyết hoặc kết luận của mình là chính xác. Ví dụ:

**Tôi thấy mình cần tập trung cho kênh livestream hơn trong 6 tháng tiếp theo để mở rộng doanh thu**. Lí do là vì:

- Kênh livestream là kênh có tốc độ tăng trưởng doanh thu và số lượng khách hàng mới cao nhất trong công ty trong 3 tháng vừa qua, trong khi các kênh khác không tăng trưởng bằng --> Data này lấy từ nội bộ doanh nghiệp
- Tiềm năng của kênh livestream vẫn còn rộng mở, bằng chứng là các sàn TMĐT cho biết họ sẽ tiếp tục đầu tư cho kênh livestream trong thời gian sắp tới --> Data này lấy từ nguồn thứ cấp
- Công ty của chúng ta đã có tương đối đầy đủ nguồn lực cho kênh livestream, và có đủ kinh phí để mở rộng thêm ít nhất là 1.5 lần trong 6 tháng tiếp theo --> Data này lấy từ nội bộ doanh nghiệp, và ước lượng chủ quan của người phân tích

Việc sử dụng data để giải quyết các bài toán kinh doanh trong hầu hết trường hợp sẽ giúp bạn đưa ra được quyết định tối ưu, chắc chắn, đáng tin cậy và thuyết phục hơn.

Dù công ty lớn hay nhỏ, thì việc sử dụng data trong doanh nghiệp có thể được mô phỏng như sơ đồ dưới đây:



### Case study
Ví dụ thực tế: Giả sử bạn đang làm cho công ty TikTok, KPI của bạn là số lượng TikToker đăng nội dung video hàng ngày. Một ngày nọ, sếp của bạn hỏi rằng: **Em ơi, hình như số lượng TikToker đăng video trong tuần này bị giảm 30% so với tuần trước. Lí do là vì sao và bây giờ em đề xuất nên làm gì?**

Là một người phân tích dữ liệu, quy trình vận dụng data để phân tích và đưa ra đường hướng chiến lược để tăng số lượng TikToker tạo video trở lại của bạn có thể trông như sau:



Tùy thuộc vào quy mô, mô hình kinh doanh và nhu cầu phân tích mà mỗi doanh nghiệp sẽ có cách vận dụng data khác nhau. Tuy nhiên như các bạn đã thấy thì quy trình phân tích thì sẽ đều là: xác định vấn đề --> lập framework và xác định những câu hỏi cần trả lời --> tìm kiếm data --> xử lí data, phân tích & đưa ra giải pháp --> trình bày phân tích. Việc thấu hiểu quy trình này và sở hữu những bộ kĩ năng để thực hiện từng bước trong quy trình sẽ giúp các bạn vận dụng data tốt hơn để giúp doanh nghiệp cải thiện việc kinh doanh. Trong bài viết sau, chúng ta sẽ đi qua một vài lưu ý trong quy trình này để việc phân tích được hiệu quả hơn, đồng thời giảm thiểu những lỗi sai không đáng có.

## Phần 2: Một vài lưu ý khi dùng data để tối ưu hóa việc kinh doanh
Như ở bài trước, chúng ta đã biết là để đảm bảo việc phân tích dữ liệu & đưa ra kết luận được hiệu quả và chính xác, chúng ta sẽ cần phải đảm bảo 3 tiêu chí chính:

- Data đủ lớn, sạch & chính xác
- Sử dụng công cụ & phương pháp phân tích phù hợp
- Đảm bảo tính logic & thực tế của phân tích

Trong bài viết này chúng ta sẽ đi sâu hơn về 3 tiêu chí này, tuy nhiên sẽ không đi quá sâu về phần kĩ thuật



### Chất lượng data
Nói một cách đơn giản thì không ai muốn đưa ra kết luận không chính xác chỉ vì data bị sai hoặc không mang tính đại diện. Đó là lí do mà trước khi làm bất kì bài toán phân tích nào, điều đầu tiên chúng ta phải làm đó là kiểm tra chất lượng của data và làm sạch nó.

**Chất lượng của data:**
- Data phải chính xác: Một vài data có thể bị sai về mặt bản chất do quá trình nhập liệu hoặc thu thập data. Ví dụ: dữ liệu doanh thu của chuỗi cà phê nhưng lại chưa thu thập hết tất cả các chi nhánh trên địa bàn; dữ liệu đơn vị là đô la nhưng lại hiểu nhầm thành đồng Việt Nam, dữ liệu số bị sai format,... Data đã sai về mặt bản chất thì không thể sử dụng được, hoặc tính đại diện sẽ không cao
- Data phải đủ lớn: data càng ít mẫu thì tính đại diện càng không cao. Ví dụ như trên thị trường có 3 người thích sản phẩm của doanh nghiệp, 7 người không thích. Tuy nhiên khi đi khảo sát thì công ty chỉ khảo sát có 2 người, và 2 người này rơi đúng vào trường hợp không thích sản phẩm. Kết luận đưa ra là 2/2 (100%) người tham gia khảo sát không thích sản phẩm của công ty, điều này là hoàn toàn sai lầm. Lí do là vì số lượng mẫu khi khảo sát chưa đủ lớn, nên không đại diện được cho toàn thể. Tùy thuộc vào bài toán đang phân tích mà người phân tích cần ước lượng số mẫu cho phù hợp, hoặc phân tích với độ sâu dữ liệu cho phù hợp để đảm bảo kết luận mang tính đại diện.

**Data phải sạch:**
- Data không chứa dữ liệu ngoại lai: Dữ liệu ngoại lai là các dữ liệu không có cùng xu hướng với toàn thể mẫu dữ liệu. Ví dụ dữ liệu học sinh tiểu học, có một số em có chiều cao lớn hơn 1m8, hoặc nhỏ hơn 1m, thì được xem là dữ liệu ngoại lai


- Data không chứa data lỗi: Data lỗi ở đây có thể là sai định dạng (dữ liệu chiều cao theo cm, nhưng tự nhiên lại có 1 dòng là "một mét ba" --> không cùng kiểu dữ liệu), bị thiếu dữ liệu (dữ liệu rỗng), hoặc dữ liệu bị sai do định dạng, do lỗi nhập liệu v.v. Những dữ liệu này cũng cần được loại ra để không ảnh hưởng đến quá trình phân tích

Một ví dụ về data chưa được làm sạch:
- Cột Class, Ticket: loại dữ liệu lộn xộn, không rõ nghĩa
- Cột Gender: định nghĩa nam, nữ không đồng nhất
- Cột Age: có dữ liệu lỗi & dữ liệu không chính xác
- Cột cost: có dữ liệu rỗng & dữ liệu ngoại lai


Kĩ thuật kiểm tra tính đại diện & làm sạch data trước khi sử dụng: có nhiều phương pháp từ thủ công (filter data trên excel và sửa bằng tay) đến tự động (sử dụng hàm & công cụ làm sạch). Hẹn các bạn trong 1 bài viết khác để tránh bài này đỡ dài.

### Công cụ phân tích & phương pháp phân tích dữ liệu
Chủ đề này rất dài và tốn giấy mực, vì tùy thuộc vào bài toán, câu hỏi phân tích, loại hình kinh doanh... mà chúng ta sẽ có những công cụ, phương pháp phân tích & đưa ra kết luận khác nhau.

Một vài công cụ phân tích thường dùng trong các doanh nghiệp
- Doanh nghiệp nhỏ với nhu cầu phân tích đơn giản: Excel hoặc Google Sheets là lựa chọn phù hợp nhờ tính dễ sử dụng và miễn phí. Tuy nhiên nên biết thêm Power Query cơ bản để dễ tổng hợp & làm sạch dữ liệu khi cần.
- Doanh nghiệp cần cộng tác và chia sẻ dữ liệu dễ dàng: Google Sheets là lựa chọn tốt do nhiều người có thể làm việc trên 1 file cùng 1 lúc.
- Doanh nghiệp cần phân tích dữ liệu chuyên sâu và trực quan hóa dữ liệu: Power BI là lựa chọn phù hợp do có nhiều tính năng tổng hợp dữ liệu, làm sạch dữ liệu, trực quan hóa và báo cáo. Tuy nhiên cần cân nhắc chi phí.
- Doanh nghiệp cần xử lý dữ liệu lớn và có khả năng lập trình: Python là lựa chọn mạnh mẽ, nhưng đòi hỏi đầu tư thời gian học tập. Ngoài ra với các doanh nghiệp này thì nhân viên cần biết thêm SQL để kéo được dữ liệu mong muốn từ database. Về công cụ trực quan hóa thì Power Bi, Taleau hay công cụ nào phù hợp với chi phí và nhu cầu cũng được.

Ngoài ra, các doanh nghiệp SME cũng có thể cân nhắc các giải pháp phân tích dữ liệu do các công ty Việt Nam phát triển. Nhiều giải pháp này có chi phí hợp lý, giao diện tiếng Việt và hỗ trợ kỹ thuật tốt, phù hợp với nhu cầu của các doanh nghiệp này.

##### Một vài phương pháp phân tích thường được sử dụng
**1. Phân tích mô tả (Descriptive Analytics):**
Tóm tắt và mô tả dữ liệu, giúp doanh nghiệp hiểu rõ hơn về đặc điểm, xu hướng và phân bố của dữ liệu.
Ví dụ:
- Phân tích mô tả dữ liệu bán hàng theo sản phẩm, khu vực, thời gian để xác định sản phẩm bán chạy, khu vực tiềm năng và xu hướng mua sắm theo mùa.
- Phân tích mô tả dữ liệu lỗi sản phẩm theo dây chuyền sản xuất, nguyên nhân lỗi và thời điểm xảy ra lỗi để cải thiện chất lượng sản phẩm.

**2. Phân tích chẩn đoán (Diagnostic Analytics):**
Xác định nguyên nhân gốc rễ của các vấn đề kinh doanh dựa trên dữ liệu.
Ví dụ:
- Phân tích chẩn đoán dữ liệu đánh giá khách hàng để xác định nguyên nhân khiến khách hàng không hài lòng và đưa ra giải pháp cải thiện dịch vụ.
- Phân tích chẩn đoán dữ liệu giỏ hàng bị bỏ lại để xác định lý do khách hàng không hoàn tất thanh toán và tối ưu hóa trải nghiệm mua sắm.

**3. Phân tích dự đoán (Predictive Analytics):**
Dự đoán các xu hướng và sự kiện tương lai dựa trên dữ liệu lịch sử.
Ví dụ:
- Phân tích dự đoán dữ liệu bán hàng để dự báo nhu cầu cho từng sản phẩm, giúp tối ưu hóa việc quản lý kho hàng.
- Phân tích dự đoán dữ liệu thị trường chứng khoán để dự đoán giá cổ phiếu và đưa ra quyết định đầu tư hiệu quả.

**4. Phân tích đề xuất (Prescriptive Analytics):**
Đề xuất các giải pháp tối ưu cho các vấn đề kinh doanh dựa trên dữ liệu.
Ví dụ:
- Phân tích đề xuất dữ liệu giao hàng để tối ưu hóa lộ trình giao hàng, giảm thiểu thời gian và chi phí giao hàng.
- Phân tích đề xuất dữ liệu giá vé máy bay để tối ưu hóa giá vé cho từng đường bay, thu nhập tối đa cho doanh nghiệp

Đây là 4 phương pháp phân tích dữ liệu thường được sử dụng nhiều nhất. Hẹn các bạn một bài viết khác, chúng ta sẽ bàn luận sâu hơn về cách sử dụng 4 phương pháp này trong thực tế, và các kiến thức các bạn cần trang bị để thực hiện tốt 4 phương pháp này.

## Phần 3: Dùng công cụ gì cho việc phân tích dữ liệu?
Việc lựa chọn công cụ phù hợp để phân tích dữ liệu là một quyết định quan trọng ảnh hưởng trực tiếp đến hiệu quả hoạt động và khả năng cạnh tranh của doanh nghiệp. Bài viết này sẽ cung cấp cho bạn thông tin về một số công cụ phân tích dữ liệu phổ biến, cùng với ưu, nhược điểm và chi phí của từng công cụ, để hỗ trợ bạn đưa ra lựa chọn phù hợp nhất cho doanh nghiệp SME của mình. Các bạn yêu thích phân tích dữ liệu nói chung, dù đang làm trong công ty SME hay các công ty lớn, thì cũng đều có thể xem qua bài viết này để có định hướng rõ ràng hơn về các công cụ phân tích bạn nên học.

**1. Excel:**
Excel thì hầu như ai cũng biết rồi do tính phổ biến rất cao của nó. Ngoài các hàm hỗ trợ xử lí và tính toán dữ liệu như sum, count, vlookup,... thì Excel cũng cung cấp thêm 2 tính năng rất mạnh cho phân tích dữ liệu đó là Pivot Table và Power Query.
Có một lưu ý nhỏ là nếu các bạn dùng Excel nhiều để phân tích thì nên mua máy có hệ điều hành Windows. Excel trên Mac không được thân thiện lắm, và cũng thiếu đi Power Query.
**Ưu điểm:**
- **Miễn phí hoặc chi phí thấp**: Excel có sẵn trên hầu hết các máy tính và thường đi kèm với bộ cài đặt Microsoft Office.
- **Dễ sử dụng**: Giao diện quen thuộc và thao tác đơn giản giúp người dùng dễ dàng học hỏi và sử dụng. Hầu như tin học văn phòng ai cũng phải học qua Excel nên nếu phải học thêm thì học cũng nhanh và không sợ thiếu tài liệu tiếng Việt.
- **Tính năng đa dạng**: Excel cung cấp nhiều chức năng tính toán, phân tích dữ liệu và khả năng trực quan hóa dữ liệu cơ bản.
- **Phù hợp cho các doanh nghiệp nhỏ**: Với nhu cầu phân tích dữ liệu đơn giản, Excel có thể đáp ứng đầy đủ nhu cầu của nhiều doanh nghiệp SME.
**Nhược điểm:**
- **Hạn chế về khả năng xử lý dữ liệu lớn**: Excel gặp khó khăn khi xử lý lượng dữ liệu lớn, dẫn đến hiệu suất chậm và khả năng phân tích bị hạn chế. Nếu data của mọi người trên 100k dòng và có quá nhiều cột thì nên cân nhắc sử dụng công cụ khác như Power BI (đọc thêm về Power BI ở phía dưới).
- **Khó khăn trong việc cộng tác**: Việc chia sẻ và cập nhật dữ liệu trong Excel giữa nhiều người dùng có thể gặp nhiều trở ngại. Thông thường muốn chia sẻ file thì phải lưu file lại gửi cho người khác, nên mỗi lần có chỉnh sửa gì thì lại phải cập nhật file mới. Nhìn chung là tính cộng tác không cao bằng Google Sheets.
- **Thiếu tính năng phân tích nâng cao**: Excel không cung cấp các tính năng phân tích dữ liệu chuyên sâu như mô hình học máy hay phân tích dự đoán.
**Chi phí**: Miễn phí (bản dùng thử) hoặc chi phí thấp khi mua bản quyền Microsoft Office.

**2. Google Sheets:**
Google Sheets là một sản phẩm của Google, có tính năng gần tương tự như Excel, nên cũng có thể sử dụng tốt cho việc xử lí và phân tích dữ liệu. Tuy nhiên Google Sheets cũng sẽ có một vài ưu điểm và nhược điểm cần phải cân nhắc.
**Ưu điểm:**
- **Miễn phí**: Google Sheets là công cụ trực tuyến hoàn toàn miễn phí, giúp tiết kiệm chi phí cho doanh nghiệp.
- **Dễ sử dụng**: Giao diện trực quan và thao tác đơn giản tương tự Excel, giúp người dùng dễ dàng học hỏi và sử dụng. Hầu hết các hàm trên Excel đều sử dụng được trên Google, với cú pháp gần như là giống nhau.
- **Tính năng cộng tác**: Google Sheets cho phép nhiều người dùng cùng chỉnh sửa dữ liệu trong thời gian thực, thúc đẩy cộng tác hiệu quả.
- **Khả năng truy cập từ mọi nơi**: Doanh nghiệp có thể truy cập và sử dụng Google Sheets từ mọi thiết bị có kết nối internet.
**Nhược điểm:**
- **Hạn chế về tính năng**: So với Excel, Google Sheets có ít chức năng phân tích dữ liệu và khả năng trực quan hóa dữ liệu hạn chế hơn.
- **Khả năng xử lý dữ liệu lớn**: Google Sheets có thể gặp khó khăn khi xử lý lượng dữ liệu lớn, hoặc nếu file có quá nhiều người cộng tác cùng một lúc, dẫn đến hiệu suất chậm.
- **Yêu cầu kết nối internet**: Doanh nghiệp cần có kết nối internet để sử dụng Google Sheets, tuy nhiên trong thời đại này thì đây cũng không phải là một trở ngại lớn.
**Chi phí**: Miễn phí.

**3. Power BI:**
Sản phẩm của Microsoft nên có giao diện dễ sử dụng, mang phong cách của Microsoft Office. Công cụ này cũng có tương thích tốt với Excel. Tuy nhiên Power BI không sử dụng được trên Macbook, các bạn muốn sử dụng trên Macbook sẽ cần tải phần mềm giả lập Windows.
Các bạn muốn học 1 công cụ trực quan hóa dữ liệu thì có thể bắt đầu với Power BI vì tính dễ sử dụng, và miễn phí (bản dùng thử) của nó.
**Ưu điểm:**
- Khả năng kết nối dữ liệu đa dạng: Power BI có thể kết nối với nhiều nguồn dữ liệu khác nhau như Excel, SQL Server, Google Analytics, v.v. Do đó nếu dữ liệu của bạn ở nhiều nguồn hoặc nhiều file khác nhau, lượng dữ liệu tương đối lớn thì có thể cân nhắc sử dụng Power BI
- **Tính năng trực quan hóa dữ liệu mạnh mẽ**: Power BI cung cấp nhiều biểu đồ, đồ thị và khả năng trực quan hóa dữ liệu chuyên nghiệp.
- **Tính năng phân tích dữ liệu nâng cao**: Power BI hỗ trợ nhiều tính năng phân tích dữ liệu như phân tích xu hướng, phân tích nhóm, phân tích dự đoán.
- **Dễ dàng chia sẻ báo cáo**: Power BI cho phép tạo và chia sẻ báo cáo phân tích dữ liệu trực quan một cách dễ dàng.
**Nhược điểm**:
- **Chi phí**: Power BI có phiên bản miễn phí với tính năng hạn chế (ví dụ như không chia sẻ báo cáo trực tuyến cho nhiều người được), phiên bản Pro và Premium có chi phí cao hơn.
- **Đường cong học tập**: Power BI có nhiều tính năng nâng cao, đòi hỏi người dùng cần đầu tư thời gian học tập để sử dụng. Nếu muốn sử dụng Power BI hiệu quả thì sẽ cần phải học thêm code DAX để viết các hàm chuyên sâu (tuy nhiên cũng không quá khó, vì nó có điểm giống với hàm Excel).
**Chi phí**: Miễn phí (bản dùng thử); Phiên bản Pro: $9.99/người dùng/tháng; Phiên bản Premium: $49.99/người dùng/tháng (chi phí tham khảo, có thể thay đổi tùy theo quốc gia và thời điểm).

**4. Tableau:**
Một đối thủ cạnh tranh với Power BI đó là Tableau, cũng cung cấp các giải pháp phân tích và trực quan hóa dữ liệu mạnh mẽ.
**Ưu điểm:** Nhìn chung thì hầu hết ưu điểm của Power BI cũng là ưu điểm của Tableau.
- Giao diện kéo thả trực quan: Tableau cung cấp giao diện kéo thả trực quan, giúp người dùng dễ dàng tạo các biểu đồ, đồ thị và báo cáo phân tích dữ liệu.
- Khả năng phân tích dữ liệu đa chiều: Tableau hỗ trợ phân tích dữ liệu theo nhiều góc nhìn khác nhau, giúp doanh nghiệp khai thác sâu hơn về insights (phân tích chuyên sâu) từ dữ liệu.
- Tính năng chia sẻ báo cáo: Tableau cho phép tạo và chia sẻ báo cáo phân tích dữ liệu một cách chuyên nghiệp và dễ dàng.
**Nhược điểm:**  Tableau có chi phí bản quyền cao, có thể là gánh nặng cho các doanh nghiệp SME.
- Phiên bản Creator: $70/người dùng/tháng;
- Phiên bản Explorer: $35/người dùng/tháng (chi phí tham khảo, có thể thay đổi tùy theo quốc gia và thời điểm).

**5. Python:**
Sau khi đã học xong các công cụ phân tích dữ liệu phía trên, nếu các bạn có nhu cầu phân tích dữ liệu chuyên sâu, phân tích dữ liệu lớn, hoặc tự động hóa công việc thì có thể cân nhắc sử dụng thêm Python.
**Ưu điểm**:
- **Miễn phí**: Python là ngôn ngữ lập trình mã nguồn mở hoàn toàn miễn phí.
- **Cộng đồng lớn**: Python có cộng đồng người dùng và nhà phát triển lớn, cung cấp nhiều tài nguyên hỗ trợ và thư viện phân tích dữ liệu phong phú.
- **Khả năng xử lý dữ liệu lớn**: Python có khả năng xử lý và phân tích lượng dữ liệu lớn hiệu quả nhờ các thư viện chuyên dụng như Pandas và NumPy. Python cũng thường được sử dụng cho các bài toán về dữ liệu chuyên sâu như Machine Learning hay AI.
- **Tính linh hoạt cao**: Python cho phép tùy chỉnh và xây dựng các giải pháp phân tích dữ liệu theo nhu cầu cụ thể của doanh nghiệp.
Nhược điểm:
- **Đường cong học tập dốc**: Python đòi hỏi người dùng có kiến thức lập trình nhất định, dẫn đến thời gian học tập lâu hơn so với các công cụ khác.
- **Yêu cầu kỹ thuật**: Doanh nghiệp có thể cần thuê chuyên gia phân tích dữ liệu có kỹ năng lập trình Python để tận dụng tối đa sức mạnh của công cụ này.
**Chi phí**: Miễn phí.

## Lời kết
Tùy thuộc vào quy mô và nhu cầu của doanh nghiệp mà bạn có thể cân nhắc sử dụng các công cụ phân tích dữ liệu khác nhau. Doanh nghiệp SME nên đánh giá nhu cầu phân tích dữ liệu thực tế của mình, nguồn lực sẵn có (nhân sự, ngân sách) và khả năng công nghệ trước khi lựa chọn công cụ phù hợp. Nên cân nhắc bắt đầu với các công cụ miễn phí như Excel, Google Sheets hoặc Power BI phiên bản miễn phí để làm quen với phân tích dữ liệu. Sau đó, khi nhu cầu gia tăng, doanh nghiệp có thể nâng cấp lên các công cụ trả phí mạnh mẽ hơn như Python hoặc Tableau.

- **Doanh nghiệp nhỏ với nhu cầu phân tích đơn giản**: Excel hoặc Google Sheets là lựa chọn phù hợp nhờ tính dễ sử dụng và miễn phí. Tuy nhiên nên biết thêm Power Query cơ bản để dễ tổng hợp & làm sạch dữ liệu khi cần.
- **Doanh nghiệp cần cộng tác và chia sẻ dữ liệu dễ dàng**: Google Sheets là lựa chọn tốt do nhiều người có thể làm việc trên 1 file cùng 1 lúc.
- **Doanh nghiệp cần phân tích dữ liệu chuyên sâu và trực quan hóa dữ liệu**: Power BI là lựa chọn phù hợp do có nhiều tính năng tổng hợp dữ liệu, làm sạch dữ liệu, trực quan hóa và báo cáo. Tuy nhiên cần cân nhắc chi phí.
- **Doanh nghiệp cần xử lý dữ liệu lớn và có khả năng lập trình**: Python là lựa chọn mạnh mẽ, nhưng đòi hỏi đầu tư thời gian học tập. Ngoài ra với các doanh nghiệp này thì nhân viên cần biết thêm SQL để kéo được dữ liệu mong muốn từ database. Về công cụ trực quan hóa thì Power Bi, Taleau hay công cụ nào phù hợp với chi phí và nhu cầu cũng được.

Ngoài ra, các doanh nghiệp SME cũng có thể cân nhắc các giải pháp phân tích dữ liệu do các công ty Việt Nam phát triển. Nhiều giải pháp này có chi phí hợp lý, giao diện tiếng Việt và hỗ trợ kỹ thuật tốt, phù hợp với nhu cầu của các doanh nghiệp này.Ngoài ra nếu bạn là nhân viên các công ty lớn, có hệ thống cơ sở dữ liệu (database) hoàn chỉnh thì nên cân nhắc học thêm SQL để biết cách trích xuất dữ liệu để sử dụng cho việc phân tích.

# 4. Vì sao data lại quan trọng?
## 4.1. Tầm Quan Trọng của Dữ Liệu Trong Kinh Doanh Hiện Đại
Trong kỷ nguyên số hiện nay, dữ liệu đã trở thành một tài sản vô cùng quý giá đối với các doanh nghiệp. Tuy nhiên, tại Việt Nam, nhiều chủ doanh nghiệp, đặc biệt là chủ doanh nghiệp vừa và nhỏ, thường không để ý đến việc sử dụng dữ liệu của chính tổ chức mà mình đang quản lý. Việc này dẫn đến việc ra quyết định thiếu chính xác và hiệu quả. Các cấp quản lý và chủ doanh nghiệp cần hiểu rõ hơn về giá trị của dữ liệu để có thể đưa ra những quyết định chiến lược thông minh và hiệu quả.

## 4.2. Tại Sao Dữ Liệu Lại Quan Trọng?
- **Ra Quyết Định Chính Xác**: Sử dụng dữ liệu giúp các doanh nghiệp đưa ra quyết định dựa trên thực tế thay vì dựa trên cảm tính. Các quyết định được hỗ trợ bởi dữ liệu thường có cơ sở vững chắc và ít rủi ro hơn. Ví dụ, khi quản lý chi phí chạy quảng cáo trên Facebook và Google Ads, việc phân tích dữ liệu giúp xác định chiến dịch nào hiệu quả nhất và tối ưu hóa ngân sách quảng cáo.
- **Nắm Rõ Tình hình doanh nghiệp**: Nhiều công ty SME ở Việt Nam hoạt động ở trạng thái "blind", tức là bạn không nắm rõ mình đã kiếm được bao nhiêu tiền, đã chi bao nhiêu và sắp phải chi tiền bao nhiêu. Việc thiếu bức tranh tổng quan về tình hình kinh doanh của công ty, hay cụ thể hơn là tình hình tài chính ra vào, có thể khiến bạn bị động trong việc quản lý dòng tiền, chậm trễ đưa ra kế hoạch phản ứng.
- **Hiểu Rõ Hơn Về Khách Hàng**: Dữ liệu giúp doanh nghiệp hiểu rõ hơn về nhu cầu và mong muốn của khách hàng. Từ đó, doanh nghiệp có thể cung cấp sản phẩm và dịch vụ phù hợp, nâng cao trải nghiệm khách hàng và tăng doanh thu. Ví dụ, thông qua phản hồi của khách hàng và dữ liệu từ hệ thống quản lý khách hàng (CRM), doanh nghiệp có thể cải thiện dịch vụ chăm sóc khách hàng, bạn có thể biết khách nào mua nhiều lần, họ mua món gì, tập khách hàng quay lại sử dụng dịch vụ, sản phẩm của bạn là ai...
- **Tối Ưu Hóa Hoạt Động Kinh Doanh**: Phân tích dữ liệu giúp xác định các điểm yếu trong quy trình kinh doanh, từ đó cải thiện hiệu quả hoạt động và giảm thiểu lãng phí. Chẳng hạn, quản lý tồn kho hiệu quả thông qua dữ liệu giúp tránh tình trạng thiếu hoặc thừa hàng, giảm chi phí lưu kho và tăng khả năng đáp ứng nhu cầu của khách hàng. Hoặc bạn có thể tối ưu thời gian di chuyển của shipper từ kho đến cửa hàng để hàng đến nhanh hơn, chi phí thấp hơn.
- **Dự Báo Tương Lai**: Dữ liệu lịch sử có thể được sử dụng để dự báo xu hướng tương lai, giúp doanh nghiệp chuẩn bị tốt hơn và có chiến lược phù hợp. Trong bán hàng, việc phân tích xu hướng mua sắm của khách hàng từ các mùa trước giúp doanh nghiệp đưa ra dự báo và lập kế hoạch kinh doanh hiệu quả. Giả sử bạn không nắm dữ liệu bán hàng của năm trước, đến năm nay bạn bị động, không biết khi nào nên nhập hàng, nhập bao nhiêu, và lượng khách sẽ mua là bao nhiêu.
- **Tự Tin Trong Quyết Định**: Không có dữ liệu, việc ra quyết định kinh doanh trở nên khó khăn và mang nhiều rủi ro. Các quyết định dựa trên cảm tính hoặc phỏng đoán thường thiếu độ chính xác và không có cơ sở vững chắc. Dữ liệu cung cấp nền tảng đáng tin cậy, giúp doanh nghiệp tự tin hơn trong việc đưa ra các quyết định quan trọng.

Không phải lúc nào chúng ta cũng có thể ra quyết định dựa trên số, vì trải nghiệm, kinh nghiệm, tầm nhìn và sự nhạy bén trong kinh doanh vẫn là một yếu tố cực kì quan trọng. Nhưng nếu có thể, hãy sử dụng dữ liệu để bạn có thể ra quyết định đúng hơn.

## 4.3. Dữ liệu của bạn có thể nằm ở đâu?
Dữ liệu của bạn, kể cả khi bạn là doanh nghiệp nhỏ SME tại Việt Nam, thực ra cũng nhiều lắm đó, chỉ là bạn có thể chưa để ý tới sự tồn tại của nó mà thôi. Một vài ví dụ, nghe qua là bạn sẽ biết ngay, và có khi là bất ngờ nữa:

- **Hệ Thống Quản Lý Khách Hàng (CRM)**: Đây là nơi lưu trữ thông tin về khách hàng, bao gồm thông tin liên lạc, lịch sử mua hàng, và phản hồi từ khách hàng.
- **Hệ Thống Quản Lý Bán Hàng (POS)**: Hệ thống POS lưu trữ dữ liệu về các giao dịch bán hàng, bao gồm sản phẩm bán chạy, doanh thu theo ngày, và xu hướng mua sắm.
- **Trang Web và Ứng Dụng Di Động**: Dữ liệu từ trang web và ứng dụng di động của bạn, như lượt truy cập, thời gian truy cập, và hành vi người dùng, có thể cung cấp cái nhìn sâu sắc về cách khách hàng tương tác với doanh nghiệp.
- **Mạng Xã Hội**: Các kênh mạng xã hội như Facebook, Instagram, TikTok, và LinkedIn lưu trữ dữ liệu về sự tương tác của khách hàng, phản hồi và cảm nhận về thương hiệu của bạn.
- **Quảng Cáo Trực Tuyến**: Dữ liệu từ các nền tảng quảng cáo như Google Ads và Facebook Ads cung cấp thông tin về hiệu suất chiến dịch, chi phí quảng cáo, và tỷ lệ chuyển đổi.
- **Email Marketing**: Dữ liệu từ các chiến dịch email marketing, bao gồm tỷ lệ mở email, tỷ lệ click, và phản hồi từ khách hàng.
- **Trong các file Excel, file Google Sheets, Lark Base...** mà bạn đang dùng để vận hành công ty mỗi ngày

## 4.4. Làm Thế Nào Để Bắt Đầu Sử Dụng Dữ Liệu?
- **Thu Thập Dữ Liệu**: Bắt đầu từ việc thu thập dữ liệu từ các nguồn hiện có của doanh nghiệp như hệ thống quản lý khách hàng (CRM), hệ thống quản lý bán hàng (POS), và các kênh truyền thông xã hội.
- **Lưu Trữ và Quản Lý Dữ Liệu**: Sử dụng các công cụ và phần mềm quản lý dữ liệu để lưu trữ và quản lý dữ liệu một cách hiệu quả.
- **Phân Tích Dữ Liệu**: Sử dụng các công cụ phân tích dữ liệu để hiểu rõ hơn về thông tin và xu hướng từ dữ liệu thu thập được.
- **Ứng Dụng Dữ Liệu**: Áp dụng kết quả phân tích vào quá trình ra quyết định và chiến lược kinh doanh.

## Kết Luận
Dữ liệu không chỉ là những con số vô tri, mà là nguồn tài nguyên vô cùng quý giá giúp doanh nghiệp phát triển và thịnh vượng. Các cấp quản lý và chủ doanh nghiệp cần nhận thức rõ ràng về tầm quan trọng của dữ liệu và cách sử dụng nó một cách hiệu quả để nắm bắt cơ hội, vượt qua thách thức và đạt được thành công bền vững.

# 5. Tầm quan trọng của việc sở hữu data của chính bạn
Một tình cảnh mình thường thấy tại các công ty ở Việt Nam đó là công ty không nắm quyền kiểm soát dữ liệu của chính mình. Thật ra tình trạng này diễn ra không chỉ ở Việt Nam mà nhiều doanh nghiệp vừa và nhỏ trên toàn thế giới cũng gặp phải. Tình trạng này do đâu mà ra? Và bạn có thể làm gì để cải thiện, khắc phục nó?

## 5.1. Nguyên nhân của việc data không thuộc sở hữu của bạn
### Do giới hạn của sản phẩm, dịch vụ
Một nguyên nhân phổ biến là do việc chọn sử dụng các hệ thống không cho phép trích xuất data ra ngoài theo các quy chuẩn phổ thông (ví dụ như API, webhook, hay thậm chí là download file Excel, CSV...). Khá nhiều hệ thống, nhất là các sản phẩm Việt Nam, không hỗ trợ các tính năng này nên sẽ gây khó khăn cho doanh nghiệp nếu cần tích hợp, trích xuất dữ liệu để sử dụng.

- Bạn không thể lấy được dữ liệu của chính mình
- Hoặc việc tải dữ liệu thủ công tốn nhiều thời gian, công sức của nhân viên
- Khi cần dữ liệu gì, đều phải trao đổi với bên cung cấp phần mềm để họ xuất thủ công, tốn thời gian

Ví dụ, một hệ thống chat dùng cho mục đích chăm sách khách hàng nhưng lại không có API để trích xuất dữ liệu người dùng, không thể lấy lịch sử chat.. nên khi doanh nghiệp cần lấy các data này để phân tích sâu hơn, hoặc dùng cho các hệ thống khác thì lại không được.

Tin mừng là hiện tại các sản phẩm Việt ngày càng hỗ trợ API nhiều hơn, chuẩn hóa hơn và theo đúng quy chuẩn phổ thông trên thế giới, nên tình trạng này đang ngày càng giảm đi.

### Do bạn outsource việc thu thập data cho bên thứ ba
Một số doanh nghiệp do nguồn lực hạn chế đã outsource cho một đối tác bên thứ ba để thu thập, ghi nhận lại các dữ liệu vận hành của mình. Việc này không phải là vấn đề nếu như bạn nhận bàn giao đầy đủ về dữ liệu từ đối tác. Nhưng trong nhiều trường hợp, công ty quá tập trung vào vấn đề kinh doanh nên bỏ quên mất các thỏa thuận về dữ liệu sau khi kết thúc hợp đồng.

### Do nhân viên ghi nhận trong... đầu
Tình trạng này diễn ra cũng khá nhiều, nhất là ở các công ty về B2B, các ngành hàng cần thời gian dài để xây dựng nên một cơ sở dữ liệu và thông tin về khách hàng, quy trình. Vấn đề hoàn toàn không xa lạ: mọi dữ liệu được nhân viên ghi nhận trong các file riêng lẻ, khi nghỉ họ không bàn giao (vô tình hoặc cố ý) nên công ty bị mất sạch toàn bộ dữ liệu này. Một số công ty có dùng Google Workspace, Microsoft 365 hay Lark thì còn có thể cứu lại được bằng cách truy cập dữ liệu từ tài khoản đã khóa, nhưng nếu không có giải pháp từ đầu thì cũng không cứu được.

Và ngay cả khi đã có hệ thống để ghi nhận, vẫn có tình trạng nhân viên cố ý không ghi nhận dữ liệu vào hệ thống, trong khi quy trình vận hành lại không bắt buộc chuyện này, nên vẫn bị... lủng.

Đây chỉ là 3 nguyên nhân phổ biến, và còn nhiều nguyên nhân khác nữa.

## 5.2. Các giải pháp có thể thực hiện
### Yêu cầu các bên bán giải pháp cung cấp dữ liệu cho bạn
Đôi khi hệ thống mà bạn đang dùng có API, nhưng không được công khai, bạn có thể yêu cầu bên cung cấp giải pháp cho bạn mở ra để bạn sử dụng. Nếu hệ thống không có sẵn, bạn cũng có thể yêu cầu họ lên kế hoạch xây dựng.

Việc lấy được dữ liệu một cách tự động thông qua API, webhook là cách nên chọn, vì khi đó bạn có thể trích xuất, tích hợp dữ liệu tự động. Với giải pháp xuất file Excel, CSV và phải download về, bạn vẫn phải thực hiện thủ công việc tải dữ liệu và đây không phải là giải pháp tốt cho dài hạn.

Tương tự, khi làm việc với các bên thứ ba, hãy đảm bảo rằng họ bàn giao lại cho bạn đầy đủ dữ liệu đã ghi nhận, theo đúng format đã thỏa thuận ban đầu (để tránh việc bạn phải ngồi chỉnh sửa dữ liệu thủ công)

### Số hóa quy trình
Việc bạn xây dựng quy trình làm việc bao gồm việc nhập liệu vào các hệ thống tương ứng cho từng khâu, từng phòng ban sẽ giúp giải quyết vấn đề phân mảnh, thất thoát dữ liệu, vì mọi thứ đã được nhập liệu lên hệ thống số ngay từ đầu. Việc thống kê, tập trung dữ liệu, phân tích và tích hợp dữ liệu về sau sẽ dễ hơn nhiều.

### Chọn lựa các hệ thống "mở" về dữ liệu ngay từ đầu
Mở ở đây có nghĩa là hệ thống cần phải sẵn sàng cho việc lấy dữ liệu qua API theo các quy chuẩn phổ biến, và có thể dễ dàng tích hợp với các phần mềm khác trong tương lai. Việc này sẽ giúp giảm các rắc rối về sau.



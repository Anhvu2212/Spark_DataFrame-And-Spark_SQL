# Spark_DataFrame-And-Spark_SQL

**GIỚI THIỆU VỀ "SPARK DATAFRAME"**
![SPARK](https://cdn.educba.com/academy/wp-content/uploads/2019/08/Spark-DataFrame.png)

DataFrame là một API bậc cao hơn RDD được Spark giới thiệu vào năm 2013 (từ Apache Spark 1.3). Tương tự như RDD, dữ liệu trong DataFrame cũng được quản lý theo kiểu phân tán và không thể thay đổi (immutable distributed). Tuy nhiên dữ liệu này được sắp sếp theo các cột, tương tự như trong Relation Database. DataFrame được phát triển để giúp người dùng có thể dễ dàng thực hiện các thao tác xử lý dữ liệu cũng như làm tăng đáng kể hiệu quả sử lý của hệ thống.
![SPARK](https://scala-phase.org/talks/rdds-dataframes-datasets-2016-06-16/images/dataframe-performance.png)

Khi sử dụng DataFrame API, chúng ta gọi các hàm để trích xuất kết quả mong muốn và Spark sẽ tự động tiến hành các thuật toán xử lý. Tuy nhiên ở bước cuối cùng thì các thuật toán này vẫn được chạy trên RDD mặc dù người dùng chỉ tương tác với DataFrame. Bên cạnh các ưu điểm, thì nhược điểm lớn nhất của DataFrame là API này không hỗ trợ Compile-time type safety, do đó chúng ta khó có thể tiến hành thao tác trên dữ liệu. Ví dụ như khi chúng ta dùng DataFrame để truy xuất people(“age”), kết quả trả về không phải ở dạng Int mà ở dạng Column object. Vì vậy chúng ta không thể thực hiện các thao tác với kết quả này như đối với một Int object. Việc không hỗ trợ type safefy này làm người dùng không thể phát huy lợi thế của type system mà các ngôn ngữ lập trình như Scala, Java,.. hỗ trợ. Ngoài ra, nó còn làm tăng các lỗi runtime mà đáng ra đã được phát hiện tại compile time.
![SPARK](http://itechseeker.com/wp-content/uploads/2018/12/img_5c11b6c1b379b.png)

**GIỚI THIỆU VỀ "SPARK Properties"**
![SPARK](https://scontent-sin6-2.xx.fbcdn.net/v/t1.0-9/93049505_2568474116718827_523214101409693696_n.jpg?_nc_cat=103&ccb=2&_nc_sid=32a93c&_nc_ohc=p4Pk_vBHKKsAX9hYsWy&_nc_ht=scontent-sin6-2.xx&oh=a76b7659bdadf5ca69a67e1886e71c7b&oe=603D39D4)

**GIỚI THIỆU VỀ "SPARK RDD"**
RDD là bộ sưu tập các bản ghi bất biến và được phân vùng, chỉ có thể được tạo bởi các hoạt động chi tiết thô như bản đồ, bộ lọc, nhóm, v.v. Bằng các thao tác chi tiết thô, điều đó có nghĩa là các hoạt động được áp dụng trên tất cả các phần tử trong bộ dữ liệu. RDD chỉ có thể được tạo bằng cách đọc dữ liệu từ bộ lưu trữ ổn định như HDFS hoặc bằng cách chuyển đổi trên RDD hiện có.
![SPARK](https://scontent-sin6-2.xx.fbcdn.net/v/t1.0-9/93049505_2568474116718827_523214101409693696_n.jpg?_nc_cat=103&ccb=2&_nc_sid=32a93c&_nc_ohc=p4Pk_vBHKKsAX9hYsWy&_nc_ht=scontent-sin6-2.xx&oh=a76b7659bdadf5ca69a67e1886e71c7b&oe=603D39D4)

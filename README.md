# Spark_DataFrame-And-Spark_SQL

**GIỚI THIỆU VỀ "SPARK DATAFRAME"**
![SPARK](https://cdn.educba.com/academy/wp-content/uploads/2019/08/Spark-DataFrame.png)

DataFrame là một API bậc cao hơn RDD được Spark giới thiệu vào năm 2013 (từ Apache Spark 1.3). Tương tự như RDD, dữ liệu trong DataFrame cũng được quản lý theo kiểu phân tán và không thể thay đổi (immutable distributed). Tuy nhiên dữ liệu này được sắp sếp theo các cột, tương tự như trong Relation Database. DataFrame được phát triển để giúp người dùng có thể dễ dàng thực hiện các thao tác xử lý dữ liệu cũng như làm tăng đáng kể hiệu quả sử lý của hệ thống.
![SPARK](https://scala-phase.org/talks/rdds-dataframes-datasets-2016-06-16/images/dataframe-performance.png)

Khi sử dụng DataFrame API, chúng ta gọi các hàm để trích xuất kết quả mong muốn và Spark sẽ tự động tiến hành các thuật toán xử lý. Tuy nhiên ở bước cuối cùng thì các thuật toán này vẫn được chạy trên RDD mặc dù người dùng chỉ tương tác với DataFrame. Bên cạnh các ưu điểm, thì nhược điểm lớn nhất của DataFrame là API này không hỗ trợ Compile-time type safety, do đó chúng ta khó có thể tiến hành thao tác trên dữ liệu. Ví dụ như khi chúng ta dùng DataFrame để truy xuất people(“age”), kết quả trả về không phải ở dạng Int mà ở dạng Column object. Vì vậy chúng ta không thể thực hiện các thao tác với kết quả này như đối với một Int object. Việc không hỗ trợ type safefy này làm người dùng không thể phát huy lợi thế của type system mà các ngôn ngữ lập trình như Scala, Java,.. hỗ trợ. Ngoài ra, nó còn làm tăng các lỗi runtime mà đáng ra đã được phát hiện tại compile time.
![SPARK](http://itechseeker.com/wp-content/uploads/2018/12/img_5c11b6c1b379b.png)

**GIỚI THIỆU VỀ "SPARK SQL"**
![SPARK](https://cdn.app.compendium.com/uploads/user/e7c690e8-6ff9-102a-ac6d-e4aebca50425/f4a5b21d-66fa-4885-92bf-c4e81c06d916/Image/753ace3c801b53535077d9474ecc5f1e/odi_spark_sql_databricks.jpg)

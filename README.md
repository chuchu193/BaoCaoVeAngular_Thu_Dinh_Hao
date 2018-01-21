<h1>Các directive cơ bản trong Angular:</h1>
<h2>ngFor trong Angular:</h2>
  NgFor cung cấp các biến cục bộ, mỗi biến có một chức năng khác nhau:<br>
  - index xác định chỉ số hiện tại của vòng lặp tương ứng.<br>
  - first xác định vòng lặp hiện tại có phải là vòng lặp đầu tiên không.<br> 
  - last xác định vòng lặp hiện tại có phải là vòng lặp cuối cùng không <br>
  - even xác định vòng lặp hiện tại có phải là vòng lặp có chỉ số chẵn không<br> 
  - odd xác định vòng lặp hiện tại có phải là vòng lặp có chỉ số lẻ không <br>
  NgFor cho phép xây dựng danh sách và bảng trình bày dữ liệu trong các mẫu HTML. Chúng ta hãy lấy ví dụ các dữ liệu sau:<br>

![](https://i.imgur.com/fAvlIal.jpg)<br>

  Với ngFor chúng tôi có thể in dữ liệu này tới màn hình dưới dạng một bảng dữ liệu, bằng cách tạo HTML tương tự như sau:

![](https://i.imgur.com/OYh5CLB.jpg)<br>
  Để sử dụng ngFor, hãy tạo một thành phần để chúng ta có thể có một mẫu HTML hoạt động:

![](https://i.imgur.com/TMS1VJl.jpg)<br>

  -Một biến lặp tên Hero được định nghĩa bằng cách sử dụng từ khóa let, phù hợp với cú pháp Javascript
   
   <h4> 1.Index: </h4>
   Một yêu cầu rất phổ biến là để thêm vào một danh sách các vị trí chỉ số số nguyên tố của nó. Chúng ta có thể lấy chỉ mục của phần tử hiện tại bằng cách sử dụng **index**:
   
   ![](https://i.imgur.com/FzcwKmu.jpg)<br>

*Lưu ý :cần từ khóa let để có được giá trị của index .

   <h4> 2.Even và Odd : </h4>
   Một chức năng rất phổ biến cần thiết khi xây dựng các bảng là để có thể định dạng một bảng bằng cách thêm một lớp css khác nhau cho các hàng chẵn hoặc lẻ.
   Giả sử rằng trong bảng trên, chúng ta muốn thêm một lớp CSS even khi hàng là chẵn và odd khi hàng là lẻ.
   Để làm như vậy, chúng ta có một vài biến có sẵn:even và odd, có thể được sử dụng theo cách sau cùng với ngClass:
   
   ![](https://i.imgur.com/mJ9nndQ.jpg)<br>

HTML được tạo ra bởi mẫu này:<br>

   ![](https://i.imgur.com/aFIHIMi.jpg)<br>
   
  <h4> 2.First và Last: </h4>
  Cũng giống như các chức năng thậm chí và lẻ, cũng có hai biến khác có thể được sử dụng để xác định các yếu tố đầu tiên và cuối cùng của danh sách:
 
   ![](https://i.imgur.com/D7CbaBL.jpg)<br>
   
   Điều này sẽ thêm một lớp CSS có tên là fist vào phần tử đầu tiên của danh sách và một lớp CSS có tên là last của phần tử cuối cùng trong danh sách:<br>
   ![](https://i.imgur.com/mGxLzMT.jpg)<br>
   




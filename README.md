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
   
   <h4> 1.Index </h4>:
   Một yêu cầu rất phổ biến là để thêm vào một danh sách các vị trí chỉ số số nguyên tố của nó. Chúng ta có thể lấy chỉ mục của phần tử hiện tại bằng cách sử dụng **index**:
   
   ![](https://i.imgur.com/FzcwKmu.jpg)<br>






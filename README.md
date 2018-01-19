# BaoCaoVeAngular_Thu_Dinh_Hao
# Model and View with 2 away binding
  - Tow-Way binding : Là sự liên kết 2 chiều giữa model và view . Nếu người dùng thay đổi giá trị các field (thuộc tính) bên trong thẻ dữ   liệu đầu vào (input) thì các thuộc tính (property) liên quan sẽ thay đổi theo , và ngược lại các thuộc tính này cũng tác động tới làm     thay đổi view.
  - Có 2 cách làm thay đổi propertys từ các giá trị input vào :
      - Cách 1 : sử dụng ng-model
      Ví dụ 1: Nhập vào tên user -> biến name nhập dữ liệu  -> show ra màn hình.
            <div ng-app="myApp" ng-controller="myCtrl">
                Name: <input ng-model="name">
                <h1>You entered: {{name}}</h1>
            </div>
      - Cách 2 :  không sử dụng ng-model
      ví dụ 2: <form ng-app="" name="myForm">
                  Email:
                  <input type="email" name="myAddress" >
                  <h1>You entered: {{ myAddress }}</h1>
                </form>
    
# Tìm Hiểu Module, Component, Injectable, Pipe, Directive.
- Mối quan hệ giữa chúng :
  ![](https://i.imgur.com/J8Lw26O.png)
1. Module:
   - Là vùng chứa cho các phần khác nhau của ứng dụng của bạn như : controllers, services, filters, directives,.... Có chức năng xử lý 1        phần gì đó trong chương trình của bạn.
      ví dụ : <div ng-app="myApp">
                <div>
                  <h3> this is: {{ 'World' | greet }}</h3>
                </div>
              </div>
              <script>
                  var myAppModule = angular.module('myApp', []);
                  // configure the module.
                  // in this example we will create a greeting filter
                  myAppModule.filter('greet', function() {
                   return function(name) {
                      return 'Hello, ' + name + '!';
                    };
                  });
              </script>
   - Lưu ý:
      + khi tạo module thì mỗi module là một tính năng.
      + Nếu một component có thể tái sử dụng thì nên tạo 1 module cho nó để dễ dàng sử dụng lại.(đặc biệt là các drectives và filters)
      
2. Component:
    - Điều chỉnh 1 thành phần của màn hình :(view)
    - Đặc điểm :
        - Component có thể chứa nhiều thẻ HTML.
        - Mỗi Component có thể chứa những Component khác trong đó.
        - Component có thể nhận tham số truyền vào :
        Ví dụ : 
        + file : book.component.ts
            export class BookComponent implements OnInit {
                name = "hello";
                arry = ['vu', 'Thi', 'Hao'];

                constructor() { }

                ngOnInit() {
                }
                showEvent(event){
                  this.name = event.target.value;
                }
            }
         + file : book.component.html
             <input  placeholder="Enter your name" (keyup) = "showEvent($event);">
             <h3> your name is: {{ name }}</h3>
    ==> Ưu điểm sử dụng component :
        - Dễ quản lý code theo quy luật đặt tên các component cha con chuẩn.
        - Tái sử dụng code dễ dàng.
  3. Injectable
  4. Pipe
  5. Drective
         

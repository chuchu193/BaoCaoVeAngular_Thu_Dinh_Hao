﻿# BaoCaoVeAngular_Thu_Dinh_Hao

<h2> 3 Hướng Đối Tượng Trong TypeScript</h2>

### TypeScript là gì
TypeScript là một dự án mã nguồn mở được phát triển bởi Microsoft, nó có thể được coi là một phiên bản nâng cao của Javascript bởi việc bổ sung tùy chọn kiểu tĩnh và lớp hướng đối tượng mà điều này không có ở Javascript. 
TypeScript có thể sử dụng để phát triển các ứng dụng chạy ở client-side (Angular2) và server-side (NodeJS).
### Tại sao nên sử dụng TypeScript
**Dễ phát triển dự án lớn**: Với việc sử dụng các kỹ thuật mới nhất và lập trình hướng đối tượng nên TypeScript giúp chúng ta phát triển các dự án lớn một cách dễ dàng.
<br>
**Nhiều Framework lựa chọn**: Hiện nay các Javascript Framework đã dần khuyến khích nên sử dụng TypeScript để phát triển, ví dụ như AngularJS 2.0 và Ionic 2.0.
<br>
**Hỗ trợ các tính năng của Javascript phiên bản mới nhất**: TypeScript luôn đảm bảo việc sử dụng đầy đủ các kỹ thuật mới nhất của Javascript, ví dụ như version hiện tại là ECMAScript 2015 (ES6).
<br>
**Là mã nguồn mở**: TypeScript là một mã nguồn mở nên bạn hoàn toàn có thể sử dụng mà không mất phí, bên cạnh đó còn được cộng đồng hỗ trợ.
<br>
**TypeScript là Javscript**: Bản chất của TypeScript là biên dịch tạo ra các đoạn mã javascript nên ban có thê chạy bất kì ở đâu miễn ở đó có hỗ trợ biên dịch Javascript. Ngoài ra bạn có thể sử dụng trộn lẫn cú pháp của Javascript vào bên trong TypeScript, điều này giúp các lập trình viên tiếp cận TypeScript dễ dàng hơn.
### Cách cài đặt và sử dụng
- Cài đặt: 

B1: Ta vô trang web: https://www.typescriptlang.org/

B2: Máy bạn cần cài đặt nodejs và npm trước để thực hiện lệnh

<img src ="https://i.imgur.com/AZhFIoj.png">

B3: Kiểm tra typescript đã cài đặt thành công chưa

<img src = "https://i.imgur.com/qm3C67F.png">

- Sử dụng:
Sử dụng công cụ Visual Studio Code để code

B1: Tạo file demo.tsc

B2: Vào cmd nhập câu lệnh tsc demo.tsc sẽ tạo ra file demo.js

B3: Cuối cùng ta nhập lệnh node demo.js sẽ biên dịch đoạn demo.js

**Kết Quả**
<img src ="https://i.imgur.com/ZUyVzqQ.png">
### Huơng Đối Tượng Trong TypeScript
- Cách khai báo 1 CLASS:
Gồm có: 
**Properties(thuộc tính)**: có public và private
<br>
**FunTion(Hàm)**

<img src ="https://i.imgur.com/Wo2l8bl.png">	
		
**Constructor()**

<img src ="https://i.imgur.com/D7oREzk.png">

Xét private của 1 tham số:

<img src="https://i.imgur.com/SNmQqMa.png">

- Tính thừa kế:
<br>
Class A và Class B: Lớp B kế thừa lớp A có nghĩa là trong lớp A có thuộc tính gì thì lớp B được kế thừa lại

<img src="https://i.imgur.com/xnjCR2s.png">

# Model and View with 2 away binding
  - Tow-Way binding : Là sự liên kết 2 chiều giữa model và view . Nếu người dùng thay đổi giá trị các field (thuộc tính) bên trong thẻ dữ   liệu đầu vào (input) thì các thuộc tính (property) liên quan sẽ thay đổi theo , và ngược lại các thuộc tính này cũng tác động tới làm     thay đổi view.
  - Có 2 cách làm thay đổi propertys từ các giá trị input vào :
      - Cách 1 : sử dụng ng-model
     + Ví dụ 1: Nhập vào tên user -> biến name nhập dữ liệu  -> show ra màn hình.<br>
          `<div ng-app="myApp" ng-controller="myCtrl"> ` <br>
               ` Name: <input ng-model="name"> ` <br>
               ` <p>You entered: {{name}}</p> `<br>
            `</div>  `<br>
           
      - Cách 2 :  không sử dụng ng-model <br>
      ví dụ 2:  `<form ng-app="" name="myForm">`<br>
                 ` Email: `<br>
                 `<input type="email" name="myAddress" > `<br>
                 ` <p>You entered: {{ myAddress }}</p> `<br>
               ` </form> `<br>
    
# Tìm Hiểu Module, Component, Injectable, Pipe, Directive.
- Mối quan hệ giữa chúng :
  ![](https://i.imgur.com/J8Lw26O.png)
## 1. Module:
   - Là vùng chứa cho các phần khác nhau của ứng dụng của bạn như : controllers, services, filters, directives,.... Có chức năng xử lý 1        phần gì đó trong chương trình của bạn.
      + ví dụ :
            `<div ng-app="myApp">` <br>
               ` <div> `<br>
                 ` <h3> this is: {{ 'World' | greet }}</h3>` <br>
                `</div> `<br>
              `</div> `<br>
             ` <script> `<br>
                 ` var myAppModule = angular.module('myApp', []); `<br>
                  `// configure the module`<br>
                  `// in this example we will create a greeting filter` <br>
                 ` myAppModule.filter('greet', function() { `<br>
                  ` return function(name) { `<br>
                    `  return 'Hello, ' + name + '!'; `<br>
                     ` });`<br>
                 ` });`<br>
             `</script>`<br>
             
   - Lưu ý:
      + khi tạo module thì mỗi module là một tính năng.
      + Nếu một component có thể tái sử dụng thì nên tạo 1 module cho nó để dễ dàng sử dụng lại.(đặc biệt là các drectives và filters)
      
## 2. Component:
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
                 ngOnInit() {}
                showEvent(event){
                  this.name = event.target.value;
                }
            } 
         + file : book.component.html
            <input  placeholder="Enter your name" (keyup) = "showEvent($event);">
             <p> your name is: {{ name }}</p> 
            
             
   - ==> Ưu điểm sử dụng component : 
        - Dễ quản lý code theo quy luật đặt tên các component cha con chuẩn.
        - Tái sử dụng code dễ dàng.
 ## 3. Injectable:
    - Injectable: Là những đối tượng được angular tạo ra từ khai báo của người dùng, do angular quản lý và có thể truyền vào trong các         class khác hoặc các đối tượng khác.
    - Injected : là đối tượng có chứa một số chỗ đánh dấu (thường là tham số của hàm khởi tạo) để AngularJS có thể truyền các đối tượng       có thể truyền được vào bên trong nó.<br>
    - Inject: để chỉ hành động lấy giá trị hoặc tham chiếu của một đối tượng (giả sử là A), gán cho thuộc tính của một đối tượng khác          (đối tượng B) theo một cách nào đó.<br>
    Ví Dụ :
            `class Engine {...}`<br>
            <br>
            `class Transmission {...}`<br>
            <br>
           ` @Injectable ()`<br>

           ` class Car {`<br>

                engine;

                trasmission;

                constructor (engine Engine, transmission Transmission) {

                    this.engine = engine;

                    this.transmission = transmission;

                }
              `}`<br>
   
##  4. Pipe
    - Là cách để ta thực hiện việc chuyển hóa dữ liệu ( transformation ), để dễ dàng hiển thị ra dưới định dạng như ta mong muốn.
    - Ví dụ :
            import { Component } from '@angular/core';

            @Component({`
              selector: 'hero-birthday',
             template: '<p>The hero's birthday is {{ birthday }}</p>'
               `})
           export class HeroBirthdayComponent {
             birthday = new Date(1988, 3, 15); // April 15, 1988
            }
            
       + Nếu để hiển thị ngày sinh bằng cách mặc định như thế này, output dạng ri Apr 15 1988 00:00:00 GMT-0700 (Pacific Daylight Time),          tương đối khó đọc. 
       
       + Bằng cách dùng pipe date, build-in có sẵn trong Angular 2, ta có thể chuyển string hiển thị ngày tháng về dạng dễ đọc hơn
         (ví dụ : template: `<p>The hero's birthday is {{ birthday | date }}</p>` . Khi đó output: April 15, 1988 ) --> thuận tiện cho             view. 
##  5. Directive
    - Directives là một thành phần mở rộng HTML, hay nói cách khác là các thuộc tính (properties) của các thẻ HTML mà Angular nó định         nghĩa thêm, vì nó của riêng của Angular nên phải tuân thủ theo nguyên tắc của nó là chữ bắt đầu luôn luôn là ký tự ng (ví dụ:ng-         prefix), trong đó tiền tố prefix là tên của derective mà chúng ta sử dụng. 
    
    - Một vài Drectives nổi bật có sẵn do angular cung cấp :
        - `Ng-app:` Khi chúng ta khai báo một Directive ng-app thì AngularJS sẽ hiểu là bắt đầu một ứng dụng Angular, nó sẽ xác định đây            là thẻ gốc (element root) và tiếp theo sẽ khởi tạo các thông số cấu hình bên trong mà ta gọi là bootstraps. Ngoài ra ng-app              còn được sử dụng để mô tả các module khác nhau trong ứng dụng. 
        - `Ng-init:` nó có ý nghĩa là khai báo dữ liệu khởi tạo khi ứng dụng vừa được chạy. Các dữ liệu này sẽ được dùng cho toàn bộ                phạm vi của controller mà nó thuộc về.
        ... 
        
     - Lưu ý : Danh sách AngularJS Directives là không cố đinh. Nghĩa là ngoài các Directives mặc định có sẵn trong Angular thì chúng           ta có thể tự tạo được, tạo ra Directives khác phù hợp với mục đích sử dụng của bạn.  
     
       + Ví dụ 1: Xây dựng một Directive xuất hiện lời chào với nội dung "Chào mừng các bạn đến với website freetuts.net".<br>
             <!doctype html>
              <html lang="en">
                  <head>
                      <meta charset="UTF-8">
                      <title>Ví dụ sử dụng Directive</title>
                     <script src="//ajax.googleapis.com/ajax/libs/angularjs/1.3.2/angular.min.js"></script>
                      <script language="javascript">
                             angular.module('myapp', [])
                              .controller('MyController', function($scope) {
                                  //
                              })
                              .directive('myDirective', function() {
                                  return {
                                     template: '<h1>Chào mừng các bạn đến với website freetuts.net</h1>'
                                 };
                              });
                      </script>
                  </head>
                  <body ng-app="myapp">
                     <div ng-controller="MyController">
                          <div my-directive></div>
                     </div>
                  </body>
              </html>
              

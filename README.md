
﻿<h1> BaoCaoVeAngular_Thu_Dinh_Hao </h1>

<h2> 1. Hướng Đối Tượng Trong TypeScript</h2>

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

<h2> 2. Model and View with 2 away binding </h2> 
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
    
<h2> 3. Tìm Hiểu Module, Component, Injectable, Pipe, Directive. </h2>
- Mối quan hệ giữa chúng :

![](https://i.imgur.com/J8Lw26O.png)

## 3.1. Module:
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
      
## 3.2. Component:
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
 ## 3.3. Injectable:
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
   
##  3.4. Pipe
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
##  3.5. Directive
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
              
			  
<h1> 4. Các directive cơ bản trong Angular:</h1>
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
   
  <h4> 3.First và Last: </h4>
  Cũng giống như các chức năng thậm chí và lẻ, cũng có hai biến khác có thể được sử dụng để xác định các yếu tố đầu tiên và cuối cùng của danh sách:
 
   ![](https://i.imgur.com/D7CbaBL.jpg)<br>
   
   Điều này sẽ thêm một lớp CSS có tên là fist vào phần tử đầu tiên của danh sách và một lớp CSS có tên là last của phần tử cuối cùng trong danh sách:<br>
   ![](https://i.imgur.com/mGxLzMT.jpg)<br>
 
 <h2> ngIf trong Angular: </h2>
 -NgIf là một chỉ thị cấu trúc có thể thêm hoặc loại bỏ phần tử lưu trữ trong cách bố trí DOM(Document Object Model: mô hình các đối tượng trong tài liệu HTML) trong thời gian chạy.NgIf hoạt động trên cơ sở kết quả đúng và sai của biểu thức nhất định.Nếu điều kiện là đúng, các phần tử sẽ được bố trí thêm vào DOM nếu không chúng sẽ được gỡ bỏ.NgIf có thể được sử dụng theo những cách khác nhau.<br>
 
 
 ![](https://i.imgur.com/oOgSYMi.jpg)
 
 Ví dụ về chỉ thị NgIf **ngif.component.html**:
 
  ![](https://i.imgur.com/MNxPp6f.jpg)
  
  -Trong đoạn mã trên hai phần tử đang sử dụng NgIf. Trên cơ sở điều kiện đúng và sai, các <div> tương ứng sẽ được thêm vào hoặc gỡ bỏ khỏi DOM.
  **ngif.component.ts**
 
![](https://i.imgur.com/oO7j0Pj.jpg)

Màn hình:

![](https://i.imgur.com/kdW6geb.jpg)

<h3>Sử dụng Ngif với else </h3>

Đối với else chúng ta cần phải sử dụng phần tử <ng-template>.
**ngif-else.component.html**
![](https://i.imgur.com/dLAM7Ta.jpg)<br>

Trong đoạn mã trên, chúng ta sử dụng hai ví dụ của chỉ thị NgIf.Khi điều kiện là đúng, phần tử máy chủ sẽ được thêm vào trong bố cục DOM và nếu điều kiện là sai thì khối mã <ng-template> sẽ chạy ở vị trí của phần tử máy chủ lưu trữ.
**ngif-else.component.ts**

![](https://i.imgur.com/LFpyeSg.jpg)<br>

Màn hình:<br>

![](https://i.imgur.com/trB7D4a.jpg)

 <h2> ngModel trong Angular: </h2>

Angular 2 có một directive để áp dụng two-way binding đó là ngModel. Chúng ta có thể bao ngModel trong cặp dấu [()], nó sẽ thực hiện đồng bộ dữ liệu từ Component vs DOM và ngược lại.
**app.component.html**<br>
![](https://i.imgur.com/u8bv68j.jpg)<br>

**app.component.ts**<br>
![](https://i.imgur.com/JAtkctx.jpg)<br>

Nếu không sử dụng [(ngModel)] chúng ta có thể hoàn toàn viết một cú pháp tương ứng cho ví dụ trên như sau:<br>

**app.component.html**<br>

![](https://i.imgur.com/qDYGjlh.jpg)<br>

Khi không sử dụng directive ngModel ở cấu trúc binding bởi cặp dấu [()], chúng ta hoàn toàn có thể tách thành 2 cấu trúc binding riêng biệt là event binding và property binding:<br>

**app.component.html**<br>
![](https://i.imgur.com/aL9T2q3.jpg)<br>

Như các bạn có thể thấy,  directive ngModel ở ví dụ minh họa trên bao gồm property ngModel và event ngModelChange.


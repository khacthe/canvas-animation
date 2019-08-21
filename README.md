# Craw canvas 2D, 3D, Animation with P5 library

## Add library
- Quản lý thư viên với npm
```
npm install -g p5-manager // install p5 manager

// Initialize a new collection

p5 new my_project

// Generate p5 project

p5 g my_project

// Generate p5 project and bundle

p5 g -b my_project

// Run server

p5 server

OR

p5 s

```
## Struct
- Ta sử dụng 2 hàm chính setup và draw để bắt đầu
```
function setup() {
	createCanvas(800, 800);  // Tạo phạm vi canvas với with, height
}

function draw() {
  // Thực thi draw
}

```
## Example
- Draw shapes
 + p5 cung cấp function vè hình 2D một cách dễ dàng
```
ellipse(100, 100, 80, 80); // Hinh tròn, 2 giá trị đầu lạ tọa độ tâm
rect(0, 0, 80, 80); // Hình chữ nhật với 2 giá trị đầu là tâm, giá trị sau là cạnh
square(30, 20, 55); // Hinhf vuông
triangle(30, 75, 58, 20, 100, 100); // Hình tam giác với mỗi cạp là tọa độ của các đỉnh tam giác

function setup() {
	createCanvas(800, 800);
}

function draw() {
  ellipse(100, 100, 80, 80);
  rect(0, 0, 80, 80);
  triangle(30, 75, 58, 20, 100, 100);
}
```
[Draw shapes pull](https://github.com/khacthe/canvas-animation/pull/1)
[Function list draw shapes 2D](https://p5js.org/reference/#group-Shape)

- Loop and Redraw
  + Quá trình trong hàm draw sẽ được loop
```
// example
let y = 100;
function setup() {
  createCanvas(720, 400);
  stroke(255); set màu
  frameRate(30); // animation delay
}

function draw() {
  background(0);
   y = y - 1;
   if (y < 0) {
     y = height;
   }
   line(0, y, width, y); vẽ line
}

ở trên quá trình vè đường line sẽ liên tục -> ta cảm nhận nó di chuyển từ dưới lên trên

view: http://localhost:5555/loop_in_p5/

```
  + Để ngăn quá trình draw loop tacos thể sử dụng hàm noLoop();

```
// add thêm function

function setup() {
  createCanvas(720, 400);
  stroke(255); set màu
  noLoop(); // set no loop
  frameRate(30); // animation delay
}
```
+ nếu bạn muốn thay đổi quá trình đó có thể sử dụng sự kiện với hàm redraw
```
function mousePressed() { // mỗi lần click chuột thì quá trình loop xảy ra
  redraw();
}
```

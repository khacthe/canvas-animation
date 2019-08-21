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

```

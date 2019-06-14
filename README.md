# tutorial-webpack
Hướng dẫn webpack
- Tác dụng của webpack:
  + Xử lý file trước khi import vào
  + Chuyển đổi jsx sang js
  + Require css vào js
  ...
  
- Tạo file webpack.config.js để lưu cấu hình webpack cho project
  + Nội dung file config:( 
    const path = require('path');

      const config = {
          entry : './src/index.js',
          // entry là điểm bắt đầu để đọc file
          output : {
              filename : 'bundle.js',
              // filename chỉ định tên file khi build ra
              path : path.resolve(__dirname, 'build')
              // chỉ định đường dẫn chưa file bundle.js,nếu không có path thì nó tạo ở thư mục ngoài cùng
          }
      }
      module.exports = config;
  )
- Cài thêm : npm i -g webpack-cli nếu bị lỗi không cài được webpack cli.
- Sử dụng : webpack để chạy => nó sẽ tạo ra thư mục build chứa file bundle.js
- Nhúng file bundle.js vào dile index mới có thể sử dụng được.
- Để lấy ảnh nhanh thì vào lorempixel.com/height/width và copy url.
- Cài các pagkage như : babel-core,babel-preset-env,babel-loader,css-loader,style-loader.
- Để trình duyệt hiểu được cú pháp của react thì cài thêm : babel-preset-react và babel-preset-stage-2 
.Trong .babelrc thêm : {"presets" : ["babel-preset-react","react","stage-2"]}
- Thay đổi scripts trong package.json thành : build :"webpack" rồi chạy npm run build thay vì gõ webpack
- Trong webpack không thể dùng BrowserRouter mà phải dùng HashRouter mới được.


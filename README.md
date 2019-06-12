# tutorial-webpack
Hướng dẫn webpack
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

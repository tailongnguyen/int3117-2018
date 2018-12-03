# Jedi - một thư viện tự động điền /phân tích tĩnh  cho Python

Jedi là một công cụ phân tích tĩnh cho Python có thể sử dụng cho cả IDE và Editor . Chức năng chủ yếu của nó là tự động điền cũng như phân tích tĩnh . Jedi chạy rất nhanh và được test rất cẩn thận. Nó có thể hiểu được các dòng code Python ở một mức sâu hơn các công cụ phân tích tĩnh khác.
Jedi sử dụng một API vô cùng đơn giản để giao tiếp với IDE, chính vì thế nó được gợi ý để sử dụng với các IDE. Các IDE được hỗ trợ bao gồm: Vim, Emacs, Sublime Text, Atom, Visual Studio Code, Gedit, Eric IDE, IPython, Kate.

Dưới đây là một vài bức ảnh của jedi-vim:

![] https://github.com/davidhalter/jedi/raw/master/docs/_screenshots/screenshot_complete.png

Tự động điền cho hầu hết các lệnh (Ctrl+Space):

![] https://github.com/davidhalter/jedi/raw/master/docs/_screenshots/screenshot_function.png

Hiển thị các hàm, các lớp:

![] https://github.com/davidhalter/jedi/raw/master/docs/_screenshots/screenshot_pydoc.png


Cài đặt
============

    pip install jedi

Chú ý: Câu lệnh trên chỉ cài đặt thư viện Jedi, không phải plugin cho trình soạn thảo


Phân tích tĩnh / Linter
------------------------

Để thưc hiện tất cả các dạng phân tích tĩnh, vui lòng sử dụng ``jedi.names``. Nó sẽ trả về một danh sách các tên để bạn có thể sử dụng để trỏ đến các dạng và hơn thế nữa

Linting cũng là một chức năng nữa của Jedi. Bạn có thể dùng thử bản alpha của chức năng này bằng câu lệnh ``python -m jedi linter``. API trên có thể thay đổi trong tương lại và có thể vẫn còn có lỗi nhỏ.

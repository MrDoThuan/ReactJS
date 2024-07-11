browserslist: Dùng để add nhiều modifications để tất cả các version đều dùng được
package-lock: Chứa những thông tin của những package đang xài, lần sau khi vào thì sẽ không cần load lại
gitignore: Chứa dữ liệu không cần thiết


Tạo SSH key
 ssh-keygen -t rsa -b 4096 -C "huuthuan110804@gmail.com" : Tạo key SSH
 Nhập nơi chứa (có thể đôi tên id_rsa), mật khẩu, xác nhận mk

  eval $(ssh-agent -s): Tạo 1 agent SSH

   ssh-add ~/.ssh/id_rsa: Add SSh key vào id_rsa
Đẩy SSh lên github
    cat ~/.ssh/id_rsa.pub: Hiện thông tin về key, Coppy

Lên github, vào cài đặt, vào SSH key, tạo mới, dán phần vừa Copy vào, đặt tên và lưu
Để kiểm tra: vào Git Bash, gõ ssh -T git@github.com 
bấm yes.
Nếu hiển thì dòng Hi,... là thành công


Đẩy code lên github với SSH key
 
 Tạo 1 repository mới: Vào github, ở dấu + bấm new repository, nhập tên repo sau đó ấn create.

 vào VS code hoặc git bash (thuộc dự án, project đó. Nghĩa là phải link tới phần code muốn push) (vd Thuan.... /d/learn-reactjs-basic)
 gõ lệnh: git remote add origin git@github.com:MrDoThuan/ReactJS.git (đuối ReactJs là tên của repository)
 sau đó gõ: git remote -v để xem đã có chưa.
 Nếu hiển thị:
 origin  git@github.com:MrDoThuan/ReactJS.git (fetch)
origin  git@github.com:MrDoThuan/ReactJS.git (push)
thì thành công.
sau đó gõ lệnh push: git push -u origin master: Nghĩa là sẽ push thông tin ở master vào origin và xóa đi master.
Lên repository vừa tạo để push, reload lại

Sử dụng Vercel: (Đã liên kết với github)
vào code như bình thường, sau đó khi muốn push lên github, vào Source Control (hình 3 hình tròn ngay dưới kinh lúp) sau đó bấm dấu + , gõ vào phần Message cái nội dung sau đó bấm tổ hợp phím Ctrl + Enter là xong.

Sau đó ngay dấu 3 chấm ( ... ) chọn Push,Pull -> Push
Đợi load, khi hoàn thành sẽ được đẩy lên github và vercel.
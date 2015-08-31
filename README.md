# HƯỚNG DẪN SỮ DỤNG GIT




-------------------------------------------------
	HƯỚNG DẪN CHO NGƯỜI MỚI BẮT ĐẦU DÙNG GIT
-------------------------------------------------

**B1**. Dùng Terminate cài đặt Git: 

	sudo apt-get -y install git
	
Nhập password để download.

**B2**. thực hiện tạo thư mục và thực hiện Git

	cd Desktop   #đi đến thư mục Desktop

	mkdir DirWord-1  #tạo 1 thư mục tên là DirWiord-1

	cd DirWord-1    #đi đến thư mục

	touch hello     #tạo file hello

**B3**. tạo Chứng thực cho Thư mục.1 online Hoặc Offline

#online

	git config --global user.name "12015851.Lê Ngọc Khánh"

	git config --global user.email "ngockhanh111021994@gmail.com"

#offline

	git config --local user.name "l12015851.Lê Ngọc Khánh"
	
	git config --local user.email "ngockhanh111021994@gmail.com"
	
**B4**. Khởi tạo và thực hiện.

	git init
	
	git clone https://github.com/chuyendemang/chuyendemang-dhth8.git 
	
* tài liệu PDF + hướng dẫn có trong này (*).
	
	git config -l
	
**B5**. ghi nội dung vào file hello

	echo "chuyen de mang lop dhth8" >hello
	
**B6**. đọc nội dung lên màn hình

	cat hello
	
**B7**. chỉ ra mục và thư mục hiện tại.

	git status
	
**B8**. thực hiện code

	git add hello   # thêm vào file hello với nội dung echo vừa ghi.
	
	git diff 	#kiểm tra sự khác nau của index và Working Directory.
	
Đọc thêm tài liệu từ Github của thầy đính trên(*) B4 trong file chuyendemang.

	git commit -m "TênCommit-1"	#lưu ý tên commit có ý nghĩa sau này còn dùng lại còn hiểu được
	
	git diff 	# so sánh lại lần nữa có giống nhau không.
	
	git status 	# kiểm tra sự khác biệt của thư mục  hiện tại.
	
	git log		#kiểm tra các commit của log trên.
	
**B9**. Thực hiện BRANCH (tạo nhánh, rẽ). mặc định Git luôn có master là branch mặc định.
branch là con trỏ, trỏ tới commit.

	git branch -v	#xem các branch cua git.
	
	git branch UPPER #tạo branch UPPER.
	
	git branch -v	#xem các lại các branch.
	
	git log	
	
	echo "LENGOCKHANH DHTH8C >>hello
	
	cat hello	#lúc này để ý thấy nội dung sẽ khác.
	
	git add hello
	
	git commit -m "TenCommit-2"
	
	git log	
	
	git checkout UPPER 	#chuyển sang branch UPPER. mặc định đang ở master.
	
	git log		#kiểm tra các branch đang dùng.	
	
	echo "lengockhanh dhth8c">>hello	#ghi nội dung thêm vào file hello.
	
	git diff	#kiem633 tra sự khác nhau với file index.
	
	git diff -u 	#update lại
	
	git commit -m "TenCommit-3"
	
	git log		
	
	git status
	
	git branch -v
	
	cat hello	#lúc này để ý thấy nội dung sẽ khác.
	
	git checkout master
	
	cat hello	#lúc này để ý thấy nội dung sẽ khác.
	
	git diff UPPER master 	#so sánh 2 branch UPPER master.
	
	git checkout master	#chuyển sang branch master.
	
**B10**. Thực hiện MERGING (gộp,hợp lại).

	git merge UPPER		#chuyển branch master tới UPPER.(lưu ý branch là con trỏ).
	
	git checkout master	#chuyển sang lạ master.	
	
	git branch -d UPPER	#xóa branch UPPER.(lưu ý xóa con trỏ nhưng nội dung vẫn còn)
	
** Đặc biệt không thể xóa master.

	git log --graph		#xem dạng log rõ ràng hơn.
	
	git status	
	
	git diff
	
**B11**. Thực hiện reset xóa các branch vửa tạo.
(khuyến khích ko nên xóa, mà tạo 1 branch mới vì branch là con trỏ tạo sẽ nhanh hơn).

	echo "Lê Ngọc Khánh DHTH8" >>hello
	
	git add -u
	
	git commit -m "TenComit-4"
	
	git diff
	
	git log
	
	git reset --hard HEAD	# xóa commit trước đó.xóa 'Tencommit-4'
	
lưu ý có thể xóa các commit theo: 

-xóa theo HEAD:	HEAD, HEAD^,HEAD^^,HEAD^^^ ......... 

	git reset --hard HEAD
	
-xóa theo Hash : ad9wa8d089w,a88d768w8ad9.... #hash này lấy trong git log ra.

	git reset --hard ad9wa8d089wa8
	

** Nhìn tổng quan lại thầy cấu trúc chương trình **

	change->add->commit
	
	(sữa -> thêm -> ghi log)

------------------------------------------------------
	CHÚC CÁC BẠN HOÀN THÀNH TỐT BÀI TẬP TUẦN 1.
	
	MỌI NGƯỜI CÙNG NHAU CHIA SẼ KINH NGHIỆM :D
------------------------------------------------------

Ngoài ra có các software dùng Github trên windows mình thấy cũng tốt và nhanh, nếu ai thích thì download về dùng thử
Link: 

	https://desktop.github.com/ 
	
Video Hướng dẫn sữ dụng cơ bản: 

	https://www.youtube.com/watch?v=bdqnubR3P1Y
	
Làm việc nhóm với Git: 	

	https://www.youtube.com/watch?v=tPYk9HthLG0

--------------------------------------------

**	PHẦN TIẾP THEO ĐƯA DỮ LIỆU LÊN GIT**

--------------------------------------------

Phần này hướng dẫn các bạn đưa dữ liệu lên Git.

sau khi đăng kí tài khoản của các bạn thì dùng git đễ push dữ liệu lên mạng sau khi edit.

Ví dụ: mình có trang web  https://www.github.com/lngkhanh/huongdansudunggit và có các file bên trong.

**B1.** mình clone web về dưới dạng HTTPS.

  	git clone https://www.github.com/lngkhanh/huongdansudunggit
  
**B2.** Xem có file đã Clone về thành công hay không.

	 ls -a
  
**B3.** Edit code của bạn. thêm hay xóa dữ liệu trong file.

  	cd huongdansudunggit
  
  	touch adderFile # mình tự tạo file tên adderFile
  
  	echo "this is file edit code add" >adderFile
  
  	cat adderFile 
  
  	git add adderFile 
  
  
	git commit -m "file added"  
  
  	git push  
**Điền mật khẩu và pass của tài khoản Github (trên website www.github.com). 
  
**đẩy nôi dung lên Git mặc định là master. nếu edit thi dùng (git push origin master )

** kiểm tra trên website có file đã cập nhật chưa !

**B4.** Thực hiện pull (kéo) dữ liệu xuống. dùng lệnh pull

  	git pull  #điền tk và passwd như push
  
** đữ liệu được cập nhật tự động. nếu chưa cập nhât các bạn clone lại hoặc đưa URL trực tiếp vào.

-----------------------------------------

	CHÚC CÁC BẠN THÀNH CÔNG
	Mọi ý kiến connit bên dưới hoặc liên hệ: 
**	Facebook: https://www.facebook.com/lengockhanh8a
**	Gmail: ngockhanh111021994@gmail.com

-----------------------------------------

 








 








# Hướng dẫn sử dụng git bash trên Linux


## Thực hiện push

*Thực hiện trên giao diện github hoặc SCM*

- Bước 1: Tạo 1 repository trên github bằng giao diện, sau đó copy đường link

![ima](../images/gitguide01.png)

- Bước 2: Tạo branch mới 

![ima](../images/gitguide03.png)

*Thực hiện trên server linux*

- Bước 1: Cài đặt git
```sh
dnf -y install git
```
 
- Bước 2: clone repository vừa tạo bằng link đã copy ở trên. Nếu là repository private sẽ phải điền username password của github.
```sh
git clone <your_url>
```

![ima](../images/gitguide02.png)

- Bước 3: Di chuyển vào thư mục đã clone về (thư mục có tên của repository), Chuyển sang nhánh cần chỉnh sửa
```sh
cd <your_directory>
git checkout <your_branch>
```
![ima](../images/gitguide04.png)

- Bước 4: **Ví dụ** ở đây thực hiện copy các file, thư mục cần đưa lên github vào thư mục đã clone về.

![ima](../images/gitguide05.png)

- Bước 5: Xem trạng thái của git ( những file thư mục đã bị chỉnh sửa, xóa, thêm)
```sh
git status
```

![ima](../images/gitguide06.png)

- Bước 6: Do đây là repo rỗng chưa có gì nên ta sẽ thực hiện xác thực việc add các tệp và thư mục lên repo, sau đó check lại status.
```sh
git add -A
```
![ima](../images/gitguide07.png)

- Bước 7: Thực hiện commit thay đổi và Điền Message commit
```sh
git commit -a -m "<your_mess>"
```
![ima](../images/gitguide08.png)

- Bước 8: Thực hiện push lên github, có thể sẽ phải điền thông tin user, pass
```sh
git push
# có thể chỉ định branch muốn push
git push origin <your_branch>
```
![ima](../images/gitguide09.png)

## Thực hiện merge request vào nhánh Master

![ima](../images/gitmerge01.png)

![ima](../images/gitmerge02.png)

![ima](../images/gitmerge03.png)

![ima](../images/gitmerge04.png)
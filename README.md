# BaiTapThayHay
DoPhucTapCuaThuatToan
Bài 1: 
Dịch nghĩa
Xem xét thuật toán sau
/// Đầu vào Một số nguyên không âm n

a. Thuật toán này tính toán những gì?
b. Những gì nó phép toán cơ bản của thuật toán?
c. Hoạt động cơ bản được thực hiện bao nhiêu lần?
d. Lớp hiệu quả của thuật toán này là gì?
e. Đề xuất một cải tiến hoặc một thuật toán tốt hơn hoàn toàn và chỉ ra lớp hiệu quả của nó. Nếu bạn không làm được, hãy cố gắng chứng minh rằng, thực tế là không thể làm được

a, Thuật toán này trả ra tổng của bình phương các số từ 1 đến n
VD:      n = 3 thì S = 1*1+2*2+3*3 = 14

b, Các phép toán cơ bản là gán,so sánh, cộng và nhân

c, Số lần thực thiện
		Algorithm my stery(n) 				   #operations
S ←- 0							                      1
for i←- 1 to n do				                 2+n
			S   ←- S + i * i	                 2n
return S						                      1
						Total   6n+4
Dòng 1: Khởi tạo biến S là 1 phép toán, gán giá trị cho biến S là 1 phép toán => sum = 1
Dòng thứ 2:
+) Đầu tiên là có 1 phép gán và phép cộng=> sum = 2
+) Vòng lặp được thực hiện n lần 	=> sum =2n
+) Hết 1 lần lặp thì được kiểm tra mỗi lần (phép so sánh i<n) => sum=1
+) Kết thúc vòng lặp thì được n + 1 lần (n thành công 1 lần thất bại) => sum = n+1
=> sum = 4n+1
Dòng thứ 3:
	+) Thực hiện phép :+,* => sum = 2
	+) Thực hiện n lần lặp => sum =2n
Dòng thứ 4: Trả ra kết quả => sum =1 
⇒	Total = 1+4n+1+1+2n=6n+3

d, Thuật toán này có thể đúng mọi trường hợp với tham số đầu vào là số nguyên dương không âm

e,  Vì tham số đầu vào là số nguyên không âm cho nên giá trị có thể chạy từ 0,....n
Nếu ta dùng vòng if để kiểm tra các trường hợp nếu n == 0 thì ta sẽ thực hiện gán giá trị luôn thì các công việc ở trong vòng lặp sẽ được giảm đi 1 lần. 1 lần thực hiện n lần là số bước không nhỏ


VD: 
Algorithm mysterybetter(n) 				   #operations
S 						                          1
if n<1 then					                    1
  S= 0					                        1
else then:					
  S=1					                          1
  for i←- 2 to n do		                  2n
				S   ←- S + i * i	              2n
 return S					1
					Total 	6n
Dòng 1: Khai báo biến S nhưng chưa gán giá trị => sum =1
Dòng 2: So sánh tham số đầu vào bằng 0 thì thực hiện dòng 3 => sum =1
Dòng 3: Gán giá trị cần trả bằng 0 => sum = 1
Dòng 5: Gán giá trị cần trả bằng 1 => sum =1
Dòng 6: 
	+) Đầu tiên là có hoạt động là 1 phép cộng và phép gán=> sum = 1
  +) Vòng lặp được thực hiện n - 1 lần => sum = n
  +) Hết 1 lần lặp thì được kiểm tra mỗi lần (phép so sánh i<n) => sum=1
  +) Kết thúc vòng lặp thì được(n - 1) + 1 lần (n-1 thành công và 1 lần thất bại) => sum = n
 => sum = 2n
Dòng 7:
	+) Thực hiện phép :+,*  => sum = 2
	+) Thực hiện n-1 lần lặp => sum =2(n-1)
  => sum = 2(n-1)
Dòng 8: Trả ra kết quả 
⇒	Total = 1+1+1+1+2n+n+2(n-1)+1 = 6n


--------------------
Bài 2: 
Algorithm Sercet(A[0...n-1])
// Input mảng có n phần tử
minval ←-A[0];
maxval ←-A[0];
for i←-1 to n-1 do
	if A[i]<minval
		minval←-A[i]
	if A[i]>maxval
		maxval ←-A[i]
return minval,maxval

a, Thuật toán này tính toán ra giá trị lớn nhất, nhỏ nhất của 1 mảng truyền vào

b, Các phép toán cơ bản so sánh, gán

c, Hoạt động cơ bản thực hiện 
Dòng 1: Khởi tạo biến minval và gán giá trị cho nó => sum = 2
Dòng 2: Khởi tạo biến maxval và gán giá trị cho nó => sum = 2
Dòng 3: 
+) Đầu tiên là có 2 hoạt động là 1 phép cộng và 1 phép gán => sum = 2
+) Vòng lặp được thực hiện n - 1 lần => sum =2(n-1)
+) Hết 1 lần lặp thì được kiểm tra mỗi lần (phép so sánh i<n) => sum=1
+) Kết thúc vòng lặp thì được(n - 1) + 1 lần (n-1 thành công và 1 lần thất bại)
 => sum = n
Dòng 4:
	+) Truy xuất giá trị của A[i] và so sánh với minval => sum =2
	+) Được thực hiện n-1 lần => sum = 2(n-1)
Dòng 5:
	+) Truy xuất giá trị của A[i] và gán cho biến minval => sum =2
	+) Được thực hiện n-1 lần => sum = 2(n-1)
Dòng 6,7: tương tự dòng 4,5 : sum = 2(n-1) + 2(n-1) = 4(n-1)
Dòng 8: Trả về 2 biến sum = 2

⇒	Total = 2+2+2(n-1)+n+4(n-1) + 4(n-1) +2 = 11n-4

d, Ưu điểm của thuật toán
Dễ hiểu và phổ cập cho sinh viên
e, 








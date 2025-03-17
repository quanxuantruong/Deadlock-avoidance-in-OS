# Deadlock-avoidance-in-OS  
Note: Input banker nằm trong file inputbanker.txt  
      Input thuật toán nhận diện nằm trong file input.txt  
=> Kết quả chạy đã có trong các file  
# Thuật toán banker

1. Work và Finish là hai mảng có độ dài m và n. Khởi tạo:  
Work = Available  
Finish [i] = false với i = 0, 1, ..., n- 1  
2. Tìm i sao cho thoả mãn  
(a) Finish [i] = false  
(b) Needi ≤ Work  
Nếu không có i thoả mãn, chuyển sang bước 4  
3. Work = Work + Allocation[i]  
Finish[i] = true  
Chuyển sang bước 2  
4. Nếu Finish [i] == true với tất cả i, thì hệ thống ở trạng thái an toàn

# Thuật toán nhận diện

1. Work và Finish là hai mảng có độ dài m và n. Khởi tạo:  
(a) Work = Available  
(b) Với i = 0, 1, ..., n- 1, nếu Allocationi ≠ 0 thì Finish [i] = false, ngược lại Finish[i] = true  
2. Tìm i sao cho thoả mãn  
(a) Finish [i] = false  
(b) Requesti ≤ Work  
Nếu không có i thoả mãn, chuyển sang bước 4  
3. Work = Work + Allocation[i]  
Finish[i] = true  
Chuyển sang bước 2  
4. Nếu Finish [i] == false với một số 0 ≤ i ≤ n-1, thì hệ thống ở trạng thái bế tắc.  
Và nếu Finish [i] == false thì Pi bị bế tắc

## Bài 1
In ra các số nguyên tố trong khoảng từ 5 đến 100

## Bài 2

Khai báo danh sách gồm 4 các user biết mỗi user gồm các thuộc tính 
```python
    ID
    Tên
    Tuổi
    Giới tính 
```

- Hiển thị những user có giới tính là nam
- Sắp sếp danh sách các user theo tuổi giảm dần


## Lời giải bài 1

### cách 1
```python

for i in range(5, 101):
    couter = 0
    for j in range(2, i):
        if i%j==0:
            couter += 1
    if couter == 2:
        print(i)


```
### cách 2
- tự nghĩ thêm nha còn nhiều cách lắm, ví dụ thay vì duyệt từ 2-i có thể duyệt từ 2- sqrt(i)

## bài 2

Tạm ổn, nhưng mà thấy có vẻ vẫn phức tạm hóa vấn đề :3 
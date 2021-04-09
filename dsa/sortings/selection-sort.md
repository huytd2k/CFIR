# Selection Sort

## Ý tưởng

Liên tục tìm kiếm phần tử nhỏ nhất và đẩy lên lên đầu

## Độ phức tạp

- Thời gian : 
  - Best case: O( n^2 ) (Luôn phải trarvese mảng ~ n^2 ops)
  - Average case: O(n^2)
  - Worst case: O(n^2)
- Không gian: O(1)

## Note

- Luôn cần ít hơn hoặc bằng n lần swap 2 phần từ => hữu dụng khi thao tác swap tốn kém
- Không ổn định (Nhưng có thể sửa thuật toán để trở nên ổn định)

## Implement (Python)

```python
# Với lần duyệt từ phần tử i
for i in range(len(A)):
    # Min lần duyệt hiện tại  
    min_idx = i
    for j in range(i+1, len(A)):
        if A[min_idx] > A[j]:
            min_idx = j
              
    # Đổi vị trí với phần từ i  
    A[i], A[min_idx] = A[min_idx], A[i]
```


# Bubble Sort

## Ý tưởng

Liên tục đổi chỗ 2 phần tử nếu chúng không đúng thứ tự, nếu trong một lần duyệt không cần đổi chỗ phần tử nào => mảng đã được sắp xếp.

Thuật toán sắp xếp ổn định (stable).

## Độ phức tạp 

- Thời gian:
  - Tốt nhất: O(n) (Duyệt một lần và không cần đổi chỗ phần tử nào)
  - Trung bình: O(n^2).
  - Tồi nhất: O(n^2).
- Không gian: O(1)

## Implement (Python)

```python
def bubbleSort(arr):
    n = len(arr)
    for i in range(n):
        swapped = False
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1] :
                arr[j], arr[j+1] = arr[j+1], arr[j]
                swapped = True
        if swapped == False:
            break
```


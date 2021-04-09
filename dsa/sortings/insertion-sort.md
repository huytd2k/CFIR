# Insertion Sort

## Ý tưởng

Chia mảng thành 2 phần: phần đã được sắp xếp và phần chưa được sắp xếp, mỗi lần duyệt sẽ insert một phần tử chưa được sắp xếp vào phần đã được sắp xếp.

## Ví dụ

(example)[https://media.geeksforgeeks.org/wp-content/uploads/insertionsort.png]

## Độ phức tạp

- Thời gian:
  - Tốt nhất: O(n) (Không cần thực hiện lần insert nào)
  - Trung bình và tệ nhất: O(n^2)

- Không gian: O(1)

## Note

- Thuật toán ổn định
- Có thể hữu dụng khi mảng đã gần được sắp xếp

## Implement (Python)

```python
def insertionSort(arr):
    for i in range(1, len(arr)):
        key = arr[i]
        j = i-1
        while j >= 0 and key < arr[j] :
                arr[j + 1] = arr[j]
                j -= 1
        arr[j + 1] = key
```


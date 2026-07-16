# -Time-Slot-Consolidation-Problem-Statement-
https://www.programiz.com/online-compiler/2udVmSNlTHUr3

n = int(input("Enter number of intervals: "))

intervals = []


for i in range(n):
    start, end = map(int, input(f"Enter interval {i+1} (start end): ").split())
    intervals.append([start, end])

----------------------------------------------------------------------------------
#  Maximum Signal Strength Problem Statement
https://www.programiz.com/python-programming/online-compiler/


n = int(input())

arr = list(map(int, input().split()))

k = int(input())

current_sum = sum(arr[:k])
max_sum = current_sum

for i in range(k, n):
    current_sum = current_sum + arr[i] - arr[i-k]
    if current_sum > max_sum:
        max_sum = current_sum

print(max_sum)


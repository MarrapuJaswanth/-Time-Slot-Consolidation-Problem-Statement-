# -Time-Slot-Consolidation-Problem-Statement-
Link: https://www.programiz.com/online-compiler/2udVmSNlTHUr3

n = int(input("Enter number of intervals: "))

intervals = []


for i in range(n):
    start, end = map(int, input(f"Enter interval {i+1} (start end): ").split())
    intervals.append([start, end])

----------------------------------------------------------------------------------
#  Maximum Signal Strength Problem Statement
LInk: https://www.programiz.com/online-compiler/4DnfCWSdA0551


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

-----------------------------------------------------------------------------------------------
# Communication Channel Analyzer Problem Statement

Link: https://www.programiz.com/online-compiler/7V43suTIuGcfh

# Input string
s = input("Enter the string: ")

seen = set()
left = 0
max_len = 0

for right in range(len(s)):
    while s[right] in seen:
        seen.remove(s[left])
        left += 1

    seen.add(s[right])

    if right - left + 1 > max_len:
        max_len = right - left + 1

print(max_len)

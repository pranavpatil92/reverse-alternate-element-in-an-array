# Alternate Pair Swapping in C++

A beginner C++ program that demonstrates array manipulation using
index-based swapping and a two-pointer-style approach.

## 📌 Problem

Given an array, swap elements in alternate pairs.

Example:

Input:
1 2 3 4 5 6 7

Output:
2 1 4 3 6 5 7

## 🧠 Approach

The program uses two index variables:

- `start` — points to the first element of the current pair.
- `end` — points to the second element of the current pair.

The program swaps the elements at these positions and then moves
both indices forward to process the next pair.

## 💻 Code

```cpp
#include <iostream>

using namespace std;

int main() {
    int arr[] = {1, 2, 3, 4, 5, 6, 7};
    int n = 7;

    int start = 0;
    int end = n - 6;

    for (int i = 0; i < n; i++) {

        if (start < n && end < n) {
            swap(arr[start], arr[end]);

            start = start + 2;
            end = end + 2;
        }

        cout << arr[i];
    }

    return 0;
}
📤 Output
2143657
🔍 Example
Original:
1 2 3 4 5 6 7

Swap:
1 ↔ 2
3 ↔ 4
5 ↔ 6

Result:
2 1 4 3 6 5 7
📚 Concepts Practiced
C++ arrays
for loops
if conditions
Array indexing
swap()
Variables and pointer/index movement
Basic problem-solving and dry runs
⚠️ Note
This program is written as a learning exercise. The index initialization
is specific to the example and is not yet a generalized solution for
arrays of arbitrary sizes.
🚀 Future Improvements
Generalize the solution for arrays of any size.
Handle both even and odd-sized arrays.
Separate array processing from output.
Improve the index logic to avoid hard-coded values.

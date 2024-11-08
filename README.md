# EXPERIMENT 20
## AIM
To study and implement Sorting Algorithm

#### Selection sort
#### Insertion sort
#### Bubble sort
## SOFTWARE USED
VS Code

## THEORY
In C++, sorting refers to the process of arranging elements in a specific order, typically in ascending or descending order. Sorting algorithms can be applied to arrays, vectors, or other containers to reorder the elements based on their values.

### Selection Sort:
Selection Sort works by repeatedly finding the minimum element from the unsorted part of the array and swapping it with the first unsorted element.
Time Complexity: O(n²) for all cases.
Space Complexity: O(1) (in-place sorting).
insertionsort

## Insertion Sort:
Insertion Sort works by building a sorted array one element at a time. It picks each element and inserts it into its correct position within the already sorted part of the array.
Time Complexity: O(n²) in the worst case; O(n) in the best case (already sorted).
Space Complexity: O(1) (in-place sorting).
Selection-sort-0 Selection-sort-1 Selection-sort-2 Selection-sort-3_1
### Bubble Sort:
Bubble Sort repeatedly swaps adjacent elements if they are in the wrong order. The largest element "bubbles up" to its correct position after each pass.
Time Complexity: O(n²) in the worst case.
Space Complexity: O(1) (in-place sorting).
bubble_sort

## CODE & OUTPUT
## CODE A:
~~~
//soham
//entc B1
//23070123084
//experiment 20
#include<iostream>
using namespace std;

void swap(int *a, int *b) {
    int temp;
    temp = *a;
    *a = *b;
    *b = temp;
}

void s_sort(int *a, int elements) {
    int n = 0;
    int *b;

    while (n < elements) {
        b = a + 1;
        for (int i = 0; i < (elements - 1) - n; i++) {
            if (*a > *b) {
                swap(a, b);
            }
            b++;
        }
        n++;
        a++;
    }
}

int main() {
    int no_el;
    cout << "How many elements in your array?" << endl;
    cin >> no_el;
    int arr[no_el];

    cout << "Enter the elements of the array: " << endl;
    for (int i = 0; i < no_el; i++) {
        cin >> arr[i];
    }

    s_sort(arr, no_el);

    cout << "Sorted array: " << endl;
    for (int i = 0; i < no_el; i++) {
        cout << arr[i] << " ";
    }
    cout << endl;
    return 0;
}
~~~
## OUTPUT A:
![image](https://github.com/user-attachments/assets/5516efe2-f719-4ab8-9713-a4cc233f41ff)

## CODE B:
~~~
//soham
//entc B1
//2307012384
//experiment 20A
#include<iostream>
using namespace std;

void insertionSort(int arr[], int n) {
    for (int i = 1; i < n; i++) {
        int key = arr[i];
        int j = i - 1;

        // Move elements of arr[0..i-1], that are greater than key, to one position ahead of their current position
        while (j >= 0 && arr[j] > key) {
            arr[j + 1] = arr[j];
            j = j - 1;
        }
        arr[j + 1] = key;
    }
}

int main() {
    int n;
    cout << "How many elements in your array?" << endl;
    cin >> n;
    
    int arr[n];
    cout << "Enter the elements of the array: " << endl;
    for (int i = 0; i < n; i++) {
        cin >> arr[i];
    }

    insertionSort(arr, n);

    cout << "Sorted array: " << endl;
    for (int i = 0; i < n; i++) {
        cout << arr[i] << " ";
    }
    cout << endl;
    
    return 0;
}
~~~
## OUTPUT B:
![image](https://github.com/user-attachments/assets/7796e481-5a06-46ad-87e7-cbac82f32161)

## CODE C:
~~~
//soham
//entc B1
//23070123084
//experiment 20
#include<iostream>
using namespace std;

void swap(int *a, int *b) {
    int temp;
    temp = *a;
    *a = *b;
    *b = temp;
}

void bubbleSort(int *a, int elements) {
    int n = 0;
    int *b;

    while (n < elements) {
        b = a + 1;
        for (int i = 0; i < (elements - 1) - n; i++) {
            if (*a > *b) {
                swap(a, b);
            }
            b++;
        }
        n++;
        a++;
    }
}

int main() {
    int no_el;
    cout << "How many elements in your array?" << endl;
    cin >> no_el;

    int arr[no_el];
    cout << "Enter the elements of the array: " << endl;
    for (int i = 0; i < no_el; i++) {
        cin >> arr[i];
    }

    bubbleSort(arr, no_el);

    cout << "Sorted array: " << endl;
    for (int i = 0; i < no_el; i++) {
        cout << arr[i] << " ";
    }
    cout << endl;

    return 0;
}
~~~
## OUTPUT C:
Screenshot 2024-10-16 091221
## CONCLUSION:
These algorithms are primarily useful for educational purposes, and while they work well on small datasets, more advanced sorting algorithms such as Quick Sort, Merge Sort, or Heap Sort are generally preferred for large datasets due to their better performance

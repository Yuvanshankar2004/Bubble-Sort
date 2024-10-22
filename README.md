# Bubble-Sort
#include <stdio.h>

// Function to perform Bubble Sort
void bubbleSort(int array[], int size) {
    for (int step = 0; step < size - 1; ++step) {
        // Run the loop for each element of the array
        for (int i = 0; i < size - step - 1; ++i) {
            // Swap if the element found is greater than the next element
            if (array[i] > array[i + 1]) {
                int temp = array[i];
                array[i] = array[i + 1];
                array[i + 1] = temp;
            }
        }
    }
}

// Function to print the array
void printArray(int array[], int size) {
    for (int i = 0; i < size; ++i) {
        printf("%d ", array[i]);
    }
    printf("\n");
}

int main() {
    int size;
    
    // Input the size of the array
    printf("Enter the number of elements in the array: ");
    scanf("%d", &size);
    
    int array[size];

    // Input the array elements
    printf("Enter the elements of the array:\n");
    for (int i = 0; i < size; ++i) {
        scanf("%d", &array[i]);
    }

    // Sorting the array using Bubble Sort
    bubbleSort(array, size);

    // Output the sorted array
    printf("Sorted Array in Ascending Order:\n");
    printArray(array, size);

    return 0;
}

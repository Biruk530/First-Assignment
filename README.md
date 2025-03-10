/*Algorithm: Find the Smallest Number in a List
Initialize a variable min_value with the first element of the list.
Iterate through the list starting from the second element.
Compare each element with min_value:
If the current element is smaller than min_value, update min_value.
Return min_value after the loop ends.*/

#include <iostream>
using namespace std;

int findSmallest(int arr[], int size) {
    if (size == 0) return -1;  // Handle empty array case

    int min_value = arr[0];  // Assume first element is smallest

    for (int i = 1; i < size; i++) {
        if (arr[i] < min_value) {
            min_value = arr[i];  // Update min_value if smaller element found
        }
    }
    return min_value;
}

int main() {
    int numbers[] = {23, 71, 52, 17, -8, 13, -74};
    int size = sizeof(numbers) / sizeof(numbers[0]);

    cout << "Smallest number: " << findSmallest(numbers, size) << endl;
    return 0;
}

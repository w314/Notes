java, array
Array is FIXED size;

```java
// create array
int[] arr = new int[3];

// add element FIXED SIZE CANNOT ADD

// modify element
int[] arr1 = {4, 5, 6}
Arrays.fill(arr, 2);
arr[1] = 5;


// get element
int n = arr[2];

// remove element FIXED SIZE CANNOT REMOVE

// iterate over array
for(int n : arr) {
  System.out.println(n);
}

// length of array PROPERTY not method
int arrLength = arr.length;

// sort array
Arrays.sort(arr);

// search sorted array
int[] arr2 = {6, 9, 7};
// sort array first
Arrays.sort(arr2);
// returns index of element if found
int indFound = Arrays.binarySearch(arr2, 9); // returns 2
// returns (-(insertion point) - 1) if not found
int indNotFound = Arrays.binarySearch(arr2, 8); // returns -3


// compare array contents
boolean sameContent = Arrays.equals(arr1, arr2);


// print array
System.out.println(Arrays.toString(arr));

// array to ArrayList
// does not work with int[] to List<Integer>
String[] arr3 = {"bob", "bobek"};
List<String> arrList = new ArrayList<>(Arrays.asList(arr3));
// OR
List<string> arrList1 = new ArrayList<>();
Collections.addAll(arrList1,arr3);



```

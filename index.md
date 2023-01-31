# Lab Report Two for CSE 15L

## Part 1 : Making a String Server
***
## Part 2 : Listing a bug and its resolution 

### Failure inducing J unit 
```
@Test
  public void testReversed_improved() {
    int[] input1 = {};
    assertArrayEquals(new int[]{}, ArrayExamples.reversed(input1));
    int[] input2 = {1,2,3};
    assertArrayEquals(new int[]{3,2,1}, ArrayExamples.reversed(input2));
  }
```

### Non- Failure inducing J unit 
```
@Test
  public void testReversed() {
    int[] input1 = {};
    assertArrayEquals(new int[]{}, ArrayExamples.reversed(input1));
  }
```

### Symptoms - outputs of j unit tests
![][Symptom1.png]
![][Symptom2.png]

### Faulty code 
```
// Returns a *new* array with all the elements of the input array in reversed
  // order
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
 ```
### Correct Code
```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[i] = arr[arr.length - i - 1];
    }
    return newArray;
  }
 ```



***

## Part 3 : Learning from week 2 and week 3 Lab 
- One of the major takewayas from the lab work of the past two weeks was the newly acquired excellence in basic junit testing which will really help us out in any project work and even in reasearch to make sure our code has the utmost quality.

***
***

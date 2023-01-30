# Part 1: Writing a webserver




# Part 2: Explaining and fixing bugs
Failure inducing input (JUnit): ```
@Test public void myTestReverseInPlace() {
    int[] input1 = { 3, 2, 1, 0 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 0, 1, 2, 3}, input1);
	} ```
  
Failure inducing input (JUnit): ``` @Test
  public void myTestReversed() {
    int[] input1 = { 3, 2, 1, 0 };
    assertArrayEquals(new int[]{ 0, 1, 2, 3 }, ArrayExamples.reversed(input1));
  } ```
  
  
  Non Failure inducing input (JUnit): ``` @Test
  public void testReversed() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
  } ```
  
  Non Failure inducing input (JUnit): ``` @Test 
	public void testReverseInPlace() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
	} ```
  
  The symptoms:
  
  
  Before fixing the bugs in reverseInPlace(): ```
  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  } ```
  
  After fixing the bugs in reverseInPlace(): ```
  static void reverseInPlace(int[] arr) {
    int [] tempArr = new int[arr.length];
    for (int i = 0; i < tempArr.length; i++) {
      tempArr[i] = arr[i];
    }

    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = tempArr[arr.length - i - 1];
    }
  } ```
  
  What the bugs were in reverseInPlace() were: The issue with this code is that after it crosses the mid point of the array, it will start copying from the 
  already changed elements which will lead to an inaccurate reversed array. I fixed this by making an entirely new array and making a deep copy of that. 
  After that, I reversed from the deep copied array so that the elements don't change.
  
  
  Before fixing the bugs in reversed(): ```
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];

    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  } ```
  
  After fixing the bugs in reversed(): ``` 
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];

    for(int i = 0; i < arr.length; i += 1) {
      newArray[i] = arr[arr.length - i - 1];
    }
    return newArray;
  } ```
  
  What the bugs were in reversed(): The bugs with this code was that it created newArray with the same length as array but no elements because It didn't copy the elements. After that it proceeded to copy null elements into the original array then returned the original array. I fixed the code by copying the elements in reverse order into newArray then returned the new reversed array.
  
  
  
  
  
  
  
  
  # Part 3: What I learned from lab in weeks 2 & 3
  
  
  
  
  
  
  

# Lab Report 2, Week 4

## Part 1: 



## Part 2: Bugs
* The method that I have chosen to focus on is the "reversed" method in the ArrayExamples class.
The method is written as follows: 
```
static int[] reversed(int[] arr) {
  int[] newArray = new int[arr.length];
  for(int i = 0; i < arr.length; i += 1) {
    arr[i] = newArray[arr.length - i - 1];
  }
  return arr;
}
```
* The given JUnit test did not fail:
```
@Test
public void testReversed() {
  int[] input1 = { };
  assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1);
}
```
* However, when I wrote my own test for this method, it failed:
```
@Test
public void testReversed2() {
  int[] input = {1,2,3,4};
  assertArrayEquals(new int[]{4,3,2,1}, ArrayExamples.reversed(input));
}
* Here is a picture displaying that the first JUnit test has passed, while the second test has failed:
![Image](TestReversed.png)

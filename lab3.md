### Bugs and Commands

## Part 1: Bugs

```
// Failure Inducing Input for Buggy Program

  @Test
  public void testReverse2() {
    int[] input1 = {4,3,2,1};
    int[] output1 = ArrayExamples.reversed(input1);
    assertArrayEquals(new int[] {1,2,3,4}, output1);
  }
```
```
// Input that Doesn't Induce a Failure

  @Test
  public void testReverse3() {
    int[] input1 = {0,0,0,0};
    int[] output1 = ArrayExamples.reversed(input1);
    assertArrayEquals(new int[] {0,0,0,0}, output1);
  }
```

`Symptom of Output of Running the Test`

<img width="664" alt="Screen Shot 2023-11-03 at 3 43 50 PM" src="https://github.com/shinaegyo/cse15l-lab3/assets/137027086/f66513e7-4281-415b-8690-cc79308c7092">


`Before`

<img width="377" alt="Screen Shot 2023-11-03 at 3 37 59 PM" src="https://github.com/shinaegyo/cse15l-lab3/assets/137027086/d43f5271-5070-4832-a039-83b0d0641cab">


`After`

<img width="379" alt="Screen Shot 2023-11-03 at 3 38 31 PM" src="https://github.com/shinaegyo/cse15l-lab3/assets/137027086/8520eb28-5902-45f9-9ec8-51af60c33ed1">


This addresses the issue because the test case `testReverse2` expected value for it to pass can only be {0,0,0,0} and no positive values. This is because the newArray object that was created sets every index value to 0 and setting arr[i] = to newArray times anything will set the indexes of arr[i] to 0. Therefore, setting newArray[i] = arr[arr.length - i - 1] will also set up a new array and reverse the order of the original array with no errors.

## Part 2: Researching Commands


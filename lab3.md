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

`-depth`

<img width="555" alt="Screen Shot 2023-11-04 at 6 57 30 PM" src="https://github.com/shinaegyo/cse15l-lab3/assets/137027086/4859ee20-129b-44c1-8b6c-b1a915468ca7">
<img width="540" alt="Screen Shot 2023-11-04 at 6 58 07 PM" src="https://github.com/shinaegyo/cse15l-lab3/assets/137027086/b81fb189-0393-4984-aa97-ee71b0c7d8d6">

`-name option`

<img width="532" alt="Screen Shot 2023-11-04 at 6 20 17 PM" src="https://github.com/shinaegyo/cse15l-lab3/assets/137027086/d4f24ca5-2cdf-4552-a381-e7467ef151ce">
<img width="636" alt="Screen Shot 2023-11-04 at 6 20 09 PM" src="https://github.com/shinaegyo/cse15l-lab3/assets/137027086/35317d75-900d-46a0-b314-526e89b8fa83">

`type option`

<img width="473" alt="-type d" src="https://github.com/shinaegyo/cse15l-lab3/assets/137027086/6dbf53d4-9ac1-4d0e-909f-cf19213af80b">
<img width="470" alt="-type f" src="https://github.com/shinaegyo/cse15l-lab3/assets/137027086/acf133c0-6185-4ded-9ac6-840ffccb05af">

`print option`

<img width="570" alt="-print option1" src="https://github.com/shinaegyo/cse15l-lab3/assets/137027086/d9b2b49e-bdca-47fc-954a-e02e2b7c44fe">
<img width="728" alt="-print option2" src="https://github.com/shinaegyo/cse15l-lab3/assets/137027086/335ad9b5-020a-4220-ab03-effedbc30855">


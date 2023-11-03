### Bugs and Commands

## Part 1: Bugs

`Failure Inducing Input for Buggy Program`

@Test
  public void testReverse2() {
    int[] input1 = {4,3,2,1};
    int[] output1 = ArrayExamples.reversed(input1);
    assertArrayEquals(new int[] {1,3,4,2}, output1);
  }

`Input that Doesn't Induce a Failure`

@Test
  public void testReverse3() {
    int[] input1 = {4,5,6,7};
    int[] output1 = ArrayExamples.reversed(input1);
    assertArrayEquals(new int[] {7,6,5,4}, output1);
  }

`Symptom of Output of Running the Test`
<img width="681" alt="Screen Shot 2023-11-03 at 3 21 24 PM" src="https://github.com/shinaegyo/cse15l-lab3/assets/137027086/287b0238-251a-4b48-8ce0-ad9ca3febd35">

`Before`

<img width="482" alt="Screen Shot 2023-11-03 at 3 22 36 PM" src="https://github.com/shinaegyo/cse15l-lab3/assets/137027086/de57f545-498c-4b21-8e25-48b934748ad2">

`After`

<img width="491" alt="Screen Shot 2023-11-03 at 3 22 52 PM" src="https://github.com/shinaegyo/cse15l-lab3/assets/137027086/f6c4ef9b-c4a3-482e-a61c-6bcf171f06f6">

This addresses the issue because the test case `testReverse2` expected value was supposed to be {1,2,3,4} but it was set to {1,3,4,2}. As we swapped the expected value to be the same as the actual value, it resulted in no failing test cases.

## Part 2: Researching Commands


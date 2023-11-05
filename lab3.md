# **LAB REPORT 3**

***
PART I
***

  * Failure inducing input:
  * ```java
    @Test
    public void averageWithoutLowest2(){
      double[] arr =  {2.2,2.2,2.2,2.2};
      assertEquals(2.2, ArrayExamples.averageWithoutLowest(arr), 0.0001);
    }
    ```
  * ![Image](lab3_code1.png)

  * No Failure inducing input:
  * ```java
    @Test
    public void averageWithoutLowest(){
      double[] arr =  {2.2,3.4,5.7,1.1,1.0};
      assertEquals(3.1, ArrayExamples.averageWithoutLowest(arr), 0.0001);
    }
    ```
  * ![Image](lab3_code2.png)

  * Before:
  * ![Image](lab3_code3.png)
  * After:
  * ![Image](lab3_code4.png)

  * Fixes report:
    * The fix I made was to add in a scenario where the array had multiple doubles that were all equal to each other. The code in the before image did not take into account that the elements in the array could all be equal to each other, therefore when the code ran, it was not able to give the right average. (which was equal to any single double element in the array)
   
***
PART II
***

(Source: https://man7.org/linux/man-pages/man1/find.1.html)

 * Command: `find`
 * Option 1: `-print`
   * Ex 1: This finds the file `TestDocSearch.java` and prints out its location.
   * ![Image](lab3_code5.png)
  
   * Ex 2: This finds the file `chapter-1.txt` and prints out its location.
   * ![Image](lab3_code5.png)
 * Option 2:  `-ls`
   * Ex 1: This finds and lists out all the files in the 911report directory (ie working directory) and lists them out in ls -dils format.
   * ![Image](lab3_code7.png)
  
   * Ex 2: This finds a specfic file called `chapter-2.txt` in the 911 report directory and lists it out in ls -dils format.
   * ![Image](lab3_code8.png)
 * Option 3: `-prune`
   * Ex 1: This finds and prints out everything (including directories) except for anything in and under the biomed directory. We use `-prune` to do that part. (Note: there are too many files, hence why the screenshot is limited)
   * ![Image](lab3_code9.png)
  
   * Ex 2: This finds and prints out everything (including directories) except for anything in and under the technical directory. We use `-prune` to do that part. (Note: there are too many files, hence why the screenshot is limited)
   * ![Image](lab3_code10.png)
 * Option 4: `-delete`
   * 
  
























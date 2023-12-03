# **LAB REPORT 5**

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
   * ```
     [user@sahara ~]$ find -name "TestDocSearch.java" -print
     ./docsearch/TestDocSearch.java
     ```
     
   * Ex 2: This finds the file `chapter-1.txt` and prints out its location.
   * ```
     [user@sahara ~]$ find -name "chapter-1.txt" -print
     ./docsearch/technical/911report/chapter-1.txt
     ```
 * Option 2:  `-ls`
   * Ex 1: This finds and lists out all the files in the 911report directory (ie working directory) and lists them out in ls -dils format. (too many files to list...)
   * ```
     [user@sahara ~/docsearch/technical/911report]$ find -ls
      35663080      4 drwxr-xr-x   2 user     user         4096 Nov  5 20:20 .
      35664249     88 -rwxr-xr-x   1 user     user        89854 Nov  5 20:20 ./chapter-13.1.txt
      35664258    148 -rwxr-xr-x   1 user     user       149063 Nov  5 20:20 ./chapter-6.txt
      35664250    108 -rwxr-xr-x   1 user     user       110568 Nov  5 20:20 ./chapter-13.2.txt
      35664256    100 -rwxr-xr-x   1 user     user        99008 Nov  5 20:20 ./chapter-5.txt
      35664245    116 -rwxr-xr-x   1 user     user       118656 Nov  5 20:20 ./chapter-1.txt
      35664251    148 -rwxr-xr-x   1 user     user       150467 Nov  5 20:20 ./chapter-13.3.txt
      35664248    128 -rwxr-xr-x   1 user     user       127587 Nov  5 20:20 ./chapter-12.txt
      35664247     72 -rwxr-xr-x   1 user     user        71151 Nov  5 20:20 ./chapter-11.txt
      35664253    288 -rwxr-xr-x   1 user     user       290993 Nov  5 20:20 ./chapter-13.5.txt
      35664252    260 -rwxr-xr-x   1 user     user       265912 Nov  5 20:20 ./chapter-13.4.txt
      35664263     84 -rwxr-xr-x   1 user     user        84835 Nov  5 20:20 ./chapter-8.txt
      35664246     48 -rwxr-xr-x   1 user     user        47307 Nov  5 20:20 ./chapter-10.txt
      35664262    128 -rwxr-xr-x   1 user     user       128370 Nov  5 20:20 ./chapter-7.txt
      35664254     80 -rwxr-xr-x   1 user     user        79803 Nov  5 20:20 ./chapter-2.txt
      35664267     12 -rwxr-xr-x   1 user     user         9332 Nov  5 20:20 ./preface.txt
      35664264    148 -rwxr-xr-x   1 user     user       149644 Nov  5 20:20 ./chapter-9.txt
      35664255    260 -rwxr-xr-x   1 user     user       264360 Nov  5 20:20 ./chapter-3.txt
     ```
  
   * Ex 2: This finds a specfic file called `chapter-2.txt` in the 911 report directory and lists it out in ls -dils format.
   * ```
     [user@sahara ~/docsearch/technical/911report]$ find -name "chapter-2.txt" -ls
      35664254     80 -rwxr-xr-x   1 user     user        79803 Nov  5 20:20 ./chapter-2.txt
     ```
 * Option 3: `-prune`
   * Ex 1: This finds and prints out everything (including directories) except for anything in and under the biomed directory. We use `-prune` to do that part. (Note: there are too many files, hence why the screenshot is limited)
   * ```
     [user@sahara ~/docsearch]$ find . -path ./technical/biomed -prune -o -print
     .
     ./technical
     ./technical/911report
     ./technical/911report/chapter-13.1.txt
     ./technical/911report/chapter-6.txt
     ./technical/911report/chapter-13.2.txt
     ./technical/911report/chapter-5.txt
     ./technical/911report/chapter-1.txt
     ```
  
   * Ex 2: This finds and prints out everything (including directories) except for anything in and under the technical directory. We use `-prune` to do that part. (Note: there are too many files, hence why the screenshot is limited)
   * ```
     [user@sahara ~/docsearch]$ find . -path ./technical -prune -o -print
     .
     ./TestDocSearch.java
     ./DocSearchServer.java
     ./lib
     ./lib/junit-4.13.2.jar
     ./lib/hamcrest-core-1.3.jar
     ./Server.java
     ./README.md
     ./.git
     ```
 * Option 4: `-delete`
   * Ex 1: This deletes all `"*.txt"` files in the technical directory.
   * ```
     [user@sahara ~/docsearch/technical]$ find . -name "*.txt" -delete
     [user@sahara ~/docsearch/technical]$ cd biomed
     [user@sahara ~/docsearch/technical/biomed]$ tree
     .

     0 directories, 0 files
     [user@sahara ~/docsearch/technical/biomed]$ cd ../
     [user@sahara ~/docsearch/technical]$ cd 911report
     [user@sahara ~/docsearch/technical/911report]$ tree
     .

     0 directories, 0 files
     [user@sahara ~/docsearch/technical/911report]$
     ```
   * Ex 2: This deletes all `"*.jar"` files in the lib directory.
   * ```
     [user@sahara ~/docsearch/lib]$ find . -name "*.jar" -delete
     [user@sahara ~/docsearch/lib]$ tree
     .

     0 directories, 0 files
     ```
  
























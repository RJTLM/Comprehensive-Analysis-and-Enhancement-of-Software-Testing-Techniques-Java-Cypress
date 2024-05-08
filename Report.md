# CMPE3008 Software Engineering Testing - Group Assignment

## **Predictive Pioneers**

## Team Members

<details>
  <summary>Click to view team members:</summary>
  <p><p>Member 1: Elizaveta Rassell, 17904982</p>
  <p>Member 2: Mitchell Pontague, 19126924</p>
  <p>Member 3: Ryan Mackintosh, 21171466</p></p>
</details>

## Chosen Code Project Details

### Source Location (3 Marks)

- **Repository URL:** [sorting-algorithms by murraco](https://github.com/murraco/sorting-algorithms)
- **Access Date:** 2 May 2024

### Chosen Methods

Describe the chosen methods here, including why they were selected based on the assignment criteria.

#### Method 1: Bubble Sort

- **Description:** [Brief description of what this method does]
- **Source File Location:** [src/main/java/murraco/BubbleSort.java](https://github.com/murraco/sorting-algorithms/blob/master/src/main/java/murraco/BubbleSort.java)

  <details>
  <summary><strong>Click to view the BubbleSort Source Code:</strong></summary>

  ```java
  package murraco;

  public class BubbleSort {

    // Time complexity: average O(n^2) and best O(n) - Space complexity: O(1)
    public static <T extends Comparable<T>> void bubbleSort(T[] arr) {
      for (int i = 0; i < arr.length - 1; i++) {
        for (int j = 1; j < arr.length; j++) {
          if (arr[j].compareTo(arr[j - 1]) < 0) {
            T temp = arr[j];
            arr[j] = arr[j - 1];
            arr[j - 1] = temp;
          }
        }
      }
    }
  }
  ```

  </details>

- **Test File Location:** [src/test/java/murraco/SortingAlgorithmsTest.java](https://github.com/murraco/sorting-algorithms/blob/master/src/test/java/murraco/SortingAlgorithmsTest.java)

  <details>
  <summary><strong>Click to view the BubbleSort Test Code:</strong></summary>

  ```java
  package murraco;

  import static org.junit.Assert.assertEquals;

  import java.util.Arrays;

  import org.junit.Test;

  import murraco.BubbleSort;
  import murraco.Heapsort;
  import murraco.InsertionSort;
  import murraco.MergeSort;
  import murraco.Quicksort;
  import murraco.SelectionSort;

  public class SortingAlgorithmsTest {

    @Test
    public void testBubbleSort() {
        final Integer[] data = {4, 3, 0, 11, 7, 5, 15, 12, 99, 1};
        BubbleSort.bubbleSort(data);
        assertEquals("[0, 1, 3, 4, 5, 7, 11, 12, 15, 99]", Arrays.toString(data));
    }

    @Test
    public void testInsertionSort() {
        final Integer[] data = {4, 3, 0, 11, 7, 5, 15, 12, 99, 1};
        InsertionSort.insertionSort(data);
        assertEquals("[0, 1, 3, 4, 5, 7, 11, 12, 15, 99]", Arrays.toString(data));
    }

    @Test
    public void testSelectionSort() {
        final Integer[] data = {4, 3, 0, 11, 7, 5, 15, 12, 99, 1};
        SelectionSort.selectionSort(data);
        assertEquals("[0, 1, 3, 4, 5, 7, 11, 12, 15, 99]", Arrays.toString(data));
    }

    @Test
    public void testMergeSort() {
        final Integer[] data = {4, 3, 0, 11, 7, 5, 15, 12, 99, 1};
        MergeSort.mergeSort(data);
        assertEquals("[0, 1, 3, 4, 5, 7, 11, 12, 15, 99]", Arrays.toString(data));
    }

    @Test
    public void testHeapsort() {
        final Integer[] data = {4, 3, 0, 11, 7, 5, 15, 12, 99, 1};
        Heapsort.heapSort(data);
        assertEquals("[0, 1, 3, 4, 5, 7, 11, 12, 15, 99]", Arrays.toString(data));
    }

    @Test
    public void testQuicksort() {
        final Integer[] data = {4, 3, 0, 11, 7, 5, 15, 12, 99, 1};
        Quicksort.quickSort(data);
        assertEquals("[0, 1, 3, 4, 5, 7, 11, 12, 15, 99]", Arrays.toString(data));
    }
  }
  ```

  </details>

#### Method 2: Insertion Sort

- **Description:** [Brief description of what this method does]
- **Source File Location:** [src/main/java/murraco/InsertionSort.java](https://github.com/murraco/sorting-algorithms/blob/master/src/main/java/murraco/InsertionSort.java)

  <details>
  <summary><strong>Click to view the InsertionSort Source Code:</strong></summary>

  ```java
  package murraco;

  public class InsertionSort {

    // Time complexity: average O(n^2) and best O(n) - Space complexity: O(1)
    public static <T extends Comparable<T>> void insertionSort(T[] arr) {
      for (int i = 0; i < arr.length; i++) {
        T temp = arr[i];
        int j = i;
        while (j > 0 && arr[j - 1].compareTo(temp) > 0) {
          arr[j] = arr[j - 1];
          j--;
        }
        arr[j] = temp;
      }
    }

  }
  ```

  </details>

- **Test File Location:** [src/test/java/murraco/SortingAlgorithmsTest.java](https://github.com/murraco/sorting-algorithms/blob/master/src/test/java/murraco/SortingAlgorithmsTest.java)

  <details>
  <summary><strong>Click to view the InsertionSort Test Code:</strong></summary>

  ```java
  package murraco;

  import static org.junit.Assert.assertEquals;

  import java.util.Arrays;

  import org.junit.Test;

  import murraco.BubbleSort;
  import murraco.Heapsort;
  import murraco.InsertionSort;
  import murraco.MergeSort;
  import murraco.Quicksort;
  import murraco.SelectionSort;

  public class SortingAlgorithmsTest {

    @Test
    public void testBubbleSort() {
        final Integer[] data = {4, 3, 0, 11, 7, 5, 15, 12, 99, 1};
        BubbleSort.bubbleSort(data);
        assertEquals("[0, 1, 3, 4, 5, 7, 11, 12, 15, 99]", Arrays.toString(data));
    }

    @Test
    public void testInsertionSort() {
        final Integer[] data = {4, 3, 0, 11, 7, 5, 15, 12, 99, 1};
        InsertionSort.insertionSort(data);
        assertEquals("[0, 1, 3, 4, 5, 7, 11, 12, 15, 99]", Arrays.toString(data));
    }

    @Test
    public void testSelectionSort() {
        final Integer[] data = {4, 3, 0, 11, 7, 5, 15, 12, 99, 1};
        SelectionSort.selectionSort(data);
        assertEquals("[0, 1, 3, 4, 5, 7, 11, 12, 15, 99]", Arrays.toString(data));
    }

    @Test
    public void testMergeSort() {
        final Integer[] data = {4, 3, 0, 11, 7, 5, 15, 12, 99, 1};
        MergeSort.mergeSort(data);
        assertEquals("[0, 1, 3, 4, 5, 7, 11, 12, 15, 99]", Arrays.toString(data));
    }

    @Test
    public void testHeapsort() {
        final Integer[] data = {4, 3, 0, 11, 7, 5, 15, 12, 99, 1};
        Heapsort.heapSort(data);
        assertEquals("[0, 1, 3, 4, 5, 7, 11, 12, 15, 99]", Arrays.toString(data));
    }

    @Test
    public void testQuicksort() {
        final Integer[] data = {4, 3, 0, 11, 7, 5, 15, 12, 99, 1};
        Quicksort.quickSort(data);
        assertEquals("[0, 1, 3, 4, 5, 7, 11, 12, 15, 99]", Arrays.toString(data));
    }
  }
  ```

  </details>

## Coverage Analysis

### Method Graphs

Include diagrams and descriptions of the converted method graphs here.

#### Graph for Method 1: BubbleSort

![BubbleSort Graph Image](Content\BubbleFlowChart.png)

#### Graph for Method 2: InsertionSort

![Graph Image](path/to/graph2.png)

### Prime Path Coverage (10 Marks)

Discuss your prime path coverage analysis for each method.

## Method 1: BubbleSort Test Coverage Analysis

### Test Requirements (TR)

#### Level 0 (L0)

- [1]
- [2]
- [5]
- [3]
- [4]

#### Level 1 (L1)

- [1,2]
- [1,5]
- [2,1]
- [2,3]
- [3,4]
- [3,2]
- [4,2]

#### Level 2 (L2)

- [1,2,1]
- [1,2,3]
- [1,5]
- [2,1,2]
- [2,1,5]
- [2,3,4]
- [2,3,2]
- [3,4,2]
- [3,2,1]
- [3,2,3]
- [4,2,1]
- [4,2,3]

### Simple Paths

- [1,2]
- [1,5]
- [2,1]
- [2,3]
- [3,4]
- [3,2]
- [4,2]
- [1,2,1]
- [1,2,3]
- [2,1,2]
- [2,1,5]
- [2,3,4]
- [2,3,2]
- [3,4,2]
- [3,2,1]
- [3,2,3]
- [4,2,1]
- [4,2,3]
- [1,2,3,4]
- [2,3,4,2]
- [3,4,2,1]
- [3,4,2,3]
- [3,2,1,5]
- [4,2,1,5]
- [4,2,3,4]
- [3,4,2,1,5]

### Prime Paths

- [3,4,2,1,5]
- [2,3,4,2]
- [1,2,3,4]
- [3,4,2,3]
- [4,2,3,4]
- [3,2,1,5]
- [2,1,2]
- [1,2,1]
- [2,3,2]
- [3,2,3]

### Test Paths for Prime Path Coverage

| Test Paths                  | Test Requirements                                   |
|-----------------------------|-----------------------------------------------------|
| [1,2,3,2,3,2,1,5]           | [2,1,2], [1,2,1]                                    |
| [1,2,3,4,2,3,4,2,1,5]       | [3,4,2,1,5], [2,3,4,2], [1,2,3,4], [3,4,2,3], [4,2,3,4] |
| [1,2,3,4,2,3,2,1,5]         | [2,3,4,2], [1,2,3,4], [3,4,2,3], [3,2,1,5], [2,3,2]   |
| [1,2,3,2,3,2,1,5]           | [3,2,1,5], [2,3,2], [3,2,3]                          |

#### Method 2: InsertionSort

### Syntax-Based Testing Analysis (10 Marks)

Discuss the creation of mutants, mutation operators used, and the analysis of Reachability, Infection, and Propagation conditions.

#### Mutants for Method 1: BubbleSort

- **Mutant 1:** [Description]
- **Mutant 2:** [Description]

#### Mutants for Method 2: InsertionSort

- **Mutant 1:** [Description]
- **Mutant 2:** [Description]

## Test Method Analysis (5 Marks)

Evaluate the existing test methods against the mutants created and provide an opinion on the sufficiency of the tests.

### Analysis for Test Method 1: BubbleSort

- **Observations:** [Your observations]
- **Sufficiency of Testing:** [Your judgment]

### Analysis for Test Method 2: InsertionSort

- **Observations:** [Your observations]
- **Sufficiency of Testing:** [Your judgment]

## Testing Tool Investigation (10 Marks)

### Chosen Tool: Cypress

- **Purpose and Functionality:**
  Cypress is an all-in-one testing framework designed for modern web application testing. Its primary purpose is to simplify the process of setting up, writing, running, and debugging tests. Unlike many other testing tools, Cypress is built on a new architecture and runs in the same run-loop as the application being tested. This allows Cypress to offer native access to every object without the need for additional drivers or proxies, resulting in more reliable and faster tests.

- **Usage:**
  Cypress can be installed via npm and integrated directly into a project's development environment. It allows for writing tests in JavaScript. A typical test in Cypress might involve visiting a web page, querying for an element, interacting with that element, and asserting that the application state has changed as expected. Here’s a basic example:

  ```javascript
  describe('My First Test', () => {
    it('Does not do much!', () => {
      expect(true).to.equal(true);
    });
  });
  ```

  This framework is particularly user-friendly for developers already familiar with JavaScript and front-end frameworks.

- **Other Considerations:**
  Cypress has grown rapidly in popularity and is widely adopted in modern web development environments. It supports end-to-end testing, integration testing, and unit testing. One key consideration is that Cypress only supports JavaScript, which could be a limitation if your development team uses other programming languages. However, its direct access to both the front and back end of web applications allows for powerful and complex testing scenarios that are more difficult to achieve with other tools.

- **Recommendation:**
  We highly recommend Cypress for teams developing single-page applications and other complex web architectures, particularly those using modern JavaScript frameworks like React, Angular, or Vue. Its ease of use, combined with powerful testing capabilities and fast feedback loops, makes it an excellent tool for both developers and QA engineers aiming to implement rigorous testing practices.

## Presentation (7 Marks)

**Link to presentation slides:** [Insert link to Google Slides, PowerPoint Online, etc.]

**Outline of Presentation:**

- **Introduction to Cypress**
  - Overview and significance in testing.
- **Purpose and Functionality**
  - Detailed discussion on what Cypress is and what it can do.
- **How to Use Cypress**
  - Demonstrating setup and simple test examples.
- **Advantages and Considerations**
  - Exploring the benefits and potential limitations of using Cypress.
- **Case Studies**
  - Examples of successful implementations and the impact on development.
- **Conclusion and Recommendation**
  - Summarizing why Cypress might be the right choice for your team or project.

## Report Summary

In our investigation of Cypress as a comprehensive testing tool, we found that its integration into development workflows offers substantial benefits in terms of ease of setup, speed of test execution, and the ability to handle both simple and complex test scenarios directly within a developer's main workflow. Cypress’s architecture allows for real-time test running alongside development, providing immediate feedback and drastically reducing debugging time. Although it is limited to JavaScript, this constraint is offset by the efficiency gains and the deep integration with modern web development tools and practices. Based on these findings, we advocate for Cypress as an excellent choice for web application testing, particularly in environments that emphasize rapid development cycles and high-quality user interfaces.

## Conclusion

Summarize the key points discovered in this assignment and any conclusions drawn from the analysis and testing tool investigation.

## References

List all references used to prepare this report and presentation.

- <https://www.cypress.io/>

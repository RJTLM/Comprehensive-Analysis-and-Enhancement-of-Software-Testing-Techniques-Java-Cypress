# CMPE3008 Software Engineering Testing - Group Assignment

## **Predictive Pioneers**

## Team Members

<details>
  <summary>Click to view team members:</summary>
  <p><p>Member 1: Elizaveta Rus, 17904982</p>
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
    <summary><strong>Click to view the BubbleSort source code:</strong></summary>

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
    <summary><strong>Click to view the Sorting Algorithms Test Code:</strong></summary>

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

#### Method 2: [Method Name]

- **Description:** [Brief description of what this method does]
- **File Location:** [Relative path in repository]
- **Test File Location:** [src/test/java/murraco/SortingAlgorithmsTest.java](https://github.com/murraco/sorting-algorithms/blob/master/src/test/java/murraco/SortingAlgorithmsTest.java)

    <details>
    <summary><strong>Click to view the Sorting Algorithms Test Code:</strong></summary>

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

#### Graph for Method 1

![Graph Image](path/to/graph1.png)

#### Graph for Method 2

![Graph Image](path/to/graph2.png)

### Prime Path Coverage (10 Marks)

Discuss your prime path coverage analysis for each method.

#### Method 1

#### Method 2

### Syntax-Based Testing Analysis (10 Marks)

Discuss the creation of mutants, mutation operators used, and the analysis of Reachability, Infection, and Propagation conditions.

#### Mutants for Method 1

- **Mutant 1:** [Description]
- **Mutant 2:** [Description]

#### Mutants for Method 2

- **Mutant 1:** [Description]
- **Mutant 2:** [Description]

## Test Method Analysis (5 Marks)

Evaluate the existing test methods against the mutants created and provide an opinion on the sufficiency of the tests.

### Analysis for Test Method 1

- **Observations:** [Your observations]
- **Sufficiency of Testing:** [Your judgment]

### Analysis for Test Method 2

- **Observations:** [Your observations]
- **Sufficiency of Testing:** [Your judgment]

## Testing Tool Investigation (10 Marks)

### Chosen Tool: [Tool/Framework Name]

- **Purpose and Functionality:** [Describe the purpose and what the tool can do]
- **Usage:** [Explain how the tool should be used with general descriptions and examples]
- **Other Considerations:** [Discuss standards, popularity, etc.]
- **Recommendation:** [Do you recommend this tool? Why?]

## Presentation (7 Marks)

Link to presentation slides or include a brief outline of what will be covered in the presentation.

## Report Summary

Provide a concise summary of your findings and analyses.

## Conclusion

Summarize the key points discovered in this assignment and any conclusions drawn from the analysis and testing tool investigation.

## References

List all references used to prepare this report and presentation.

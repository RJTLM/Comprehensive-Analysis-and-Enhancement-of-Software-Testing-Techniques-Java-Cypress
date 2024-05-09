# CMPE3008 Software Engineering Testing - Group Assignment

## **Predictive Pioneers**

## Team Members

<details>
  <summary>Click to view team members:</summary>
  <p><p>Member 1: Elizabeth Russell, 17904982</p>
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

# Testing Tool Investigation (10 Marks)

## Chosen Tool: Cypress

Cypress is primarily designed for developers and quality assurance (QA) engineers who are involved in building and testing modern web applications. It's particularly well-suited for the following groups and scenarios:

1. **JavaScript Developers**: Cypress is built for and uses JavaScript exclusively for writing tests. This makes it ideal for developers and teams already using JavaScript as their main programming language, as it allows them to write tests in a language they are familiar with.

2. **Front-end Developers**: Since Cypress is tailored for testing web applications, front-end developers, particularly those working with modern JavaScript frameworks like React, Angular, or Vue.js, find it highly beneficial. Cypress integrates seamlessly with these frameworks, making it easy to test applications as they are built.

3. **Full-stack Developers**: Cypress not only handles front-end testing but also allows for testing server responses and APIs directly from the browser. This makes it a useful tool for full-stack developers looking to perform end-to-end testing.

4. **DevOps and CI/CD Pipelines**: Cypress supports Continuous Integration/Continuous Deployment processes, providing features that make it straightforward to integrate into automated testing pipelines. Teams practicing DevOps can use Cypress to automate their testing workflows, ensuring that tests are run automatically whenever changes are made to the codebase.

5. **Quality Assurance Teams**: QA teams looking for a robust testing tool that can handle complex user interactions and simulate real user behavior will find Cypress valuable. Its ability to run tests in a real browser environment allows testers to see exactly what users will see, helping to identify and fix issues more effectively.

6. **Teams Emphasizing Test-driven Development (TDD)**: Cypress facilitates TDD practices by making it simple to write and run tests before implementing functionality. This approach helps ensure that the development process leads to robust and bug-free software.

7. **Projects Requiring Detailed Test Reporting**: Cypress provides rich, interactive test reports that make debugging easier. Teams that need comprehensive reporting to analyze test outcomes will benefit from Cypress's detailed logs and visual test command execution.

Overall, while Cypress is particularly favored by those using JavaScript, its broad capabilities make it suitable for a wide range of web development and testing tasks across different team roles and project types. It’s a versatile choice that aligns well with contemporary web development and testing standards.

## Comparison

Cypress is a popular tool for web application testing, and it faces competition from several other well-established testing frameworks. Here are three of the main rivals of Cypress, along with a comparison of their pros and cons in relation to Cypress:

1. **Selenium**
2. **Puppeteer**
3. **Playwright**

Here's a table comparing Cypress with these top three rivals:

| Feature/Tool   | Cypress                                                 | Selenium                                               | Puppeteer                                              | Playwright                                             |
|----------------|---------------------------------------------------------|--------------------------------------------------------|--------------------------------------------------------|--------------------------------------------------------|
| **Language Support** | JavaScript only                                         | Supports multiple languages (Java, C#, Ruby, Python)   | JavaScript only                                        | JavaScript, Python, C#, and Java                       |
| **Architecture** | Runs inside the browser; direct access to DOM           | Operates outside the browser; uses drivers             | Operates outside the browser; uses Chrome DevTools Protocol | Uses browser contexts for parallel testing; uses CDP   |
| **Ease of Setup** | Very easy to set up and use                              | Complex setup involving drivers and grid configurations | Easy to set up, especially for Chrome                  | Similar to Puppeteer but supports multiple browsers    |
| **Execution Speed** | Fast due to running in the same loop as the application | Can be slower due to HTTP requests to browser drivers   | Very fast execution in Chrome                           | Fast, supports parallel testing across browsers        |
| **Browser Support** | Limited to Chrome, Firefox, and Edge                     | Wide support for almost all browsers                    | Chrome and Chromium-based browsers only                | Wide support, including Chrome, Firefox, and Safari    |
| **Use Case**  | Best for end-to-end testing of SPA and modern web apps   | Suitable for cross-browser testing and legacy applications | Ideal for quick scripting and scraping in Chrome       | Suitable for end-to-end testing and cross-browser needs |
| **Community and Ecosystem** | Growing rapidly; extensive plugins                   | Very large; mature ecosystem                            | Growing, especially among developers needing Chrome-specific tests | Rapidly growing; benefits from being newer and learning from predecessors |
| **Testing Capabilities** | Limited to what can be executed in a browser            | Comprehensive; can test any web application             | Primarily focused on headless browser testing           | Comprehensive; integrates best features of both Puppeteer and Selenium |

### Pros and Cons Comparison

- **Cypress**
  - **Pros:**
    - Direct access to DOM and application's JavaScript
    - Real-time reloads and test execution
    - Simplified debugging with automatic waiting and command log
  - **Cons:**
    - Only supports JavaScript
    - Limited to testing in Chrome, Firefox, and Edge
    - Not suitable for multi-domain management within tests

- **Selenium**
  - **Pros:**
    - Supports a wide range of programming languages
    - Extensive browser support
    - Well-established, with a vast amount of resources and integrations
  - **Cons:**
    - Requires setup of browser drivers and potentially complex grid configurations
    - Generally slower test execution due to its architecture
    - Can be overcomplex for simple projects

- **Puppeteer**
  - **Pros:**
    - Fast execution for tests in Chrome or Chromium
    - Ideal for tasks requiring direct browser control like PDF generation or scraping
    - Simple API focused on Chrome automation
  - **Cons:**
    - Limited to Chrome and Chromium-based browsers
    - Not designed for cross-browser testing
    - Less suitable for non-technical users due to API complexity

- **Playwright**
  - **Pros:**
    - Supports multiple languages and browsers, including mobile versions
    - Designed for fast and reliable execution across browser types
    - Offers features like video recording out-of-the-box
  - **Cons:**
    - Newer and less mature compared to Selenium
    - Smaller community, though rapidly growing
    - Potentially redundant if projects are committed to a single browser environment

Each tool has its strengths and ideal use cases, so the choice between Cypress and its rivals depends largely on specific project requirements, such as the programming languages in use, required browser support, and the complexity of the testing needs.

### Purpose and Functionality

Cypress is a state-of-the-art testing framework developed specifically for the needs of modern web application testing. Its design philosophy focuses on simplifying every aspect of testing web applications, including setup, test writing, execution, and debugging. Unlike traditional testing tools that operate outside the browser or through remote commands, Cypress executes in the same run-loop as the application. This unique approach eliminates the complexities associated with remote driving of a browser, which enhances test accuracy and execution speed dramatically.

Cypress is engineered to handle both simple and complex testing scenarios, offering full native access to the DOM and all related objects without the need for third-party drivers or proxies. This direct access is pivotal for creating reliable and rapid tests that can interact with the application as users do.

### Usage

Installing Cypress is straightforward, requiring only a few commands to integrate it into any existing web project via npm. It is particularly well-suited for JavaScript developers due to its API and syntax, which are intuitive for those with JavaScript experience.

A typical Cypress test involves several key actions: navigating to a webpage, selecting elements to interact with, performing actions like clicking or typing, and verifying the outcomes through assertions. These actions mimic real user interactions, making Cypress ideal for end-to-end testing.

**Basic Example Test:**

```javascript
describe('My First Test', () => {
  it('Checks for the presence of an element', () => {
    cy.visit('https://example.com');
    cy.get('.important-element').should('be.visible');
  });
});
```

**Detailed Example Test:**

```javascript
describe('Product Purchase Test', () => {
  it('Allows a user to purchase a product', () => {
    cy.visit('https://example-store.com');
    cy.get('#product-list').find('.add-to-cart').first().click();
    cy.get('#cart').click();
    cy.get('checkout-button').click();
    cy.get('#payment-info').type('4111111111111111');
    cy.get('#submit-payment').click();
    cy.contains('Thank you for your purchase!').should('be.visible');
  });
});
```

These examples demonstrate how Cypress tests are structured and executed, reflecting real user interactions within a web application, from visiting pages to completing transactions.

### Other Considerations

Cypress's rapid growth in popularity is due in part to its robust community and extensive documentation, which supports new users and seasoned developers alike. Its focus on JavaScript, while highly beneficial in JavaScript-centric development environments, can be a limitation in diverse development contexts where multiple programming languages are used.

Furthermore, Cypress offers a range of plugins and integrations that enhance its capabilities, including visual testing, accessibility checks, and integration with Continuous Integration/Continuous Deployment (CI/CD) pipelines, making it a versatile tool for modern software development practices.

### Recommendation

Given its comprehensive feature set, ease of use, and strong community support, Cypress is highly recommended for teams engaged in developing interactive, dynamic web applications, especially those using modern frameworks like React, Angular, or Vue. Its ability to streamline the testing process, from development to production, makes it an invaluable tool for enhancing software quality and reliability.

## Conclusion

Cypress stands out in the landscape of web application testing tools for its innovative approach and powerful capabilities. It not only simplifies the testing process but also enhances the quality and reliability of web applications. Our detailed investigation supports Cypress's adoption for teams aiming to integrate efficient and effective testing practices into their development cycles, ensuring high-quality user experiences and robust application performance.

---

This expanded content should provide a more detailed and comprehensive report, suitable for filling two pages with more in-depth analysis and examples, which will be beneficial for your assignment submission.

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

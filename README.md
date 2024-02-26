# COSC 3337 - Data Science I 
## Decison Trees, SVM, and K-NN Assignment ##

### Due Date: March X, 11:59 PM ###

#### The goal of this assignment is to:
1. Understand how decision trees, k-nn, and support vector machines (SVMs) are used for classification tasks.
2. Learn to tune hyperparameters in decision trees, k-nn, and SVMs to avoid overfitting.
3. Gain proficiency in using recall, precision, and accuracy as metrics for evaluating classification model performance.
4. Learn to use cross-validation techniques to assess model performance.

## Dataset - Dry Beans
**Intended Outcome:** Apply machine learning algorithms for the task of classifying varieties of beans based on visual morphological measurements. This assignment will focus on understanding and implementing classification algorithms such as decision trees, k-nearest neighbors (k-nn), and support vector machines (SVMs). Students will also gain skills in model evaluation and hyperparameter tuning.

**Dataset Description:** The dataset for this assignment is adapted from the paper [Multiclass classification of dry beans using computer vision and machine learning techniques](https://www.sciencedirect.com/science/article/pii/S0168169919311573?via%3Dihub) by Koklu et al in which the authors evaluate the capabilities of several machine learning models in classifying the varieties of beans based on the output of an image segmentation algorithm that receives images of dry beans and produces a segmentation mask.  Features were then extracted from the segmented images that pertain to the size, shape, and structure of each bean. The dataset contains 13,611 instances belonging to 7 different varieties, which are listed below.

**Dataset Preprocessing:** The dataset remains identical to the original, only with class labels encoded as numerical values in the 'Class' column rather than the original string format. The original class column is left for reference as "Class_String." Additionally, the four Shape Factor columns are dropped.

**Attributes**

The dataset contains 

- *[Class_String]:*: Original text-based class labels
- *[Class]: Class labels for each bean*
    - Barbunya: 0
    - Bombay: 1
    - Cali: 2
    - Dermosan: 3 
    - Horoz: 4
    - Seker: 5
    - Sira: 6
- *12 feature columns:*
    - Area: The area of a bean zone and the number of pixels within its boundaries.
    - Perimeter: Bean circumference; the length of its border.
    - MajorAxisLength: The distance between the ends of the longest line that can be drawn from a bean.
    - MinorAxisLength: The longest line that can be drawn from the bean while standing perpendicular to the main axis.
    - AspectRation: Defines the relationship between the Major and Minor Axis Lengths.
    - Eccentricity: Eccentricity of the ellipse having the same moments as the region.
    - ConvexArea: Number of pixels in the smallest convex polygon that can contain the area of a bean seed.
    - EquivDiameter: The diameter of a circle having the same area as a bean seed area.
    - Extent: The ratio of the pixels in the bounding box to the bean area.
    - Solidity: Also known as convexity. The ratio of the pixels in the convex shell to those found in beans.
    - roundness: Calculated with the following formula: (4piA)/(P^2)
    - Compactness: Measures the roundness of an object: (Equivalent Diameter / Major Axis Length).

### Assignment Tasks ###

**Task 1**

A. Using all attributes, build a Decision Tree model to predict bean varieties: Train the Decision Tree model using the given maximum depths (3, 7, 11, 15).  **8 points**

B. Perform 5-fold cross-validation for each of the 4 max depths and compute accuracy (mean of validation scores), precision and recall. Generate a table, as given below, for the obtained results. **5 points**   

**Decision Tree Experiments**
| Max Depths  | Accuracy    | Precision  | Recall     |
| ----------- | ----------- | ---------- | ---------- |
| 3           |             |            |            |
| 7           |             |            |            |
| 11          |             |            |            |
| 15          |             |            |            |

C. Explain how the tree size/depth affects model performance in the context of overfitting/underfitting. **3 points**

D. Explain the meaning of the difference in accuracy, precision and recall scores in relation to the task; only if there is a significant difference. **2 points**

**Task 2**

A. Using all attributes, build a k-nn classifier to predict bean varieties: Train the k-nn using the given neighbors (3, 9, 17, 25).  **8 points**

B. Perform 5-fold cross-validation for each of the 4 neighbor size and compute accuracy (mean of validation scores), precision and recall. Generate a table, as given below, for the obtained results. **5 points**

**K-NN Experiments**
|  Neighbors  |   Accuracy  | Precision  | Recall     |
| ----------- | ----------- | ---------- | ---------- |
| 3           |             |            |            |
| 9           |             |            |            |
| 17          |             |            |            |
| 25          |             |            |            |

C. Explain how the number of neighbors affects model performance in the context of overfitting/underfitting. **3 points**

D. Explain the meaning of the difference in accuracy, precision and recall scores in relation to the task; only if there is a significant difference. **2 points**

**Task 3**

A. Using all attributes, build an SVM Model to predict bean varieties: Train the SVM model using the given kernel functions (linear, polynomial, rbf, sigmoid). **10 points**

B. Perform 5-fold cross-validation for each of the 4 kernel functions and compute accuracy (mean of validation scores), precision and recall. Generate a table, as given below, for the obtained results. **5 points**

**SVM Experiments**
| Kernel Function |  Accuracy  |  Precision  |  Recall    |
| --------------- | ----------- | ---------- | ---------- |
| Linear               |             |            |            |
| Polynomial               |             |            |            |
| RBF              |             |            |            |
| Sigmoid              |             |            |            |

C. Discuss the impact of different kernels on model performance. **2 points**

D. Explain the meaning of the difference in accuracy, precision and recall scores in relation to the task. **2 points**

**Task 4**
- Interpret the tables you generated in questions 1B, 2B, 3B; compare the performance of the Decision Tree, K-NN and SVM models. Which model performs better? Why do you think that is the case? What would you recommend to further improve each model’s performance? **5 points** (*and up to 3 extra points*)



## Deliverables

1. A Python file with your code and analysis
2. A separate pdf of your report (1-2 pages) of your findings and the conclusions for Task 1C, 1D, 2C, 2D, 3C, 3D, and 4. Boldly state the task name before your explanations. 

## Submission Instructions
Please push and commit your developed solution to the github repository. Please ensure that your Github username, name, and PSID are filled in at the start of the file. Please ensure that all required plots are generated while running your solution and that your interpretations and conclusions, as required for each task, are included as comments after each task listed in the shell python file.

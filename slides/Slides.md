---
marp: true
theme: custom-default
footer: 'https://guy--l.github.io/detect-malaria'
---

# Improving Malaria Detection with Data Science
Guy Lister
MIT ADSP Jan 24 --- April 13, 2024
![bg right contain](./img/speciescycles.jpg)

---

<!-- Speaker Notes -->
# Problem Definition

- Malaria is a major global health issue with over 200 million cases annually, leading to substantial morbidity and mortality.
- Current detection methods are slow and require specialized training, hindering timely diagnosis and treatment.
<!-- Can have multiple on a slide -->

---

# Problem to Solve

- **Need for Speed and Accuracy**: Improve the speed and accuracy of malaria detection to facilitate earlier and more effective treatment.
- **Accessibility**: Enhance the availability of reliable diagnostic methods in resource-limited settings.

---

# Solution Approach

- Develop a data-driven model using machine learning to identify malaria parasites in blood samples from digital images.
- Compare various machine learning algorithms to find the most effective solution.

---

# Datasets Available

- **Publicly Available Datasets**: Utilization of open-source datasets of blood smear images that are annotated with malaria parasite presence.
    * MP-IDB: The Malaria Parasite Image Database for Image Processing and Analysis
    * MalariaSD: Malaria-Infected Cell Images dataset (Charania & Mehendale)
- **Our Dataset**: 24958 training, 2600 testing images evenly split between un/infected classes
- **Partnership Collections**: Collaboration with healthcare providers for real-world data to enhance model training.

---

# Proposed Model Solution

- Initial trials focus on Convolutional Neural Networks (CNN) due to their success in image recognition tasks.
- Feature engineering to improve model sensitivity to parasite indicators.
- Model selection will ultimately be based on the best recall

---

# Final Model Solution

- A refined CNN model showcasing superior performance metrics compared to traditional microscopy.
- Demonstration of model scalability and adaptability to different microscopy settings.
- **Final Model**: A deep CNN with LeakyReLU activation, dropout, batch normalization, and a softmax output layer, optimized with Adam. Achieves a test accuracy of 98.42%, with precision, recall, and F1-scores near or above 0.98.


---

# Proposed Business Solution

- Implementation of the model in diagnostic devices for use in clinics and remote locations.
- Partnership with health organizations for model deployment and training.

---

# Executing Business Solution

- **Pilot Program**: Launch in regions with high malaria incidence to measure impact.
- **Feedback Loop**: Incorporate field feedback to refine the model and deployment strategy.

---

# Recommendations for Implementation

- **Validation & Integration** 
- **Stakeholder Actionables**
- **Benefits & Costs**
- **Risks & Further Analysis**

<!-- ::: notes
Validate extensively against existing methods before real-world clinical deployment; integrate with health record systems and workflows.

Secure pilot testing partnerships, address data privacy and ethics, and train healthcare professionals.

Reduced diagnostic time, increased accuracy, and wider access, with costs involving deployment, maintenance, and training. Expected to significantly lower economic burdens from delayed or incorrect diagnoses.

Address potential model biases, need for updates, and ensure user trust. Monitor real-world performance, enhance model interpretability, and explore applicability to other diseases.
:::
-->
---

# Executive Summary

- **Objective**: Enhance malaria detection using data science to improve diagnosis speed and accuracy, ultimately saving lives.
- **Approach**: Utilize machine learning models to analyze blood sample images for faster, more accurate detection.
- **Key Findings**: Our proposed model significantly outperforms traditional diagnostic methods in speed and accuracy.
- **Recommendations**: Implement the model in pilot regions with high malaria prevalence to assess real-world impact.

---

# Risks & Challenges

- **Data Quality and Availability**: Ensuring high-quality, diverse datasets for model training.
- **Implementation**: Challenges in deploying and integrating the solution in existing healthcare infrastructures.
- **Adaptability**: Keeping the model updated with evolving malaria strains and resistance patterns.

---

# Thank You

Thank you for your attention and interest in improving malaria detection through data science. Your support can make a significant difference.

---

# Appendix

---

### Comparing all models

| Model Description      | Precision | Recall | F1-Score | Accuracy |
|------------------------|-----------|--------|----------|----------|
| Base                   | 0.98      | 0.98   | 0.98     | 0.98     |
| 1 new layers           | 0.98      | 0.98   | 0.98     | 0.98     |
| 2 batch normalize      | 0.98      | 0.98   | 0.98     | 0.98     |
| 3 augmentation         | 0.97      | 0.97   | 0.97     | 0.97     |
| 4 augmentation++       | 0.98      | 0.98   | 0.98     | 0.98     |
| VGG16                  | 0.95      | 0.95   | 0.95     | 0.95     |

---
## Best Two Models Comparison

<div class="columns">
<div>

### Training for Model 1

![h:400](./img/epoch1.png)

</div>
<div>

### Training for Model 3

![h:400](./img/epoch3.png)

</div>
</div>

---
##  Accuracy Comparison in Validation Data

```
                            Model 1                          Model 3          
              precision recall f1-score        precision recall f1-score    support
  uninfected       0.97   0.97     0.97             0.99   0.96     0.97       1300
 parasitical       0.97   0.97     0.97             0.96   0.99     0.98       1300
                                               
    accuracy                       0.97                             0.98       2600
   macro avg       0.97   0.97     0.97             0.98   0.98     0.98       2600
weighted avg       0.97   0.97     0.97             0.98   0.98     0.98       2600

```

---
## Results Comparison

<div class="columns">
<div>

### Model 1

![h:400](./img/matrix1.png)

</div>
<div>

### Model 3

![h:400](./img/matrix.png)

</div>
</div>

---

![contain](./img/parasitehistory.png)

---

![contain](./img/parasite2020.png)

---

## Author

<i class="fa-brands fa-twitter"></i> Twitter:&emsp;&emsp;<a href="https://twitter.com/Guy__Lister" target="_blank">@Guy__Lister</a>
<i class="fa-brands fa-linkedin"></i> LinkedIn:&ensp;&emsp;<a href="https://www.linkedin.com/in/guy-lister-coding-consultant/" target="_blank">guy-lister-coding-consultant</a> 
<i class="fa-brands fa-github"></i> GitHub:&emsp;&emsp;<a href="https://github.com/guy--l" target="_blank">Guy--L</a>

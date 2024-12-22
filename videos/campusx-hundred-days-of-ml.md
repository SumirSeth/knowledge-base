---
title: 'CampusX 100 days of machine learning'
description: 'A video series by campusx going over different concepts of machine learning.'
video: 'https://www.youtube.com/playlist?list=PLKnIA16_Rmvbr7zKYQuBfsVkjoLcJgxHH'
playlist: 'https://www.youtube.com/playlist?list=PLKnIA16_Rmvbr7zKYQuBfsVkjoLcJgxHH'
tags: ['machine learning', 'ml', 'ai']
source: 'CampusX'
---

# Video : Simple Linear Regression | Intuition

Linear regression is generally the first model that is taught to beginners.

- Easy to understand

- Concepts carry forward

<span style="color:green">Important </span>- LR is a **supervised algorithm**.

There are different types of LR:

- Simple LR - one input and one output column.

- Multiple LR - multiple input columns.

- Polynomial LR - a little advanced topic, so not detailed here.

<u>Stochastic Error</u> : 

- What is error in context of LR?
  
  - Error is just the difference between the actual value and the predicted value.

- What does it mean?
  
  - Stochastic error refers to errors or deviations caused by external random noises in the dataset.

- Stochasticity:
  
  - It refers to the well distribution of data points. It is very important in a data set. Ideally, there should be no effect of the inputs on the errors, if there are errors, it means that the model has failed to capture certain relationships in the data.
  - Hence it is important for the errors to be *random* or *stochastic* and not show patterns.

Since there will be stochastic errors in the data set, the concept of **best fit line** becomes important.

<u>Best fit line </u> : line (y = mx + c). goal: to find the best m and c such that the *residuals* becomes least.

# Sudolver models
This repository contains the training data and ML models for the sudolver app.

This repository can be viewed as a sort of incubator project for models. As soon as a model is good enough it will be incorporated into sudolver.app and put into production.

## Model Performance

| Model | Correct (%)  |
| :---:   | :-: |
| AWS Textract | 28.13 |

## Models

This section explains the various approaches to solving the task of "detecting a sudoku and solving it".

### AWS Textract

This model does nothing more than take the picture taken by the user's camera and run it through AWS Textract and solving the first table that looks like a sudoku.

# Sudolver models
This repository contains the training data and ML models for the sudolver app.

This repository can be viewed as a sort of incubator project for models. As soon as a model is good enough it will be incorporated into sudolver.app and put into production.

## Model Performance (training/validation set)

| Model | Correct (%)  |
| :---:   | :-: |
| YOLO + Laplacian (alpha=10) + AWS Textract | 56.64 |
| YOLO + Laplacian (alpha=5) + AWS Textract | 55.55 |
| YOLO + Unsharp Masking (k=10) + AWS Textract | 52.60 |
| YOLO + Unsharp Masking (k=5) + AWS Textract | 51.44 |
| AWS Textract | 28.13 |

Tesseract OCR was also used, but didn't give good enough results.

## Models

This section explains the various approaches to solving the task of "detecting a sudoku and solving it".

### AWS Textract

This model does nothing more than take the picture taken by the user's camera and run it through AWS Textract and solving the first table that looks like a sudoku.

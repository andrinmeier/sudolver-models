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

## Model Performance (test set)

| Model | Correct (%)  |
| :---:   | :-: |
| YOLO + Laplacian (alpha=10) + AWS Textract | 65.90 |
| Laplacian (alpha=10) + AWS Textract | 47.72 |
| AWS Textract | 27.27 |
| YOLO + AWS Textract | 15.90 |

The YOLO + Lapliacian sharpening + AWS Textract approach yielded the best results, also 40% more accuracy and just using AWS Textract.

## Models

This section explains the various approaches to solving the task of "detecting a sudoku and solving it".

### AWS Textract

This model does nothing more than take the picture taken by the user's camera and run it through AWS Textract and solving the first table that looks like a sudoku.

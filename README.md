# AR - Activity Recognition

The Activity Recognition (AR) project is the implementation of a system based on Data Mining (DM) and Machine Learning (ML) techniques to detect transportation modes using the accelerometer data of iLog users. The DM and ML techniques were used in combination to pre-process the streaming data and evaluate the models to provide confident labels for specific trips. In the pre-processing step, the accelerometer data was transformed using Fast Fourier Transformation [1] and in the ML step, standard techniques were used like Artificial Neural Networks, Decision Tree induction algorithms, k-Nearest Neighbour, Naive Bayes, Random Forest and Support Vector Machines [2]. The result is a model able to predict the labels with high accuracy and confident level. 

## Technical requirements

The system was develop in R version 3.4.4 -- "Someone to Lean On" [3]. To execute the code, the packages are required: e1071, kknn, randomForest, pROC and RWeka. The installation process is similar to other packages available on CRAN:

```r 
# install the packages
install.packages(c("e1071", "kknn", "randomForest", 
  "pROC", "RWeka"))
```

## Exemplo of use

```r
# load the code
setup()
# execute the evaluation
main(size=45)
```

## Datasets availables

## Add more data or labels

You can add more data (from other users) including a new file in the subfolder datasets. The file needs to be a csv separated by comma with the accelerometer (x, y, and z) columns and the label column. The scale of the accelerometer data needs to respect the range [-32, 32]. To add more labels, is important to guarantee that at least 2 users have the same label to avoid errors in the evaluation process.

## Developer notes

To submit bugs and feature requests, report at [project issues](https://github.com/QROWD/AR/issues).

## References

[1] Cooley, James W., and Tukey, John W. (1965). An algorithm for the machine calculation of complex Fourier series, Mathematics of Computation, 19(90), 297–301. doi: 10.2307/2003354.

[2] Mitchell, Thomas M. (1997). Machine Learning (1ed.), McGraw-Hill, Inc., New York, NY, USA.

[3] R Core Team (2018). R: A language and environment for statistical computing. R Foundation for Statistical Computing, Vienna, Austria. URL https://www.R-project.org/.

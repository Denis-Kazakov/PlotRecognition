Portfolio project: use of a neural network to digitize scanned plots

Industrial standards and building codes provide various calculation techniques. Older (but still effective) documents, aside from formulas, often have plots for manual determination of various parameters (see OmegaLambda.JPG in this folder). Formulas can be easily converted into code but plots are more difficult to digitize, which is further complicated by a grid of the same color as the curve.

The project aims to train a neural network to restore a function from a plot.

This version provides relative values only (y coordinates in pixels vs. x coordinates in pixels) and all plots should have the same dimensions in pixels.

There are three programs in the folder:
1. curve_generator.ipynb generates a given number of random curves by spline approximation on a set of randomly knots. And then generates plots of these curves with random numbers of grid lines. The results are saved as Numpy arrays.
2. train_test_split.ipynb splits the arrays into train and test sets.
3. plot_recognition.ipynb trains a neural network on these data.
4. OmegaLambda.ipynb test the trained model on a real plot.

This version uses Matplotlib to produce smooth curves which are then saved in a Numpy array used to train a neural network. I used the default settings of Matplotlib for the curve and grid line thicknesses in this version.

For more details, please visit:
In Russian: https://denis-kazakov.com/nomogram_ru.html
In English: https://denis-kazakov.com/nomogram_en.html
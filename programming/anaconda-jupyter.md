# Anaconda/Jupyter

```python
conda create -n my_env [python=X.X] [LIST_OF_PACKAGES]
conda activate my_env
conda deactivate

conda env list

conda list
conda install <package list>

conda env export > environment.yaml
conda env create -f environment.yaml
```

### Jupyter

#### Magic Keywords

```python
%timeit foo(bar) # Time a function

%matplotlib inline # Render images in the notebook
%config InlineBackend.figure_format = 'retina' # image with higher resolution

%pdb # Turn on the debugger
```

### Resources

* [NumPy and Pandas by Udacity](https://classroom.udacity.com/courses/ud170)
* [Python for Data Analysis](http://www.ruxizhang.com/uploads/4/4/0/2/44023465/python_for_data_analysis.pdf)


# decision trees: scikit-learn + pandas

This script/modue provides an example of learning a deccision tree with
scikit-learn.  Pandas is used to read data and custom functions are employed
to investigate the decision tree after it is learned.  Grab the code and try
it out.

## Requirements

* python -- developed with 2.7.6
* sckit-learn
* pandas
* numpy

and to create the graphc of the tree you muust have graphviz/dot installed.

## Usage

### 1. Run script from command line

```bash

    $ python analyze_dt.py
```

should produce

```
-- get data:
-- trying to download from github
-- writing to local iris.csv file
   SepalLength  SepalWidth  PetalLength  PetalWidth         Name
0          5.1         3.5          1.4         0.2  Iris-setosa
1          4.9         3.0          1.4         0.2  Iris-setosa
2          4.7         3.2          1.3         0.2  Iris-setosa
3          4.6         3.1          1.5         0.2  Iris-setosa
4          5.0         3.6          1.4         0.2  Iris-setosa


-- get_code:
if ( PetalLength <= 2.45000004768 ) {
    return Iris-setosa ( 50 examples )
}
else {
    if ( PetalWidth <= 1.75 ) {
        if ( PetalLength <= 4.94999980927 ) {
            if ( PetalWidth <= 1.65000009537 ) {
                return Iris-versicolor ( 47 examples )
            }
            else {
                return Iris-virginica ( 1 examples )
            }
        }
        else {
            return Iris-versicolor ( 2 examples )
            return Iris-virginica ( 4 examples )
        }
    }
    else {
        if ( PetalLength <= 4.85000038147 ) {
            return Iris-versicolor ( 1 examples )
            return Iris-virginica ( 2 examples )
        }
        else {
            return Iris-virginica ( 43 examples )
        }
    }
}

-- look back at original data using pandas
-- df[df['PetalLength'] <= 2.45]]['Name'].unique():  ['Iris-setosa']
```

### 2. Use interactively wth (i)python

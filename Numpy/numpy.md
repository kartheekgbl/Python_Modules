# Content

1. Introduction to numpy
2. Installation of Numpy
3. importing Numpy
4. Creating Array
5. initialization of Array
6. Array Properties
7. Array Operations
8. Array Fundtions

## 1. Introduction to numpy

- Numpy is a python Library used for working with arrays
- Lists are slow to excecute so numpy comes

## 2. Installation of Numpy

     pip install numpy

## 3. importing Numpy

    import numpy as np
    # to know the version 
    print(np.__version__)

## 4. Creating Array

- ### Array( )

  - 0-Dimentional Array

        np.array(10)

  - 1-Dimentional Array

        np.array([10,20])

  - 2-Dimentional Array

        np.array([[ 20,30],[ 30,40]])

  - 3-Dimentional Array

        # Collection of Two dimentional Arrays
        np.array([[[ 10,20],[ 20,30]],[[ 30,40],[ 40,50]] ])

- ### asarray( ) with nditer( )

it contains 3 inputs after two dimentional arrays

Generally it has array name, dtype, order

    a=[10,20,30]
    b=np.asarray(a,dtype=float)

    a=[[10,40],[30,40]]
    Here c is the row major order display with nditer and for
    b=np.asarray(a,dtype=int, order="c")

    # Here F is the column major order display with nditer and for
    b=np.asarray(a,dtype=int, order="c")

    # Printing
    for i in np.nditer(b):
    print(i)

- ### frombuffer( )

The frombuffer() function in NumPy is used to create a NumPy array from a buffer. A buffer is a contiguous block of memory that can be accessed directly by NumPy. This can be useful for a variety of tasks, such as reading data from a file or from a network connection.

The frombuffer() function takes the following arguments:

buffer: The buffer that the NumPy array should be created from.

dtype: The data type of the NumPy array.

count: The number of elements in the NumPy array.

offset: The offset in bytes from the beginning of the buffer where the NumPy array should start.

    a=b"Welcome to NUmpy"
    np.frombuffer(a,dtype="S1",count=10,offset=3)

- ### fromiter( )
        a=[10,20,30]
        np.fromiter(a,dtype=int,count=3)

## 5. initialization of Array

- zeros( )

      a=np.zeros([2,3])
      #  it fill with zeros the complete array based on dimentions

- full( )

        np.full([2,3],1)
        # it fill givention array with given number

- random.rand( )

        np.random.ran(2,3)
        # it fill the random values in given dimention and        dimentions   directly pass with out subscript

- ones( )
- eye( )

### Numarical ranges

- arange( )
- linespace( )
- logspace( )

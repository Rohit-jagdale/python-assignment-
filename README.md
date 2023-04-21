# python-assignment-
In [4]:
import numpy as np np.__version__
Out [4]: '1.24.2' In [6]:
L = list(range(10)) [str(c) for c in L] ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9']
Out [6]: ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9'] In [11]: [type(item) for item in L] Out [11]: [int, int, int, int, int, int, int, int, int, int] In [12]: np.zeros(10, dtype='int') Out [12]: array([0, 0, 0, 0, 0, 0, 0, 0, 0, 0]) In [13]: Out [13]: np.ones((3,5), dtype=float)
array([[1., 1., 1., 1., 1.], [1., 1., 1., 1., 1.], [1., 1., 1., 1., 1.]])
In [14]: Out [14]: np.full((3,5),1.23)
array([[1.23, 1.23, 1.23, 1.23, 1.23], [1.23, 1.23, 1.23, 1.23, 1.23], [1.23, 1.23, 1.23, 1.23, 1.23]])
In [15]: np.arange(0, 20, 2) Out [15]: array([ 0, 2, 4, 6, 8, 10, 12, 14, 16, 18]) In [16]: np.linspace(0, 1, 5) Out [16]: array([0. , 0.25, 0.5 , 0.75, 1. ]) In [17]: Out [17]: np.random.normal(0, 1, (3,3))
array([[ 0.15827122, 0.83275579, -0.36265561], [ 0.07562821, -0.43015947, -0.37054683], [ 1.02269042, 0.91796927, 0.67863548]])
In [18]: np.eye(3)Out [18]:
In [21]:
array([[1., 0., 0.],
[0., 1., 0.],
[0., 0., 1.]])
np.random.seed(0)
x1 = np.random.randint(10, size=6)
x2 = np.random.randint(10, size=(3,4))
x3 = np.random.randint(10, size=(3,4,5))
print("x3 ndim:", x3.ndim)
print("x3 shape:", x3.shape)
print("x3 size: ", x3.size)
x3 ndim: 3
x3 shape: (3, 4, 5)
x3 size: 60
In [22]:
x1 = np.array([4, 3, 4, 4, 8, 4])
x1
Out [22]: array([4, 3, 4, 4, 8, 4])
In [23]:
x1[0]
Out [23]: 4
In [24]:
x1[0]
Out [24]: 4
In [25]: x1[-1]
Out [25]: 4
In [26]:
x1[-2]
Out [26]: 8
In [27]:
x2 = np.array([[3, 7, 5, 5],
[0, 1, 5, 9],
[3, 0, 5, 0]])
x2
Out [27]:
array([[3, 7, 5, 5],
[0, 1, 5, 9],
[3, 0, 5, 0]])
In [28]:
x2[2,3]
Out [28]: 0In [29]:
x2[2,-1]
Out [29]: 0
In [30]:
x2[0,0] = 12
x2
Out [30]:
array([[12, 7, 5, 5],
[ 0, 1, 5, 9],
[ 3, 0, 5, 0]])
In [31]:
x = np.arange(10)
x
Out [31]: array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])
In [32]: x[:5]
Out [32]: array([0, 1, 2, 3, 4])
In [33]:
x[4:]
Out [33]: array([4, 5, 6, 7, 8, 9])
In [34]:
x[4:7]
Out [34]: array([4, 5, 6])
In [35]:
x[ : : 2]
Out [35]: array([0, 2, 4, 6, 8])
In [36]: x[1::2]
Out [36]: array([1, 3, 5, 7, 9])
In [37]:
x[::-1]
Out [37]: array([9, 8, 7, 6, 5, 4, 3, 2, 1, 0])
In [38]:
x = np.array([1, 2, 3])
y = np.array([3, 2, 1])
z = [21,21,21]
np.concatenate([x, y,z])
Out [38]: array([ 1, 2, 3, 3, 2, 1, 21, 21, 21])
In [39]:
grid = np.array([[1,2,3],[4,5,6]])
np.concatenate([grid,grid])Out [39]:
array([[1, 2, 3], [4, 5, 6], [1, 2, 3], [4, 5, 6]])
In [40]: Out [40]: In [41]: np.concatenate([grid,grid],axis=1)
array([[1, 2, 3, 1, 2, 3], [4, 5, 6, 4, 5, 6]])
x = np.array([3,4,5]) grid = np.array([[1,2,3],[17,18,19]]) np.vstack([x,grid])
Out [41]:
array([[ 3, 4, 5], [ 1, 2, 3], [17, 18, 19]])
In [42]:
z = np.array([[9],[9]]) np.hstack([grid,z])
Out [42]: In [43]:
array([[ 1, 2, 3, 9], [17, 18, 19, 9]])
x = np.arange(10) x
Out [43]: array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9]) In [46]:
x1,x2,x3 = np.split(x,[3,6]) print (x1,x2,x3)
[0 1 2] [3 4 5] [6 7 8 9] In [47]:
grid = np.arange(16).reshape((4,4)) grid upper,lower = np.vsplit(grid,[2]) print (upper, lower)
[[0 1 2 3] [4 5 6 7]] [[ 8 9 10 11] [12 13 14 15]]
In [ ]:

# Matlab notes


## tutorial
[科学计算与MATLAB语言 刘卫国 中南大学](https://www.youtube.com/playlist?list=PLBPbUxsZM4SYMRRX-lLE9P9i946XW7_AL)

[New Ways to Work in Simulink](https://www.youtube.com/playlist?list=PLn8PRpmsu08rVD5-hGVKTKTtUPHpGy3Te)



## function
- [montage](https://www.mathworks.com/help/images/ref/montage.html?searchHighlight=montage&s_tid=srchtitle)  
  Display multiple image frames as rectangular montage

- [colon, :](https://www.mathworks.com/help/matlab/ref/colon.html?searchHighlight=%28%3A%29&s_tid=srchtitle)

- [drawrectangle](https://www.mathworks.com/help/images/ref/drawrectangle.html?s_tid=srchtitle)  
  Create customizable rectangular ROI

- [normxcorr2](https://www.mathworks.com/help/images/ref/normxcorr2.html)  
  Normalized 2-D cross-correlation 
  [[example]](https://www.mathworks.com/help/images/registering-an-image-using-normalized-cross-correlation.html)

- [transpose, .'](https://www.mathworks.com/help/matlab/ref/transpose.html?searchHighlight=transpose&s_tid=srchtitle)
```matlab
B = A.'  
B = transpose(A)
```

[contains](https://ww2.mathworks.cn/help/matlab/ref/contains.html) 确定字符串中是否有

[sortrows](https://www.mathworks.com/help/matlab/ref/double.sortrows.html#bt8bwzx-1-direction)
Sort rows of matrix or table

[unique](https://www.mathworks.com/help/matlab/ref/double.unique.html#bs_6vpd-1-setOrder)
Unique values in array


Optimization Toolbox™ 教程  
https://ww2.mathworks.cn/help/optim/ug/optimization-toolbox-tutorial.html  
https://ww2.mathworks.cn/help/optim/ug/optim.problemdef.optimizationproblem.optimoptions.html  






### script
```matlab
#matrix 
A = [1 2 3 4 ; 5 6 7 8; 1 2 9 10; 2 5 11 12]

#Determinate
a = det (A)

```



#### 在cell中找指定元素
```
a_cell = {'ni', 'hao', 'hao'}
% 第一种方法
idx = find(ismember(a_cell, 'ni' ))

% 第二种方法
idx = find(strcmp(a_cell, 'ni' ))
```

输出
```
idx =

     2     3
```


#### import file
```
% T = readtable('./file.csv');

% T1 = importdata('./file.csv');

% T2 = load('./file.csv'); 

```

[readtable](https://www.mathworks.com/help/matlab/ref/readtable.html)
[textscan](https://www.mathworks.com/help/matlab/ref/textscan.html#btghhyz-1-fileID)

# python
## 函數
list,range,type,str,print  
1.1 enumerate:輸入list,start_index輸出tuple
## 常用參數
dtype:"float32",int,float,bool
## numpy
2.1 array:list,dtype  
2.2 zeros:number,dtype  
2.3 ones:tuple,dtype  
2.4 full:tuple,number  
2.5 arange:起始值，末值，間隔  
2.6 linsqace:起始值，末值，長度  
2.7 random.random:tuple  
2.8 random.normal:mean,stv,tuple  
2.9 random.randint:min,max,tuple  
2.10 eye:number  
2.11 empty:number  
2.12 random.seed:number
2.13 random.RandomState:number
2.14 add.at:array,list位置,number
2.15 concatenate:\[array1,array2\],axis  
2.16 vstack:\[array1,array2\]  
2.17 hstack:\[array1,array2\]  
2.18 split:list,list分割點
2.19 vsplit:array,list分割點  
2.20 hsplit:array,list分割點  
### 屬性
ndim,shape,size,itemsize,nbytes,dtype
### 方法
3.1 reshape:tuple
3.2 copy

### 取值
4.1 一維  
4.1.1 單一值:\[位置\]  

4.1.2 多個值:\[array\](與array形狀一樣)  

4.1.3 範圍:\[起始點:最末點:間隔\]  
4.2 二維  
4.2.1 單一值:\[row,column\]  

4.2.2 多個值\[array1,array2\](array1與array2一個一個對應，不足擴充到一樣大)  

4.2.3 範圍:\[::,::\]  
4.2.4 某一列:\[number\]
* 可用mask取值
### 其他變形方法
5.1 \[:,np.newaxis\]
## list
### 方法
6.1 append  
6.2 pop:輸入number,輸出取出值  
6.3 extend:輸入list  



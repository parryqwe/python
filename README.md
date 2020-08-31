# python
## 函數
list,range,type,str,print(sep,end),astype,input,sorted(dict,key,reverse),sorted(list,reverse),to_dict,tolist,to_json  
1.1 enumerate:輸入list,start_index輸出tuple  
1.2 join:輸入list  

## 常用參數
dtype:"float32",int,float,bool,dict("names":tuple,"formats":tuple),'U10','i4','f8',np.float32,(np.str_,10),np.datetime64,"category","object","float64","int64"
## 文字處理str
lower,ast.literal_eval,startswith,capitalize,upper,rjust,center,replace,strip,islower,isdigit,splitlines,join(list),split,extract,len,findall,get,get_dummies,contains
### string
punctuation(屬性)
### 正規化re
sub,IGNORECASE(屬性)
## 時間處理
pd.to_datetime(format="%Y%m%d"):dayofweek,year,month,day,strftime  
pd.datetime(year,month,day)  
pd.to_timedelta(np.arange(12),'D')  
pd.Timedelta(number,"D")  
pd.DatetimeIndex(list)  
to.period("D"):days  
pd.date_range(開始日,結束日) or pd.date_range(日期,periods,freq),pd.period_range(日期,periods,freq),pd.timedelta_range(時間,periods,freq)  
*freq:"H","M","D","2H30T",BDay()  
asfreq(freq,method('bfill' or "ffill" or "pad"))  
shift  
tshift  
rolling  
### from pandas.tseries.offsets import BDay
Bdays
### from datetime import datetime
datetime(year,month,day)
datetime.strftime(time,'%Y-%m-%d %H:%M:%S UTC' or '%Y' or "%m" or "%d" or "%H" or "%M" or "%S" or "%w" or "%U")
### from dateutil import parser
parse(text):strftime
### from pandas_datareader import data
DataReader(,start,end,data_source)
## 字典
get,items,add,remove,setdefault
## 集合
intersection,union,symmetric_difference,difference
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

2.21 dtype:dict("name":tuple,"formats":tuple) or list(tuple)  

2.22 argmin:array  

2.23 sort:array  

2.24 argsort:array,axis  

2.25 partition:array,axis  

2.26 add,subtract,divide,floor_divide,power,mod:array,number  

2.27 abs,add.reduce,multiply.reduce,add.accumulate,multiply.accumulate:array  

2.28 power:number,array  

2.29 multiply.outer:array,array  

2.30 percentile:array,number(or list)

2.31 count_nonzero,sum,any,all:array(裡面放true or false),axis  

2.32 zeros_like(array)
2.33 searchsorted(array1,array2)
2.34 random.multivariate_normal(mean,cov,number)  
2.35 where(條件,,)  
### 屬性
ndim,shape,size,itemsize,nbytes,dtype  

### 方法
3.1 reshape:tuple
3.2 copy
3.3 sum.max,min,mean,std.median:axis
3.4 ravel
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
## pandas
7.1 Series  
7.1.1 list,index  
7.1.2 dict  
7.2 DataFrame  
7.2.1 dict(columns_name:Series)  
7.2.2 list(dict)一列一列加  
7.2.3 Series,columns  
7.2.4 array,index,columns  
7.2.5 結構化陣列  
7.3 concat(list(Series or dataframe),axis,ignore_index,keys=list,join,join_axes=list)  
7.4 cut(list,list)  
7.5 qcut(list,number)  
7.6 Index   
7.6.1 Index(list)  
7.6.2 MultiIndex.from_tuples(list(tuple),names)  
7.6.3 MultiIndex.from_arrays(array,names)  
7.6.4 MultiIndex.from_product(array,names)  
7.6.5 MultiIndex(levels=array,labels=array,names)  
### 屬性
values,index(.names),columns,T,shape
### 方法
8.1 items  
8.2 query("條件")  
8.3 iterrows  
8.4 add(Series,fill_value)  
8.5 stack  
8.5.1 mean  
8.6 subtract(Series,axis)  
8.7 groupby(list,as_index) or groupby(dict)  
8.7.1 rename(dict)  
8.7.2 aggregate(list)統計量 or aggregate(dict(columns:統計量))  
8.7.3 filter(function),transform(function),apply(function)  
8.8 describe  
8.9 unstack(level)  
8.10 set_index(columns)  
8.11 fillna:number  
8.12 value_counts  
8.13 sort_values(by,ascending)  
8.14 replace(number,number)  or replace(dict,inplace)  
8.15 append(dataframe)  
8.16 merge(how,on,left_on,right_on,left_index,right_index,suffixes=list)  
8.17 join(dataframe)  
8.18 mean(axis,level="")  
8.19 pivot.table("",index,columns,margins,aggfunc) or pivot.table(index,columns,aggfunc=dict(columns:統計量))  
8.20 reindex(index方法7.6)  
8.21 sort_index  
8.22 reset_index(columns)  
8.23 isnull  
8.24 dropna  
8.25 eval(text)  
8.26 resample  
8.27 drop  
8.28 select_dtypes(includes)  
8.29 align(data,join,axis)
8.30 unique
###  取值loc,iloc,ix,pd.IndexSlice(多個index,多個columns)
9.1 Series  
9.1.1 單一值:number  
9.1.2 多個值:list  
9.1.3 範圍:\[起始點:最末點\]  
9.1.4 根據條件:\[條件\]  
9.2 DataFrame  
9.2.1 單一值:\[row,column\]   
9.2.2 範圍:\[起始點:最末點\,起始點:最末點\]  
# collections
## defaultdict
10.1 defaultdict(lambda:0) or defaultdict(list)
## time
11.1 time 

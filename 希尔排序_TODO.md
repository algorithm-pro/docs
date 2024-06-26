对原始数组进行预处理。 
所谓分组，就是让元素两两一组，同组两个元素之间的跨度，是数组总长度的一半。 

```
public static void shellSort(int[] array){
  //希尔排序的增量
  int d = array.length;
  while( d>1){
    d=d/2;
    for (int x=0; x<d; x++){
      for (int i=x+d; i<array.length; i=i+d){
        int temp=array[i];
        int j;
        for (j=i-d; (j>=0)&&(array[j]>temp); j=j-d){
          array[j+d] = array[j]
        }
        array[j+d] = temp;
      }
    }
  }
}

public static void main(String[] args){
  int[] array={5,3,9,12,6,1,7,2,4,11};
  shellSort(array)
}
```

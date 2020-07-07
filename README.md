# Exercise 2

统计页面所有view的个数，可以通过如下代码递归实现

```java
public int countViewNum(ViewGroup target_view){
  int viewNum = target_view.getChildCount();
  for(int i=0; i<childNum; i++){
    View oneChild = target_view.getChildAt(i);
    if(oneChild instanceof ViewGroup){
      int childchildNum = countViewNum(child);
      viewNum = viewNum + childchildNum;
    }
    else{
      viewNum++;
    }
  }
  return viewNum;
}
```


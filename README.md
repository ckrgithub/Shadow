# Shadow

检查AndroidP是否有非sdk的隐藏api调用
```java
private static void detectNonSdkApiUsageOnAndroidP(){
  if(Build.VERSION.SDK_INT<Build.VERSION_CODES.P){
    return;
  }
  StrictMode.VmPolicy.Builder builder=new StrictMode.VmPolicy.Builder();
  builder.penaltyDeath();
  builder.detectNonSdkApiUsage();
  StrictMode.setVmPolicy(build.build());
}
```
**io流工具类：common-io**

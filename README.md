### 1.flutter 网络请求例子

#### 使用方式

```
import 'utils/http.dart';

void initState () {
  super.initState();
  getHttp();
}
void getHttp() async{
    try {
      var result = await Http().get("/in_theaters",data: {});
      print(result);
      setState(() {
      title = result['title'];
      subjects = result['subjects'];
    });
    }catch(e){
      return print(e);
    }
}
```

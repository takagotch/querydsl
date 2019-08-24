### querydsl
---
https://github.com/querydsl/querydsl

http://www.querydsl.com/

```java
//

public class SerializerBaseTest {
  
  @Test
  public void test() {
    DummySerializer serializer = new DummySerializer(new JavaTemplates());
    StringPath strPath = Expressions.stringPath("str");
    
    serializer.handle(strPath);
    
    serializer.handle(strPath.IsNotNull());
    
    serializer.handle(new PathBuilder<Object>(Object.class,"p").getList("l",Map.class).get(0));
    
    serializer.handle(ConstantImpl.create(""));
    
    serializer.handle(ExpressionUtils.tmplate(Object.class, "xxx", ConstantImpl.create("")));
  }
}
```

```sh
mvn -Pquickbuild,{projectname} clean install
librarian-puppet install
vagrant up
```

```
```



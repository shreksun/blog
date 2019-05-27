---
title: code
date: 2019-05-22 20:32:41
categories:
- Java
tags:
- code
---

#### 拷贝具有大量相同属性的类

```java
//拷贝到target
public static void copyProperties(Object source, Object target) throws BeansException {
		copyProperties(source, target, null, null);
	}
```


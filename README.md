Абстрактный класс Metal: 

``` 
public abstract class Metal { 
public abstract int getEndurance(); 
} 
``` 

Классы steel, copper, iron, унаследованные от Metal: 
``` 
public class Steel extends Metal { 
@Override 
public int getEndurance() { 
return 50; 
} 
} 

public class Copper extends Metal { 
@Override 
public int getEndurance() { 
return 20; 
} 
} 

public class Iron extends Metal { 
@Override 
public int getEndurance() { 
return 30; 
} 
} 
``` 

Класс Plastic не наследуется от Metal: 
``` 
public class Plastic { 
} 
``` 

Класс Sword с использованием дженериков: 
``` 
public class Sword<T extends Metal> { 

private final T metal; 

public Sword(T metal) { 
this.metal = metal; 
} 

public boolean checkEndurance() { 
return metal.getEndurance() > 49; 
} 

} 
``` 

Тестовый класс Test: 
``` 
public class Test { 
public static void main(String[] args) { 
// Не компилируется 
// Sword<Plastic> plasticSword = new Sword<>(new Plastic()); 

// Создаем меч с использованием steel 
Sword<Steel> steelSword = new Sword<>(new Steel()); 

// проверяем прочность и выводим результат на экран 
boolean isStrong = steelSword.checkEndurance(); 
System.out.println("Меч из стали " + (isStrong ? "прошел" : "не прошел") + " проверку прочности"); 
} 
} 
```Абстрактный класс Metal: 

``` 
public abstract class Metal { 
public abstract int getEndurance(); 
} 
``` 

Классы steel, copper, iron, унаследованные от Metal: 
``` 
public class Steel extends Metal { 
@Override 
public int getEndurance() { 
return 50; 
} 
} 

public class Copper extends Metal { 
@Override 
public int getEndurance() { 
return 20; 
} 
} 

public class Iron extends Metal { 
@Override 
public int getEndurance() { 
return 30; 
} 
} 
``` 

Класс Plastic не наследуется от Metal: 
``` 
public class Plastic { 
} 
``` 

Класс Sword с использованием дженериков: 
``` 
public class Sword<T extends Metal> { 

private final T metal; 

public Sword(T metal) { 
this.metal = metal; 
} 

public boolean checkEndurance() { 
return metal.getEndurance() > 49; 
} 

} 
``` 

Тестовый класс Test: 
``` 
public class Test { 
public static void main(String[] args) { 
// Не компилируется 
// Sword<Plastic> plasticSword = new Sword<>(new Plastic()); 

// Создаем меч с использованием steel 
Sword<Steel> steelSword = new Sword<>(new Steel()); 

// проверяем прочность и выводим результат на экран 
boolean isStrong = steelSword.checkEndurance(); 
System.out.println("Меч из стали " + (isStrong ? "прошел" : "не прошел") + " проверку прочности"); 
} 
} 
```

# 09/29/21: Polymorphism
- Polymorphism is when a subtype (instance of child class) and can act as its parent object
- Ex (see below): Dog object can be sent a method that takes an Animal
- **Tip**: think of extends as "is a"

```java
class Pet { }
// Pet is a Pet, i.e. every class can behave like itself
// Pet is a Object
class Dog extends Pet { }
// Dog is a Dog
// Dog is a Pet
// Dog is a Object
```

- Method overloading can get confusing with polymorphism

```java
class Pet {
    public String getType() {
        return "Pet";
    }
    void greetPet(Pet pet) {
        System.out.println("Hello, " + pet.getType());
    }
}
class Dog extends Pet {
    @Override
    public String getType() {
        return "Dog";
    }
}

Dog dog = new Dog();
greetPet(dog); // this  prints Hello Dog even though the greetPet method morphs dog into a Pet, Java still knows that it is a Dog and runs that overridden method
```

## Upcasting
- Is always safe, Java does it automatically
- Dog extends Pet and Pet extends Object. Dog can be morphed into a Dog, Pet, or Object (apply IS A)
- Java uses type of **VARIABLE (left side)** to determine what methods can be called
- Ex: Pet pet can also be a cat or a fish, so it doesn't make sense for you to be able to access Dog's woof method
- You can call all of Pet's methods using Pet pet = new Dog because Dog extends Pet and thus the behavior is also inherited

```java
class Pet {
    public void greet() {
        System.out.println("Hello");
    }
}
class Dog extends Pet {
    void woof() {
        System.out.println("Woof");
    }
}

Dog dog = new Dog();
Pet pet = new Dog(); 
Object o = "test"; // any object can be stored as Object


// these are allowed
pet.greet();
System.out.println(o.toString());

// these are wrong
pet.woof();
o.woof();
```

## Downcasting
- Use **instanceof** to test if an object is an instance of a particular class
- You can explicitly cast objects only once you check that it's an instanceof the desired class
```java
class Pet { }
class Dog extends Pet {
    void bark() { }
}
class Cat extends Pet {
    void meow() { }
}

Pet dog = new Dog();
Pet cat = new Cat();
Pet pet = new Cat();

if (cat instanceof Cat) {
    Cat ourCat = (Cat) cat;
    outCar.meow();
}

cat = new Pet();
System.out.println(cat instanceof Cat); // is FALSE
```

- Note for hw: "single class method" means public **static** method
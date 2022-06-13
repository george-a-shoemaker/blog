---
layout: single
title:  "Kotlin Generic Types: In vs Out"
date:   2022-05-20 12:00:00 -0600
categories: jekyll update
---
\~or\~ the meaning of covariance and contravariance in programming.

When dealing with the generics in Kotlin, there are two keywords that made me scratch my head: `in` & `out`. To understand the concepts behind them, we need to reason about the relationship between super classes and the sub classes derived from them.

## A subclasses are super classes
To get warmed up consider this example:

```kotlin
open class Super
class Sub: Super()

data class Wrapper<T>(val data: T)

fun main() {
    val wrapper : Wrapper<Super> = Wrapper(Sub())
    val data : Sub = wrapper.data // Does not compile
}
```
Notice that the generic type `T` has been set to `Super` in our `wrapper` variable. But we can pass an instance of `Sub` as the initializer argument. This is an example of how subclasses can be treated as superclasses and the compiler is happy.

However the compiler won't let us treat `wrapper.data` as an instace of `Sub` (not without casting). This is because a superclass is not necesarilly a subclass, therefore the subclass details of the instance is ignored.

## Preserving the subclass details




Now coniuder the following classes and their relationship:
```kotlin
open class Animal
class Dog: Animal()
```
In OOP every subclass can be treated as it's superclass. Ever `Dog` is an `Animal` and can be treated as such.

Intutively, we'd expect the following to work:
```kotlin
val dataWrapper : DataWrapper<Animal> = DataWrapper(Dog())
```



<!-- [jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/ -->

## typedoc-plugin-no-inherit

A plugin for [Typedoc](http://typedoc.org) to exclude inherited members from a Typedoc class using `@noInheritDoc` annotation.

### Installation

```
npm install typedoc-plugin-no-inherit --save-dev
```

### Usage

Add `@noInheritDoc` tags in a class or interface's docstring to prevent it from inheriting documentation from parents.

```ts
class Animal {
  /**
   * Documentation for move() method.
   */
  public move(distanceInMeters: number = 0) {
    console.log(`Animal moved ${distanceInMeters}m.`);
  }
}

/**
 * Documentation for the Dog class.
 * @noInheritDoc
 */
class Dog extends Animal {
  /**
   * Documentation for bark() method.
   */
  public bark() {
    console.log('Woof! Woof!');
  }
}
```

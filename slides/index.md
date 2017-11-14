- title : Make Web Apps Fun to Build and Easy to Refactor with Elm
- description : Introduction to React Native with F#
- author : Daniel Bachler
- theme : night
- transition : none
- width: 1920
- height: 1080

***

## Make Web Apps Fun to Build & Easy to Refactor with Elm

<br/>
<br/>

#### Daniel Bachler
#### [danielbachler.de](http://danielbachler.de)
#### [@danyx23](http://twitter.com/danyx23) on Twitter


***
- data-background-image: images/intro_Ber.png
- data-background-size: contain

***
- data-background-image: images/LandsOfLanguages.jpg
- data-background-size: contain

***

## Elm Elevator pitch

* Purely functional programming language
* Statically typed
* Compiles to JavaScript
* Designed to make Web Apps
* Easy to learn, nice to use


***

## Javascript syntax

```Javascript
function addNumbers(a, b) {
    return a + b;
}

// Whatever
var result = addNumbers(4, "three");
```

---

## Elm syntax

```elm
         addNumbers a  b =
           a + b


-- Compile error!
    result = addNumbers 4  "three"
```

---

## Elm syntax

```elm

addNumbers a b =
    a + b


result = addNumbers 4 3
```


---

## Type annotations

```elm
addNumbers : Int -> Int -> Int
addNumbers a b =
    a + b

result : Int
result = addNumbers 4 3
```

---

## Functions must be a single expression

```elm
calculateFormula : Int -> Int -> Int
calculateFormula a b =
    squaredA = a * a
    squaredB = b * b
    squaredA + squaredB
    -- compile Error
```

---

## Let blocks for intermediate results

```elm
calculateFormula : Int -> Int -> Int
calculateFormula a b =
    let
        squaredA = a * a -- <- Compile error
        squaredB = b * b -- <- Compile error
    in
        squaredA + squaredB

```

***

### Pain points Elm solves

--- 

### Undefined is not a function
#### Elm doesn't have null/undefined

--- 

### Refactoring is hard & error prone
#### Elm is statically typed and has a simple but powerful type system

--- 

### 
#### Elm is statically typed and has a simple but powerful type system


***

```elm
// MODEL

type alias Model = {
    counters : List Int
}

type Msg = 
| Insert
| Remove
| Modify Int (List Int)

init : Model
init =
    { counters = [] }
```

***

### Modern mobile app development?

* UI/UX
    * "Native mobile apps"
    * Performance
* Tooling
    * Hot loading
    * IntelliSense
* Maintainability
    * Easy to debug
    * Correctness

---

### "Native" UI

 <img src="images/meter.png" style="background: transparent; border-style: none;"  width=300 />

---
- data-background-image: images/hotloading.gif
- data-background-size: contain

*** 

### Model - View - Update

#### "Elm - Architecture"

 <img src="images/Elm.png" style="background: white;" width=700 />


 <small>http://danielbachler.de/2016/02/11/berlinjs-talk-about-elm.html</small>


*** 

### Thank you!

* https://github.com/fable-compiler/fable-elmish
* https://ionide.io
* https://facebook.github.io/react-native/


***
- data-background-image: images/outro_Ber.png
- data-background-size: contain
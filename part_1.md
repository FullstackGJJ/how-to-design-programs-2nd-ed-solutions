# Part I: Fixed-Size Data

## Exercise 1:
`(sqrt (+ (sqr x) (sqr y)))`

## Exercise 2:
`(string-append prefix "_" suffix)`

## Exercise 3:
`(string-append (substring str 0 5) "_" (substring str 5 (string-length str)))`

## Exercise 4:
`(string-append (substring str 0 5) (substring str (+ i 1) (string-length str)))` a value of i that is less than the length of the string are legitimate

## Exercise 5:
```
(above (triangle 100 "solid" "green")
       (rectangle 30 50 "solid" "brown"))
```

## Exercise 6:
`(* (image-width cat) (image-height cat))`

## Exercise 7:
`(or (not sunny) friday)`

## Exercise 8:
```
(if
 (> (image-height cat) (image-width cat))
 "tall"
 (if
  (= (image-height cat) (image-width cat))
  "square"
  "wide"))
```

## Exercise 9:
```
(cond
  [(string? in) (string-length in)]
  [(image? in) (* (image-width in) (image-height in))]
  [(number? in) (abs in)]
  [in 10]
  [(not in) 20])
```
## Exercise 10:
NA

## Exercise 11:
```
(define (distance-from-origin x y)
  (sqrt (+ (sqr x) (sqr y))))
```

## Exercise 12:
```
(define (cvolume length)
  (expt length 3))

(define (csurface length)
  (* (sqr length) 6))
```

## Exercise 13:
```
(define (string-first str)
  (substring str 0 1))
```

## Exercise 14:
```
(define (string-last str)
  (substring str (- (string-length str) 1) (string-length str)))
```

## Exercise 15:
```
(define (==> sunny friday)
  (or (not sunny) friday))
```
## Exercise 16:
```
(define (image-area image)
  (* (image-width image) (image-height image)))
```

## Exercise 17:
```
(define (image-classify image)
  (if
 (> (image-height image) (image-width image))
 "tall"
 (if
  (= (image-height image) (image-width image))
  "square"
  "wide")))
```

## Exercise 18:
```
(define (string-join prefix suffix)
  (string-append prefix "_" suffix))
```

## Exercise 19:
```
(define (string-insert str i)
  (string-append (substring str 0 5) "_" (substring str 5 (string-length str))))
```

## Exercise 20:
```
(define (string-delete str i)
  (string-append (substring str 0 5) (substring str (+ i 1) (string-length str))))
```

## Exercise 21:
It does not  reuse the results of computation

## Exercise 22:
It does match my intuition

## Exercise 23:
It works by grabbing the first substring of length 1 at the beginninng of the string

## Exercise 24:
#false

## Exercise 25:
Stepping through does not suggest a fix

## Exercise 26:
It replaces a character at the number with a "_"

## Exercise 27:
```
(define attendance-at-benchmark-price 120)

(define benchmark-price 5.0)

(define change-in-attendance 15)

(define change-in-price 0.1)

(define (attendees ticket-price)
  (-
   attendance-at-benchmark-price
   (*
    (- ticket-price benchmark-price)
    (/ change-in-attendance change-in-price))))
```

## Exercise 28:
$2.90

## Exercise 29:
Removing the fixed cost but increasing variable cost to 1.50 made the most profitable price become $3.60 instead, but the revenue dropped from $1000 to $693

## Exercise 30:
`(define price-sensitivity (/ 15 0.1))`

## Exercise 31:
NA

## Exercise 32:
- Pressure sensor
- Incoming notification from external service
- Reacting to body signals
- Touch screens input
- Change in lighting sensed by cameras

## Exercise 33:
Year 2000 problem is good illustration for how perfect solutions don't exist and it's important to understand how to design programs and be adaptable and flexible

## Exercise 34:
```
; String -> String
; gets the first single char of str as a string
; given: apple, expect: a
; given: banana, expect: b
(define (string-first str)
  (substring str 0 1))
```

## Exercise 35:
```
; String -> String
; gets the last single char of str as a string
; given: apple, expect: e
; given: banana, expect: a
(define (string-last str)
  (substring str (- (string-length str) 1) (string-length str)))
```

## Exercise 36:
```
; Image -> Number
; gets the number of pixels in a given image
(define (image-area image)
  (* (image-width image) (image-height image)))
```

## Exercise 37:
```
; String -> String
; get a new string that is str but with the first character removed
; given: banana, expect: anana
; given: apple, expect: pple
(define (string-rest str)
  (substring str 1 (string-length str)))
```

## Exercise 38:
```
; String -> String
; get a new string that is str but with the last character removed
; given: banana, expect: banan
; given: apple, expect: appl
(define (string-remove-last str)
  (substring str 0 (- (string-length str) 1)))
```

## Exercise 39:
```
(define (car-image wheel-radius)
  (overlay/xy
    (rectangle (* wheel-radius 5) (* wheel-radius 2) "solid" "red")
    0 wheel-radius
    (overlay/xy
      (circle wheel-radius "solid" "black")
      (* 3 wheel-radius) 0
      (circle wheel-radius "solid" "black"))))
```

## Exercise 40:
```
; WorldState -> WorldState 
; moves the car by 3 pixels for every clock tick
; examples: 
(check-expect (tock 20) 23)
(check-expect (tock 78) 81)
(define (tock cw)
  (+ cw 3))
```

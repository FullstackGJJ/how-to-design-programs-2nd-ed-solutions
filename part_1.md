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

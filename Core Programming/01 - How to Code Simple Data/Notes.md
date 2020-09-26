- [x] [Introduction](https://link)
- [x] [Beginning student language](https://link)
- [x] [How to design functions](#htdf)


----------
### <a name="htdf">Beginning Student Language</a> : 

#### Notes
- **Predicate :** Is a logical expression which evaluates to TRUE or FALSE, normally to direct the execution path in code.

- Expressions give value `1 + 1` is an expression


----------
### <a name="htdf">How To Design Functions</a> : 

#### Notes
- Function Design recepie
  - Signature ,purpose ,and Stub 
  - Define Examples and Test cases
  - Function Template
  - Function body
  - Run 
- Examples :
    ```
    ;#Signature : Number -> Number     
    ;#purpose   : Takes a number and produces twice the number.
    ;#Stub      : (define double n) 0 )
    ;#Test Cases: 
        (check-expect (double 5) 10)
        (check-expect (double 0) 0)  

    ;#Template  : 
        (define (double n)
            (...n))

    ;Body        :
        (define (double n) 
            (n * 2))
    ```

#### Quiz 1 :

```
(require 2htdp/image) 
;; Image -> Boolean
;; Takes two images and produces true if the first is larger than the second (larger means both width and height is larger than the other)

(check-expect (larger-image (rectangle 40 40 "solid" "red") (rectangle 20 5 "solid" "red")) true)
(check-expect (larger-image (square 40 "solid" "red") (square 40 "solid" "red")) false)
(check-expect (larger-image (circle 40 "solid" "red") (circle 50 "solid" "red")) false)
(check-expect (larger-image (rectangle 1 1 "solid" "red") (rectangle 20 5 "solid" "red")) false)

;; (defind (compareImgs img1 img2) true) ;this is stub

;; (defind (compareImgs img1 img2) true)
;;         (... img1 img2))

(define (larger-image img1 img2)
  (and (> (image-width img1) (image-width img2))
       (> (image-height img1) (image-height img2))))
  
```
*__Question:__ Use predicates (i) through (iv) to answer questions*

i.

!['image'](Exercise-8.2.1-image1.png)

ii.

!['image'](Exercise-8.2.1-image2.png)

iii.

!['image'](Exercise-8.2.1-image3.png)

iv.

!['image'](Exercise-8.2.1-image4.png)


*__Answer:__*
<br>
- a. Draw the Karnaugh maps for f and f_.
    - i:
        - f:
        
        !['img.png](img.png)
        - f_:
          
        !['img_1.png](img_1.png)
        
    - ii:
        - f:
          
        ![img_2.png](img_2.png)
        - f_:
          
        ![img_3.png](img_3.png)
        
    - iii:
        - f:
          
        ![img_4.png](img_4.png)

        - f_:

        ![img_5.png](img_5.png)
      
    - iv:
        -f:
      
        ![img_6.png](img_6.png)
      
        -f_:
      
        ![img_7.png](img_7.png)
    
<br>

- b. Find the nonredundant prime implicant representation for f and
  f_.
  - i:
    - f = b(-c)
    - f_ = (-b) + c
    
  - ii:
    - f = (-a)(-b)(-c)(-d) + abcd
    - f_ = (-a)d + c(-d) + b(-c) + a(-b)
  - iii:
    - f = ab + (-b)c
    - f_ = (-a)b + (-b)(-c)
  - iv:
    - f = (-a)(-c) + bd + (-c)d
    - f_ = a(-d) + c(-d) + (-b)c
    
<br>

- c. Give a test set that satisfies Implicant Coverage (IC) for f.
    - i:
      - Implicants: {(-b), c, b(-c)}
      - T = {xTF, xFT}
    - ii:
      - Implicants: {(-a)(-b)(-c)(-d), abcd, (-a)d, c(-d), b(-c), a(-b)}
      - T = {FFFF, TTTT, FTFT, TFTF}
    - iii:
      - Implicants: {(-b)c, (-a)b, (-b)(-c)}
      - T = {TT-, -FT, FT-, -FF}
    - iv:
        - Implicants: {(-a)(-c), bd, (-c)d, a(-d), c(-d), (-b)c}
        - T = {FTFT, TFTF}
    


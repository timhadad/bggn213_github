# Class06 10.18.24
Tim

``` r
ADD <- function (x,y) {x + y}
```

``` r
ADD(1,1)
```

    [1] 2

``` r
ADD(x=1, y=100)
```

    [1] 101

``` r
ADD(c(100,1,100),1)
```

    [1] 101   2 101

``` r
add <- function (x,y=1) {x + y}
add(10)
```

    [1] 11

``` r
add(1,1)
```

    [1] 2

# Q. make a function “GENERATE_DNA()” that makes a random nucluotide seq of any length

# a second function

``` r
bases<- c("A", "C", "G","T")
sequence <- sample(bases, size=5, replace = TRUE)
```

``` r
generate_dna <- sample(bases, size=100, replace = TRUE, prob = NULL)
generate_dna
```

      [1] "G" "C" "C" "C" "G" "T" "G" "A" "C" "G" "A" "G" "T" "G" "A" "T" "T" "G"
     [19] "C" "A" "A" "A" "T" "A" "A" "C" "C" "C" "G" "G" "T" "A" "G" "G" "T" "A"
     [37] "G" "C" "C" "G" "A" "T" "A" "G" "G" "A" "A" "G" "T" "T" "G" "G" "G" "A"
     [55] "C" "T" "G" "T" "A" "A" "A" "G" "T" "G" "A" "C" "C" "G" "G" "A" "T" "G"
     [73] "T" "A" "A" "G" "A" "A" "T" "A" "G" "A" "T" "G" "T" "G" "C" "T" "C" "A"
     [91] "C" "T" "A" "T" "A" "A" "T" "C" "T" "A"

``` r
generate_dna <- function(length) {bases<- c("A", "C", "G","T")
sequence <- sample(bases, size=length, replace = TRUE) 
return(sequence)}
```

``` r
aa <- unique(bio3d::aa.table$aa1)[1:20]
```

``` r
generate_protien <- function(length) {bases<- c("A", "C", "G","T")
sequence <- sample(aa, size=length, replace = TRUE)
sequence <- paste(sequence,collapse = "")
return(sequence)}
```

``` r
generate_protien(6)
```

    [1] "IQFLDH"

``` r
answer <- sapply(6:12, generate_protien)
answer
```

    [1] "VAHMKI"       "CCEFEME"      "HNYAPYMV"     "GFQIWTHKD"    "HVCPKRYIIV"  
    [6] "GMFIWQQCHMR"  "ESLNMNHDAYQW"

``` r
paste(">id.",6:12)
```

    [1] ">id. 6"  ">id. 7"  ">id. 8"  ">id. 9"  ">id. 10" ">id. 11" ">id. 12"

``` r
paste(">id.",6:12, sep = "")
```

    [1] ">id.6"  ">id.7"  ">id.8"  ">id.9"  ">id.10" ">id.11" ">id.12"

``` r
paste(">id.",6:12,"\n",answer, sep = "")
```

    [1] ">id.6\nVAHMKI"        ">id.7\nCCEFEME"       ">id.8\nHNYAPYMV"     
    [4] ">id.9\nGFQIWTHKD"     ">id.10\nHVCPKRYIIV"   ">id.11\nGMFIWQQCHMR" 
    [7] ">id.12\nESLNMNHDAYQW"

``` r
cat(paste(">id.",6:12,"\n",answer, sep = ""))
```

    >id.6
    VAHMKI >id.7
    CCEFEME >id.8
    HNYAPYMV >id.9
    GFQIWTHKD >id.10
    HVCPKRYIIV >id.11
    GMFIWQQCHMR >id.12
    ESLNMNHDAYQW

``` r
cat(paste(">id.",6:12,"\n",answer), sep="\n")
```

    >id. 6 
     VAHMKI
    >id. 7 
     CCEFEME
    >id. 8 
     HNYAPYMV
    >id. 9 
     GFQIWTHKD
    >id. 10 
     HVCPKRYIIV
    >id. 11 
     GMFIWQQCHMR
    >id. 12 
     ESLNMNHDAYQW

``` r
cat(paste(">id.",6:12,"\n",answer, sep=""), sep="\n")
```

    >id.6
    VAHMKI
    >id.7
    CCEFEME
    >id.8
    HNYAPYMV
    >id.9
    GFQIWTHKD
    >id.10
    HVCPKRYIIV
    >id.11
    GMFIWQQCHMR
    >id.12
    ESLNMNHDAYQW

\`\`\`

How many incomplete registrants?

    ## [1] 2

How many total registrants?

    ## [1] 12

Summary statistics for may meeting thus far

    summary(df$`Do you agree to abide by the event Code of Conduct?`)

    ## Yes 
    ##  12

    summary(df$`Which Team are you a member of?`)

    ##                                  Data Stewards 
    ##                                              1 
    ## Team Carbon (PI: Issac Kohane & Paul Avillach) 
    ##                                              4 
    ##                  Team Copper (PI: Titus Brown) 
    ##                                              3 
    ##          Team Oxygen (PI: Lucila Ohno-Machado) 
    ##                                              2 
    ##                 Team Sodium (PI: Merce Crosas) 
    ##                                              2

    summary(df$`Do you have any dietary restrictions?`)

    ##                          Gluten-free                              no pork 
    ##                                    1                                    1 
    ##                      No restrictions No restrictions, Allergic to seafood 
    ##                                    9                                    1

    summary(df$`Do you agree to video recording?`)

    ## Yes, I agree to the video release 
    ##                                12

    # maybe shown as `-`
    summary(df$`Do you need assistance with childcare (reimbursements, accomdations)?`)

    ##   -  no yes 
    ##   1  10   1

How many incomplete registrants?

    ## [1] 2

How many total registrants?

    ## [1] 22

Summary statistics for may meeting thus far

    summary(df$`Do you agree to abide by the event Code of Conduct?`)

    ## Yes 
    ##  22

    summary(df$`Which Team are you a member of?`)

    ##                                  Data Stewards 
    ##                                              4 
    ##                                            NIH 
    ##                                              1 
    ## Team Carbon (PI: Issac Kohane & Paul Avillach) 
    ##                                              4 
    ##                  Team Copper (PI: Titus Brown) 
    ##                                              4 
    ##                Team Nitrogen (PI: Avi Ma'ayan) 
    ##                                              3 
    ##          Team Oxygen (PI: Lucila Ohno-Machado) 
    ##                                              2 
    ##                 Team Sodium (PI: Merce Crosas) 
    ##                                              2 
    ##        Team Xenon (PI: Brandi Davis-Dusenbery) 
    ##                                              1 
    ##              Team Yttrium (PI: Jennifer Ytrri) 
    ##                                              1

    summary(df$`Do you have any dietary restrictions?`)

    ##                          Gluten-free                    Gluten-free, Keto 
    ##                                    1                                    1 
    ##                              no pork                      No restrictions 
    ##                                    1                                   15 
    ## No restrictions, Allergic to seafood                                Vegan 
    ##                                    1                                    2 
    ##                           Vegetarian 
    ##                                    1

    summary(df$`Do you agree to video recording?`)

    ## Yes, I agree to the video release 
    ##                                22

    # maybe shown as `-`
    summary(df$`Do you need assistance with childcare (reimbursements, accomdations)?`)

    ##   -  no yes 
    ##   3  18   1

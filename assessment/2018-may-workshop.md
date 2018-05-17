How many incomplete registrants?

    ## [1] 1

How many total registrants?

    ## [1] 47

Summary statistics for may meeting thus far

    summary(df$`Do you agree to abide by the event Code of Conduct?`) 

    ## Yes 
    ##  47

    summary(df$`Team`)

    ##         Argon       Calcium        Carbon        Copper Data Stewards 
    ##             3             5             4             6             6 
    ##        Helium           NIH      Nitrogen        Oxygen        Sodium 
    ##             6             2             5             3             2 
    ##         Xenon       Yttrium 
    ##             4             1

    summary(df$`Do you have any dietary restrictions?`)

    ##                                    -                          Gluten-free 
    ##                                    1                                    1 
    ##                    Gluten-free, Keto                              no pork 
    ##                                    1                                    1 
    ##                      No restrictions No restrictions, Allergic to seafood 
    ##                                   37                                    1 
    ##                                Vegan                           Vegetarian 
    ##                                    2                                    3

    summary(df$`Do you agree to video recording?`)

    ## Yes, I agree to the video release 
    ##                                47

    # maybe/unsure shown as `-`
    summary(df$`Do you need assistance with childcare (reimbursements, accomdations)?`)

    ##    Length     Class      Mode 
    ##        47 character character

Reconciling the may registrants, the Google onboarding form, and their
Github handles. Of 47 registratns, 24 emails matched the Google sheet,
and 22 of those have GitHub accounts.

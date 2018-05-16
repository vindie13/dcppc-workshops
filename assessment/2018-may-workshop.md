How many incomplete registrants?

    ## [1] 3

How many total registrants?

    ## [1] 36

    #names(df)[7]<-"Team"
    df$`Which Team are you a member of?` <- ifelse(grepl("Data Stewards", df$`Which Team are you a member of?`), "Data Stewards",
                      ifelse(grepl("NIH", df$`Which Team are you a member of?`), "NIH",
                      ifelse(grepl("Carbon", df$`Which Team are you a member of?`), "Carbon",
                      ifelse(grepl("Copper", df$`Which Team are you a member of?`), "Copper",
                      ifelse(grepl("Nitrogen", df$`Which Team are you a member of?`), "Nitrogen",
                      ifelse(grepl("Sodium", df$`Which Team are you a member of?`), "Sodium",
                      ifelse(grepl("Xenon", df$`Which Team are you a member of?`), "Xenon",
                      ifelse(grepl("Yttrium", df$`Which Team are you a member of?`), "Yttrium", 
                      ifelse(grepl("Argon", df$`Which Team are you a member of?`), "Argon",
                      ifelse(grepl("Calcium", df$`Which Team are you a member of?`), "Calcium",
                      ifelse(grepl("Helium", df$`Which Team are you a member of?`), "Helium",
                      ifelse(grepl("Phosphorus", df$`Which Team are you a member of?`), "Phosphorus", "Other"))))))))))))
    df$`Which Team are you a member of?` <- as.factor(as.character(df$`Which Team are you a member of?`))

    names(df)[7]<-"Team"

Summary statistics for may meeting thus far

    summary(df$`Do you agree to abide by the event Code of Conduct?`) 

    ## Yes 
    ##  36

    summary(df$`Team`)

    ##       Calcium        Carbon        Copper Data Stewards        Helium 
    ##             3             4             4             6             4 
    ##           NIH      Nitrogen         Other        Sodium         Xenon 
    ##             2             4             3             2             3 
    ##       Yttrium 
    ##             1

    summary(df$`Do you have any dietary restrictions?`)

    ##                          Gluten-free                    Gluten-free, Keto 
    ##                                    1                                    1 
    ##                              no pork                      No restrictions 
    ##                                    1                                   29 
    ## No restrictions, Allergic to seafood                                Vegan 
    ##                                    1                                    2 
    ##                           Vegetarian 
    ##                                    1

    summary(df$`Do you agree to video recording?`)

    ## Yes, I agree to the video release 
    ##                                36

    # maybe/unsure shown as `-`
    summary(df$`Do you need assistance with childcare (reimbursements, accomdations)?`)

    ##    Length     Class      Mode 
    ##        36 character character


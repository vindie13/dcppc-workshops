    summary <- attendees %>%
      group_by(Team) %>%
      summarize (n = n())
    summary <- as.data.frame(summary)
    #summary

Summary statistics for may meeting thus far

    ##  Make factors
    cols <- c(6:11) # character columns to turn to factors
    df[cols] <- lapply(df[cols], factor) # set as factor
    summary(df$`Do you agree to abide by the event Code of Conduct?`) 

    ## Yes 
    ##  15

    summary(df$`Do you have any dietary restrictions?`)

    ##                                                                                       Keto 
    ##                                                                                          1 
    ##                                                                            No restrictions 
    ##                                                                                         12 
    ## No restrictions, Dietary restrictions -- need other categories -- no pork or bacon for me! 
    ##                                                                                          1 
    ##                                                                                      Vegan 
    ##                                                                                          1

    summary(df$`Do you agree to video recording?`)

    ## Yes, I agree to the video release 
    ##                                15

    summary(df$`Do you need assistance with childcare (reimbursements, accomdations)?`)

    ## maybe/unsure           no          yes 
    ##            1           13            1

    summary(df$`Are you interested in attending a group dinner on Wed. July 25?`)

    ##   No  Yes NA's 
    ##    1   13    1

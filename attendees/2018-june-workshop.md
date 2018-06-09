    summary <- attendees %>%
      group_by(Team) %>%
      summarize (n = n())
    summary <- as.data.frame(summary)
    summary

    ##            Team n
    ## 1       Calcium 2
    ## 2        Carbon 1
    ## 3        Copper 3
    ## 4 Data Stewards 3
    ## 5        Helium 2
    ## 6        Oxygen 1
    ## 7        Sodium 1
    ## 8         Xenon 2
    ## 9       Yttrium 1

Summary statistics for may meeting thus far

    ##  Make factors
    cols <- c(5:12) # character columns to turn to factors
    df[cols] <- lapply(df[cols], factor) # set as factor
    summary(df$`Do you agree to abide by the event Code of Conduct?`) 

    ## Yes 
    ##  16

    summary(df$`Do you have any dietary restrictions?`)

    ##            No restrictions No restrictions, pork free 
    ##                         12                          1 
    ##                      Vegan                 Vegetarian 
    ##                          2                          1

    summary(df$`Do you agree to video recording?`)

    ## No, I'd rather not have the video released, thanks 
    ##                                                  1 
    ##                  Yes, I agree to the video release 
    ##                                                 15

    summary(df$`Do you need assistance with childcare (reimbursements, accomdations)?`)

    ##  no yes 
    ##  14   2

    summary(df$`Will you be participating in the workshop, hackathon, or both?`)

    ##                                                              - 
    ##                                                              1 
    ##                                       A combination of the two 
    ##                                                              6 
    ## Workshop only (lightning talks in AM, breakout sessions in PM) 
    ##                                                              9

    summary(df$`Have you registered for \"CollaborationFest\", too?`)

    ##      -     No Unsure    Yes 
    ##      1      5      5      5

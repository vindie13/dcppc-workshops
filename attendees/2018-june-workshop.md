    summary <- attendees %>%
      group_by(Team) %>%
      summarize (n = n())
    summary <- as.data.frame(summary)
    #summary

Summary statistics for may meeting thus far

    ##  Make factors
    cols <- c(5:12) # character columns to turn to factors
    df[cols] <- lapply(df[cols], factor) # set as factor
    summary(df$`Do you agree to abide by the event Code of Conduct?`) 

    ## Yes 
    ##  37

    summary(df$`Do you have any dietary restrictions?`)

    ##                     No restrictions No restrictions, lactose intolerant 
    ##                                  29                                   1 
    ##   No restrictions, no pork products          No restrictions, pork free 
    ##                                   1                                   1 
    ##                               Vegan                          Vegetarian 
    ##                                   2                                   3

    summary(df$`Do you agree to video recording?`)

    ## No, I'd rather not have the video released, thanks 
    ##                                                  4 
    ##                  Yes, I agree to the video release 
    ##                                                 33

    summary(df$`Do you need assistance with childcare (reimbursements, accomdations)?`)

    ## maybe/unsure           no          yes 
    ##            1           33            3

    summary(df$`Will you be participating in the workshop, hackathon, or both?`)

    ##                                                              - 
    ##                                                              2 
    ##                                       A combination of the two 
    ##                                                             18 
    ##                      Hackathon only (hacking all day each day) 
    ##                                                              2 
    ## Workshop only (lightning talks in AM, breakout sessions in PM) 
    ##                                                             15

    summary(df$`Have you registered for \"CollaborationFest\", too?`)

    ##      -     No Unsure    Yes 
    ##      1     10      7     19

How many incomplete registrants?

    ## [1] 4

How many total registrants?

    ## [1] 31

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

Summary statistics for may meeting thus far

    summary(df$`Do you agree to abide by the event Code of Conduct?`) 

    ## Yes 
    ##  31

    summary(df$`Which Team are you a member of?`)

    ##        Carbon        Copper Data Stewards        Helium           NIH 
    ##             4             4             6             3             2 
    ##      Nitrogen         Other        Sodium         Xenon       Yttrium 
    ##             4             3             2             2             1

    summary(df$`Do you have any dietary restrictions?`)

    ##                          Gluten-free                    Gluten-free, Keto 
    ##                                    1                                    1 
    ##                              no pork                      No restrictions 
    ##                                    1                                   24 
    ## No restrictions, Allergic to seafood                                Vegan 
    ##                                    1                                    2 
    ##                           Vegetarian 
    ##                                    1

    summary(df$`Do you agree to video recording?`)

    ## Yes, I agree to the video release 
    ##                                31

    # maybe/unsure shown as `-`
    summary(df$`Do you need assistance with childcare (reimbursements, accomdations)?`)

    ##    Length     Class      Mode 
    ##        31 character character

    attendees <- df %>% 
      select(`Ticket Full Name`, `Which Team are you a member of?`) %>%  
      arrange(`Which Team are you a member of?`)
    attendees <- as.data.frame(attendees)
    attendees

    ##          Ticket Full Name Which Team are you a member of?
    ## 1        Gregoire Versmee                          Carbon
    ## 2           Laura VERSMEE                          Carbon
    ## 3           Paul Avillach                          Carbon
    ## 4           Jessica Lyons                          Carbon
    ## 5            Rayna Harris                          Copper
    ## 6            Brad Chapman                          Copper
    ## 7      Sarah Wait Zaranek                          Copper
    ## 8          Rebecca Calisi                          Copper
    ## 9          Kristin Ardlie                   Data Stewards
    ## 10     Christopher Tabone                   Data Stewards
    ## 11            Ben Heavner                   Data Stewards
    ## 12               Josh Bis                   Data Stewards
    ## 13           Jared Nedzel                   Data Stewards
    ## 14         Jeffrey DePons                   Data Stewards
    ## 15             Stan Ahalt                          Helium
    ## 16        Claris Castillo                          Helium
    ## 17            Jeremy Yang                          Helium
    ## 18 valentina di francesco                             NIH
    ## 19          Chip Schwartz                             NIH
    ## 20          Daniel Clarke                        Nitrogen
    ## 21            Avi Ma'ayan                        Nitrogen
    ## 22         Sherry Jenkins                        Nitrogen
    ## 23    Megan Wojciechowicz                        Nitrogen
    ## 24        Anupama Gururaj                           Other
    ## 25          Firat Tiryaki                           Other
    ## 26          Cole Davisson                           Other
    ## 27           Merce Crosas                          Sodium
    ## 28         Daniel S. Katz                          Sodium
    ## 29            Alison Leaf                           Xenon
    ## 30         Saiju Pyarajan                           Xenon
    ## 31      Kristen Cleveland                         Yttrium

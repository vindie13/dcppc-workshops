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

    attendees <- df %>% 
      select(`Ticket Full Name`, `Team`) %>%  
      arrange(`Team`)
    attendees <- as.data.frame(attendees)
    attendees

    ##          Ticket Full Name          Team
    ## 1              Zac Flamig       Calcium
    ## 2           Cricket Sloan       Calcium
    ## 3             Walt Shands       Calcium
    ## 4        Gregoire Versmee        Carbon
    ## 5           Laura VERSMEE        Carbon
    ## 6           Paul Avillach        Carbon
    ## 7           Jessica Lyons        Carbon
    ## 8            Rayna Harris        Copper
    ## 9            Brad Chapman        Copper
    ## 10     Sarah Wait Zaranek        Copper
    ## 11         Rebecca Calisi        Copper
    ## 12         Kristin Ardlie Data Stewards
    ## 13     Christopher Tabone Data Stewards
    ## 14            Ben Heavner Data Stewards
    ## 15               Josh Bis Data Stewards
    ## 16           Jared Nedzel Data Stewards
    ## 17         Jeffrey DePons Data Stewards
    ## 18             Stan Ahalt        Helium
    ## 19        Claris Castillo        Helium
    ## 20            Jeremy Yang        Helium
    ## 21            Sarah Davis        Helium
    ## 22 valentina di francesco           NIH
    ## 23          Chip Schwartz           NIH
    ## 24          Daniel Clarke      Nitrogen
    ## 25            Avi Ma'ayan      Nitrogen
    ## 26         Sherry Jenkins      Nitrogen
    ## 27    Megan Wojciechowicz      Nitrogen
    ## 28        Anupama Gururaj         Other
    ## 29          Firat Tiryaki         Other
    ## 30          Cole Davisson         Other
    ## 31           Merce Crosas        Sodium
    ## 32         Daniel S. Katz        Sodium
    ## 33            Alison Leaf         Xenon
    ## 34         Saiju Pyarajan         Xenon
    ## 35        Ross Rounsevell         Xenon
    ## 36      Kristen Cleveland       Yttrium

    attendees <- df %>% 
      select(`Ticket Full Name`, `Team`) %>%  
      arrange(`Ticket Full Name`)
    attendees <- as.data.frame(attendees)
    attendees

    ##          Ticket Full Name          Team
    ## 1             Alison Leaf         Xenon
    ## 2         Anupama Gururaj         Other
    ## 3             Avi Ma'ayan      Nitrogen
    ## 4             Ben Heavner Data Stewards
    ## 5            Brad Chapman        Copper
    ## 6           Chip Schwartz           NIH
    ## 7      Christopher Tabone Data Stewards
    ## 8         Claris Castillo        Helium
    ## 9           Cole Davisson         Other
    ## 10          Cricket Sloan       Calcium
    ## 11          Daniel Clarke      Nitrogen
    ## 12         Daniel S. Katz        Sodium
    ## 13          Firat Tiryaki         Other
    ## 14       Gregoire Versmee        Carbon
    ## 15           Jared Nedzel Data Stewards
    ## 16         Jeffrey DePons Data Stewards
    ## 17            Jeremy Yang        Helium
    ## 18          Jessica Lyons        Carbon
    ## 19               Josh Bis Data Stewards
    ## 20      Kristen Cleveland       Yttrium
    ## 21         Kristin Ardlie Data Stewards
    ## 22          Laura VERSMEE        Carbon
    ## 23    Megan Wojciechowicz      Nitrogen
    ## 24           Merce Crosas        Sodium
    ## 25          Paul Avillach        Carbon
    ## 26           Rayna Harris        Copper
    ## 27         Rebecca Calisi        Copper
    ## 28        Ross Rounsevell         Xenon
    ## 29         Saiju Pyarajan         Xenon
    ## 30            Sarah Davis        Helium
    ## 31     Sarah Wait Zaranek        Copper
    ## 32         Sherry Jenkins      Nitrogen
    ## 33             Stan Ahalt        Helium
    ## 34 valentina di francesco           NIH
    ## 35            Walt Shands       Calcium
    ## 36             Zac Flamig       Calcium

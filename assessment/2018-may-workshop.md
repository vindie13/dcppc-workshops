How many incomplete registrants?

    ## [1] 1

How many total registrants?

    ## [1] 46

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
    ##  46

    summary(df$`Team`)

    ##         Argon       Calcium        Carbon        Copper Data Stewards 
    ##             3             5             4             5             6 
    ##        Helium           NIH      Nitrogen         Other        Sodium 
    ##             6             2             5             3             2 
    ##         Xenon       Yttrium 
    ##             4             1

    summary(df$`Do you have any dietary restrictions?`)

    ##                                    -                          Gluten-free 
    ##                                    1                                    1 
    ##                    Gluten-free, Keto                              no pork 
    ##                                    1                                    1 
    ##                      No restrictions No restrictions, Allergic to seafood 
    ##                                   36                                    1 
    ##                                Vegan                           Vegetarian 
    ##                                    2                                    3

    summary(df$`Do you agree to video recording?`)

    ## Yes, I agree to the video release 
    ##                                46

    # maybe/unsure shown as `-`
    summary(df$`Do you need assistance with childcare (reimbursements, accomdations)?`)

    ##    Length     Class      Mode 
    ##        46 character character

    attendees <- df %>% 
      select(`Ticket Full Name`, `Team`) %>%  
      arrange(`Team`)
    attendees <- as.data.frame(attendees)
    attendees

    ##          Ticket Full Name          Team
    ## 1            Ravi Madduri         Argon
    ## 2             Rick Wagner         Argon
    ## 3          Carl Kesselman         Argon
    ## 4              Zac Flamig       Calcium
    ## 5           Cricket Sloan       Calcium
    ## 6             Walt Shands       Calcium
    ## 7        Ilyana Rosenberg       Calcium
    ## 8         Kristin Anderka       Calcium
    ## 9        Gregoire Versmee        Carbon
    ## 10          Laura VERSMEE        Carbon
    ## 11          Paul Avillach        Carbon
    ## 12          Jessica Lyons        Carbon
    ## 13     Sasha Wait Zaranek        Copper
    ## 14           Rayna Harris        Copper
    ## 15           Brad Chapman        Copper
    ## 16     Sarah Wait Zaranek        Copper
    ## 17         Rebecca Calisi        Copper
    ## 18         Kristin Ardlie Data Stewards
    ## 19     Christopher Tabone Data Stewards
    ## 20            Ben Heavner Data Stewards
    ## 21               Josh Bis Data Stewards
    ## 22           Jared Nedzel Data Stewards
    ## 23         Jeffrey DePons Data Stewards
    ## 24             Stan Ahalt        Helium
    ## 25        Claris Castillo        Helium
    ## 26            Jeremy Yang        Helium
    ## 27            Sarah Davis        Helium
    ## 28            Ray Idaszak        Helium
    ## 29              Steve Cox        Helium
    ## 30 valentina di francesco           NIH
    ## 31          Chip Schwartz           NIH
    ## 32          Daniel Clarke      Nitrogen
    ## 33            Avi Ma'ayan      Nitrogen
    ## 34         Sherry Jenkins      Nitrogen
    ## 35    Megan Wojciechowicz      Nitrogen
    ## 36          Juergen Klenk      Nitrogen
    ## 37        Anupama Gururaj         Other
    ## 38          Firat Tiryaki         Other
    ## 39          Cole Davisson         Other
    ## 40           Merce Crosas        Sodium
    ## 41         Daniel S. Katz        Sodium
    ## 42            Alison Leaf         Xenon
    ## 43         Saiju Pyarajan         Xenon
    ## 44        Ross Rounsevell         Xenon
    ## 45           Sarper Avcil         Xenon
    ## 46      Kristen Cleveland       Yttrium

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
    ## 6          Carl Kesselman         Argon
    ## 7           Chip Schwartz           NIH
    ## 8      Christopher Tabone Data Stewards
    ## 9         Claris Castillo        Helium
    ## 10          Cole Davisson         Other
    ## 11          Cricket Sloan       Calcium
    ## 12          Daniel Clarke      Nitrogen
    ## 13         Daniel S. Katz        Sodium
    ## 14          Firat Tiryaki         Other
    ## 15       Gregoire Versmee        Carbon
    ## 16       Ilyana Rosenberg       Calcium
    ## 17           Jared Nedzel Data Stewards
    ## 18         Jeffrey DePons Data Stewards
    ## 19            Jeremy Yang        Helium
    ## 20          Jessica Lyons        Carbon
    ## 21               Josh Bis Data Stewards
    ## 22          Juergen Klenk      Nitrogen
    ## 23      Kristen Cleveland       Yttrium
    ## 24        Kristin Anderka       Calcium
    ## 25         Kristin Ardlie Data Stewards
    ## 26          Laura VERSMEE        Carbon
    ## 27    Megan Wojciechowicz      Nitrogen
    ## 28           Merce Crosas        Sodium
    ## 29          Paul Avillach        Carbon
    ## 30           Ravi Madduri         Argon
    ## 31            Ray Idaszak        Helium
    ## 32           Rayna Harris        Copper
    ## 33         Rebecca Calisi        Copper
    ## 34            Rick Wagner         Argon
    ## 35        Ross Rounsevell         Xenon
    ## 36         Saiju Pyarajan         Xenon
    ## 37            Sarah Davis        Helium
    ## 38     Sarah Wait Zaranek        Copper
    ## 39           Sarper Avcil         Xenon
    ## 40     Sasha Wait Zaranek        Copper
    ## 41         Sherry Jenkins      Nitrogen
    ## 42             Stan Ahalt        Helium
    ## 43              Steve Cox        Helium
    ## 44 valentina di francesco           NIH
    ## 45            Walt Shands       Calcium
    ## 46             Zac Flamig       Calcium

    write.csv(attendees, "./data/attendees.csv")

    names(df)[10]<-"Childcare"
    childcare <- df %>% 
      select(`Ticket Full Name`, `Childcare`) %>%  
      filter(Childcare != "no")
    childcare <- as.data.frame(childcare)
    childcare

    ##    Ticket Full Name    Childcare
    ## 1  Gregoire Versmee            -
    ## 2       Alison Leaf            -
    ## 3       Ben Heavner            -
    ## 4    Jeffrey DePons          yes
    ## 5   Claris Castillo maybe/unsure
    ## 6     Cricket Sloan            -
    ## 7       Walt Shands            -
    ## 8      Ravi Madduri            -
    ## 9       Rick Wagner            -
    ## 10   Carl Kesselman            -

    #This is the percent of females registered
    15/36

    ## [1] 0.4166667

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

    ##          Ticket Full Name          Team             GitHub
    ## 1      Sasha Wait Zaranek        Copper               <NA>
    ## 2        Gregoire Versmee        Carbon               <NA>
    ## 3           Laura VERSMEE        Carbon               <NA>
    ## 4            Rayna Harris        Copper       raynamharris
    ## 5           Paul Avillach        Carbon           avillach
    ## 6            Merce Crosas        Sodium               <NA>
    ## 7           Jessica Lyons        Carbon               <NA>
    ## 8          Daniel S. Katz        Sodium        danielskatz
    ## 9          Kristin Ardlie Data Stewards            kardlie
    ## 10        Anupama Gururaj        Oxygen          aegururaj
    ## 11          Firat Tiryaki        Oxygen               <NA>
    ## 12           Brad Chapman        Copper               <NA>
    ## 13     Christopher Tabone Data Stewards        christabone
    ## 14            Alison Leaf         Xenon                   
    ## 15            Ben Heavner Data Stewards               <NA>
    ## 16     Sarah Wait Zaranek        Copper       swzCuroverse
    ## 17 valentina di francesco           NIH               <NA>
    ## 18          Daniel Clarke      Nitrogen               <NA>
    ## 19      Kristen Cleveland       Yttrium               <NA>
    ## 20               Josh Bis Data Stewards            joshbis
    ## 21            Avi Ma'ayan      Nitrogen          AviMaayan
    ## 22         Sherry Jenkins      Nitrogen     sherry-jenkins
    ## 23         Saiju Pyarajan         Xenon               <NA>
    ## 24          Cole Davisson        Oxygen         cmdavisson
    ## 25           Jared Nedzel Data Stewards            jnedzel
    ## 26             Stan Ahalt        Helium          stanahalt
    ## 27    Megan Wojciechowicz      Nitrogen meganwojciechowicz
    ## 28          Chip Schwartz           NIH               <NA>
    ## 29         Jeffrey DePons Data Stewards               <NA>
    ## 30        Claris Castillo        Helium           clarisca
    ## 31         Rebecca Calisi        Copper               <NA>
    ## 32            Jeremy Yang        Helium               <NA>
    ## 33        Ross Rounsevell         Xenon               <NA>
    ## 34             Zac Flamig       Calcium            zflamig
    ## 35            Sarah Davis        Helium          davissn30
    ## 36          Cricket Sloan       Calcium       cricketsloan
    ## 37            Walt Shands       Calcium               <NA>
    ## 38            Ray Idaszak        Helium            rayi113
    ## 39              Steve Cox        Helium               <NA>
    ## 40           Ravi Madduri         Argon            madduri
    ## 41            Rick Wagner         Argon               <NA>
    ## 42         Carl Kesselman         Argon               <NA>
    ## 43           Sarper Avcil         Xenon                   
    ## 44          Juergen Klenk      Nitrogen            jaklenk
    ## 45       Ilyana Rosenberg       Calcium               <NA>
    ## 46        Kristin Anderka       Calcium          keanderka
    ## 47           Charles Reid        Copper               <NA>

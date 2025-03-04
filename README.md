# DOCS1
Objective: TO find solution for multilangual support for the application like (English,Hindi,Marathi)
(Dynamic Translation for Content)
If you want to translate the actual data (like product descriptions, comments, etc.) into Marathi or Hindi, you have to pass each item to a translation service (like LibreTranslate, Google Translate, etc.) before rendering it in FlatList.

    Option1. Localization (Use i18/next package for applying language for from backend where files for English(en), Hindi(hn),Marathi(mr) are storing the objects of each table listed in database.
             like below: 
                        common.json=(store the common button used in aplication).
                        About.json = (common for everyone).
                        Home.json = (Home page file also can be common for all users ) 

             these files can be converted into selected langauge by user prefence for that we have to create files like this 
        src->
             locales->
                        en->
                           common.json
                           About.json
                           Home.json

                        hn->
                           common.json
                           About.json
                           Home.json
                        mr-> 
                           common.json
                           About.json
                           Home.json
             after that we can use this files and store it in our backend server with complete controll and unlimited usage.


     Option2.(MyMemory: API)
     
            Usage:   ➡️MyMemory tracks it usage in words. This means that it doesn't matter how many requests you submit to consult the archive, but the weight of each request.
                     ➡️Free, anonymous usage is limited to 5000 chars/day.
                     ➡️After providing the email address we can use 50,000 char/day limit.

            Limitation:     ❌ Does not support "Marathi" Language.
            
     Option3.(LibreTranslate (Free Self-Hosted Option))
            Usage: ➡️ You can self-host LibreTranslate and call it directly.
                   ➡️ Free if self-hosted.
                   ➡️ Works with React Native (regular fetch request).
                   
            Limitation:    ❌ Does not support to "Marathi" language but their is option for trained a "lang model"

     Option4.(Hybrid Approch)
     
     we can use i18next for UI texts like "Product Name", "Description", "Add to Cart" (labels).
     Use Translation API (MyMemory,LibreTranslate/Google Translate) only for dynamic data like product titles, descriptions, user comments,user names, etc.

      limitation:
      ➡️ Works for dynamic content from API.
      ➡️ Supports full multi-language content.
      ❌ Slower because each item is translated via network request.
      ❌ Needs rate-limiting handling if your data list is large.
      ❌ If translation API fails, fallback to English.

     

    

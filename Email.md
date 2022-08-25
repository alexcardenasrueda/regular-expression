# Emails Regex

Examples to Work

- esto.es_un.mail@mail.com
- esto.es_un.mail+complejo@mail.com
- dominio.com
- rodrigo.jimenez@yahoo.com.mx
- ruben@starbucks.com
- esto_no$es_email@dominio.com
- no_se_de_internet3@hotmail.com

First, we should create a regex to obtain the domain

``` @[\w\.\-]{3,}\.\w{2,5}$ ```

Explaination step by step

- ``` @ ``` Find @ character begining match
- ``` [\w\.\-]{3,} ``` Find a word including . and / characters. We must use \ (backSlash) character to skip keyWords to regex
- ``` \. ``` Next find a . character
- ``` \w{2,5}$ ``` Finally find TLD and finish line with $ character

Now that we have this we can think about the user's side of things

``` [\w\._]{5,30}\+?[\w]{0,10} ```

I'm building a class that allows me to any character that be a word plus point or underscore next that this accept alias gmail form.

Then if we join the last two regex, we obtain


``` [\w\._]{5,30}\+?[\w]{0,10}@[\w\.\-]{3,}\.\w{2,5}$ ```

# URL
url: https://www.instagram.com/p/BXB4zsUlW5Z/?taken-by=beco.mx

url: http://instagram.com/p/blablablah

url: http://itam.mx/test

http://instagram.com/p/blablablah

https://www.vanguarsoft.com.ve

http://platzi.com

https://traetelo.net

https://traetelo.net/images archivo.jsp

url: https://subdominio.traetelo.net

url: https://www.instagram.com/p/BXB4zsUlW5Z/?taken-by=beco.mx

url: http://instagram.com/p/blablablah

url: http://itam.mx/test

http://instagram.com/p/blablablah

https://www.google.com.co/

https://sub.dominio.de.alguien.com/archivo.html

https://en.wikipedia.org/wiki/.org

https://cdn-microsoft.org/image/seixo2t9sjl_22.jpg

https://hola.pizza

https://platzi.com/clases/1301-expresiones-regulares/11860-urls9102/ clase

https://api.giphy.com/v1/gifs/search?q=Rick and Morty&limit=10&api_key=DG3hItPp5HIRNC0nit3AOR7eQZAe

http://localhost:3000/something?color1=red&color2=blue

http://localhost:3000/display/post?size=small

 http://localhost:3000/?name=satyam

 http://localhost:3000/scanned?orderid=234

 http://localhost:3000/getUsers?userId=12354411&name=Billy

 http://localhost:3000/getUsers?userId=12354411

http://localhost:3000/search?city=Barcelona

To use regular expressions to match URL we can use as follows

```
https?:\/\/[\w\-\.]+\.\w{2,5}\/?\S*
```

Explain step to step
Match exactly http
Letter “S” can be or can’t be, for this reason we use “?” s?
Follow this is mandatory a character :
Slash character is a reserved character so don’t remember escape this \/\/
Until here we find Strings that contains http:// or https://
After that we need to create a class to indicate a group of characters including (-) and (.), for this add to our regex [\w\-\.]+
This class indicates characters including (-) and (.) and to appear at least once
Next we wanna find a point character to separate TLD (Top level domains. Examples: .com , .org , .mx , etc) \.\2{2,5}
Finally the URL complement can be file names, paths and anything but never there are spaces character so we exclude this spaces in our regex \/?\S*
Copy snipet of code and write regex step to step to see amazing power of regular expressions!

This information can help to understand a little more about regex
http://w3.unpocodetodo.info/utiles/regex.php
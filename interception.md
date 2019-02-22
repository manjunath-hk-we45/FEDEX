# INTERCEPTION

### ❓ Does it works?

      Yes!! We know thick client applications do most of their work on the  client side, but sometimes applications need to access the external resources by using **database drivers or API calls** to get the work done, which can be considered as an attack surface for thick clients as we can sniff its data over the network channel.

{% hint style="info" %}
Intercepting application traffic is a bit different than intercepting web application
{% endhint %}

### ❓How to Intercept?

      We can setup a proxy to intercept application traffic or we can use Wire shark and intercept the communication done by the host in the given network and map the request and response to the application's communication channel or setup a system level proxy using **Burp Suite or Fiddler** \(These can also provide you the  option with MITM attacks and also they intercept sockets!\)

### ❓What to look for  during interception?

* Look for packets which contain credentials either during the  request phase or response phase, which can yield in attacks on authentication, and it can be used to brute forcing with other user credentials and \(if defaults or not changed or if the server is using simple usernames/passwords\) attack can be get sever by escalating the privileges
* Look for database query calls as one can do SQL injection attacks on database to get more information or can compromise the database server
* MITM attack can also be extended by intercepting socket communication and here also we have many attack methods to play with socket security

### \*\*\*\*💸 **TIP**

      Intercept data during application execution and also during initial installation of the application as we can, even intercept the initial server communication of the application as it might include server sending some sensitive information to the client which application can use it in future communication. \(We found a credential which server responded to the client, which client can use in its operational lifetime\)

{% embed url="https://www.paladion.net/blogs/thick-client-testing-toolkit-part-3-tools-testing-techniques-interception-testing" %}






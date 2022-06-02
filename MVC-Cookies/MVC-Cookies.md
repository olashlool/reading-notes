# Reading 28: MVC Cookies

## What is a cookie?
A cookie is data that a server sends to the users web browser, the browser can store it and send that same data back at a future time.

Another approach to storing data in the browser is the Web Storage API.

Cookies are an important part of the web today and improperly managing them can lead to all kinds of issues from poor user experience to security holes.


**Cookies are usually used for 3 purposes:**
- Session management
- Personalization
- Tracking


**Cookies are made up of multiple different parts, each is separated by a semi-colon and tells the server some piece of information:**

- Expires option which tells the server when the cookie expires. 
- Domain option which tells it what domains for which the cookie should be sent. 
- Path option, which tells what URL the cookie uses in the header. 
- Secure option. If a cookie is secure it is sent over HTTPS.

**The lifetime of a cookie can be defined in two ways:**

- Session cookies are deleted when the current session ends. 
- Permanent cookies are deleted at a date specified by the Expires attribute, or after a period of time specified by the Max-Age attribute.

### Cookie prefixes
Cookie Prefixes are a way of "smuggling" information in the name prefix of a cookie to ensure that certain attributes accompany the request to set a cookie.

- __Host-
- __Secure-

**Ways to mitigate attacks involving cookies:**

- Use the HttpOnly attribute to prevent access to cookie values via JavaScript.
- Cookies that are used for sensitive information (such as indicating authentication) should have a short lifetime, with the SameSite attribute set to Strict or Lax. 


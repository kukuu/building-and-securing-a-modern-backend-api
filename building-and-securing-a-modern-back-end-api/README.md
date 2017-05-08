

#  Strategies for Securing APIs - Applications on nodejs


APIs are an emerging technology for integrating applications using web technology.  APIs allow developers to
create an open architecture for sharing functionality and data between
applications.

The problem with APIs is that they often provide a roadmap describing the underlying implementation of an application details that would otherwise
be buried under layers of web app functionality. This can give hackers valuable clues that could lead to attack vectors they might otherwise overlook.

APIs tend to be extremely clear and self-documenting at their best, providing insight into internal objects and even internal database structure all valuable intelligence for hackers.But increased visibility isn’t the only risk APIs introduce. Increasing the number of potential calls also increases the attack surface, meaning that a hacker simply has more to exploit. Risk increases with opportunity.

There are three main attack vectors that hackers target most frequently with APIs. Understanding these will help you to build
safer APIs.

# PIM

##### Parameters

Parameter attacks exploit the data sent into an API, including URL, query parameters, HTTP headers, and/or post content.

The most common of which is a SQL injection attempt to manipulate a system by providing it with inputs that exploit behavior of applications and the infrastructure that supports them (such as databases).

These normally result from developers not carefully checking input into an application. And in contrast to many web apps, APIs often
clearly identify a parameter’s underlying usage by its name, offering enticing clues to even the casual attacker. 


##### Identity

Identity attacks exploit flaws in authentication, authorization, and session tracking. In particular, many of these are the result
of migrating bad practices from the web world into API development.

APIs are identified using keys. They uniquely identify which application is calling an API. API keys are typically hidden inside
the code of a calling client application, and despite best efforts to conceal it on the part of developers, they are generally easy to find and exploit.


##### Man-in-the-Middle

These attacks intercept legitimate transactions and exploit unsigned and/or unencrypted data being sent between the
client and the server. They can reveal confidential information (such as personal data), alter a transaction in flight, or even
replay legitimate transactions.

APIs that are not properly configured using SSL/TLS are highly vulnerable to this form of attack. Unfortunately, the culture
in web design is to leave most communications in the clear, largely because of historical challenges in scaling SSL loads.
Even when SSL/TLS is applied, often it is misconfigured or vulnerable to downgraded attacks that render it ineffective.

Stakes are higher and transport protection is essential to secure data, sessions, and access to functionality.


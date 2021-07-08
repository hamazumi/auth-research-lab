# ![GA Logo](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Auth Research Lab

---

Authentication is a complex and exciting topic that involves using many of the concepts we've already studied as well as several new ideas.

An authentication system allows the registration / signup of new users and allows those users to sign in. It has to be able to identify each user and keep their information private and secure.

Being able to develop secure user login systems is in fact a whole career and life path in and of itself, but understanding the broad concepts of **Auth** is critically import for all developers.

Describing auth flow and understanding key terms are very common **interview questions** for junior developers, so lets take some time to research and understand auth and the related concepts.

## Setup

Fork and clone this repository and answer the questions as you research directly in the README. You do not have to pull request and submit this lab, but you will want to have it on hand for reference in the future.

## Auth Concepts Worksheet

#### Define the following

1. _Authentication_
   The identity of the user is checked to provide access to the system. This process verifies ‘who you are?’ so the user needs to supply login details to authenticate.

2. _Authorization_
   Process of verifying if the authenticated user is authorized to access specific information or be allowed to execute a certain operation. This process determines which permissions the user has.

3. Explain how _authentication_ and _authorization_ are related but distinct concepts.
   Before authorization is done. User must be authenticated with login details. Once there is a match with login details, authorization will check to see what type of access that authenticated user has access to.

4. _Sessions vs Token based auth_
   In Stateful(SESSIONS) authentication, the server creates a session for the user after successfully authenticating. The session id is then stored as a cookie in the user's browser and the user session store in the cache or database. When the client tries to access the server with a given session id, the server attempts to load the user session context for the session store, checks if the session is valid, and decides if the client has to access the desired resource or rejects the request.

   Stateless(TOKEN) is when a token in stored as a cookie or local storage (client-side) and is verified by the server on each request. Since the user session is stored on the client-side, this approach frees the overhead to maintain the user session state.

5. _json web token (also know as a jwt)_
   JWTs are a good way of securely transmitting information between parties because they can be signed, which means you can be sure that the senders are who they say they are. Additionally, the structure of a JWT allows you to verify that the content hasn't been tampered with. jwts ARE NOT hashed or encrypted and anyone can see the information inside of them.

6. _Encoding, encryption and hashing_ along with the uses for and differences between the three

   ENDOING:

   - Transforms data so that it can be properly and safely sent to another system.
   - Can be decoded by anyone.
   - Useful for zipping data into a smaller size.

   ENCRYPTION:

   - Transform data in order to keep it secret from others, e.g. sending someone a letter that only they should read, or securely sending a password over the Internet.
   - Goal is to ensure data can only be used by intended person.
   - Uses cypher to scramble data. Only someone with same cypher can retrieve the data.

   HASHING:

   - Purpose of ensuring integrity, i.e. making it so that if something is changed you can know that it’s changed.
   - Process that can be used to validate the authenticity various types of input. It is widely used in authentication systems to avoid storing plaintext passwords in databases, but is also used to validate files, documents and other types of data.

7. _oAuth_ (pronounced oh-Auth)
   - Open standard for access delegation, commonly used as a way for Internet users to grant websites or applications access to their information on other websites but without giving them the passwords.

#### Explore and then describe the following npm packages:

1. [bcrypt](https://www.npmjs.com/package/bcrypt)

   - Hashing function allows us to build a password security platform and safely store them in a DB.

2. [jsonwebtoken](https://www.npmjs.com/package/jsonwebtoken)
   -An npm package that is used for encoding jwts, signing jwts and decoding jwts.

3. [passport](https://www.npmjs.com/package/passport)

   - Passport is Express-compatible authentication middleware for Node.js.

   - also describe what a _strategy_ is in the context of this npm package
     - Passport uses the concept of strategies to authenticate requests. Strategies can range from verifying username and password credentials, delegated authentication using OAuth (for example, via Facebook or Twitter), or federated authentication using OpenID.

---

## Licensing

1. All content is licensed under a CC-BY-NC-SA 4.0 license.
2. All software code is licensed under GNU GPLv3. For commercial use or alternative licensing, please contact legal@ga.co.

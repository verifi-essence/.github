## Verifi : The complete offline OTP solution


Verifi do 2 step authentication even on the locations where the cellular network is weak or very poor. Verifi will be using a common token to authenticate between the server and the registered user, to increase the security instead of using token directly like the traditional way. 

- System will be generating a cryptographic HMAC hash with the current timestamp in UTC format and the common token for generating the OTP 

- Current timestamp will be rounded off by 30s so the OTP will remain the same for the next 30 seconds. 

- We are using the same process on the server side so the server can allow an OTP for the next 30 seconds.

Verifi Complete Offline OTP Solution comes with product categories involving:

“VERIFI”- THE PLATFORM (FOR USERS)

Verifi generates OTP in users device without having any cellular & internet connection. Basically, user will be able to generate OTP by adding their service accounts via scanning QR or entering secret key manually. “Verifi“ solves the issue faced in remote areas where cellular connections are very weak. And also, this offline authentication technique is far more secured than the traditional cellular OTP system. 

How Verifi is more secure than previous traditional cellular OTP system?

Problem with Traditional OTP system :

    * SIM Swap Security Risk

    * SS7 Technical Flaw

    * Social Engineering Risks

    * Sending OTP Through SMS Can Be Quite Expensive

    * Friction in User Experience

What Verifi Provides:

    * High Security

    * Low Cost when compared to traditional cellular OTP system

    * Works on Both Online & Offline mode

    * Requires no cellular connection

    * Handy to Use, no need to send OTP again & again, at it changes automatically every 30 seconds

    * One-time setup is required only

    * Highly efficient user experience, most of the things happens automatically, no need to put extra-effort for verification

“VERIFI-PWA APP” (FOR USERS)

Verifi-PWA will be used to scan QR or enter secret key, and it will generate the OTP without having any cellular and internet connection, and it will store the key in local storage, also OTP will be changed every 30secs. After connecting to internet, it will store secret key in the Verifi-database in highly encrypted manner.

We created Verifi-PWA because:

   * Short loading time

   * Suitable for both offline & online mode

   * Small size

   * Avoid app aggregators (Google Play, App Store, etc.), no need to install it from app stores. Just simply go to browser, and after visiting   Verifi-Link , click on “Add to Home Screen“ 

   * Instant updates





“VERIFI-PACKAGES“ (PACKAGES TO BE DEPLOYED DIRECTLY ON SERVICE PROVIDERS PLATFORMS TO ENABLE OFFLINE OTP FEATURE)

In general, to develop offline OTP feature on a platform a developer needs to write the code in backend with specified parameters to implement it, which usually consists of lengthy codes to be rewritten again and again for different platforms. So, the basic idea to develop Verifi-packages is to provide a generalised solution, where one wants to implement the feature on their platform can just import it as library & just write a few line of code to see the magic! 🎩 🪄 Just like the Bootstrap!

On implementing Verifi-Packages to a Service provider’s website, following features can be expected:

On a platform, on activating offline OTP feature, a secret token from backend will be generated & displayed on the screen with popup, which will consist of:

    - A QR Image

    - A base-32 secret Key

         * This base-32 Secret Key will be stored in the database, for further validation of OTP, while logging in again.

         * This base-32 key pair will be triggered based on time-based keying & a secured hashing algorithm will generate a 6-digit OTP from the generated secret key taking it as reference.

         * This 6-digit OTP will change per 30 secs.

         * Enter OTP box will appear on clicking “ENTER OTP“ button on the popup to enter the OTP & to submit it, there’s a submit button. (ALL OF THESE UI CAN BE IMPLEMENTED IN FRONTEND BY USING A SIMPLE VERIFI-PACKAGE)

         * Adding incorrect OTP for more than 5 times (Only 5 attempts will be provided), will restrict OTP entry for 2 minutes, which will handle security vulnerability like brute-force attack.

         * On POST, OTP is verified with backend (i.e servers generated OTP), if it matches ( it returns true i.e. Validation Successful), if not (it returns false, Unsuccessful, Error Message is shown).

         * On Validation of OTP, it redirects to Verified Window. Services of platform will be accessible to user.

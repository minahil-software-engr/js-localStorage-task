   Browser Storage Ke 3 Main Ways

LocalStorage:

Purpose:High-capacity data ko client side par permanently save karne ke liye use hota hai.
Working: Data browser ke storage mein hamesha rehta hai. Isay browser tab close karne ya system restart karne se koi farq nahi parta.
Usage: Core application data, themes (dark/light mode), aur saved user preferences ke liye best hai.

 SessionStorage:

Purpose:Temporary data ko sirf ek single active browser session tak store karne ke liye use hota hai.
Working: Iska data tab tak rehta hai jab tak woh specific tab open hai. Page reload hone par data rehta hai, lekin tab close hotay hi data clear ho jata hai.
Usage: Single-session security forms, temporary workspace states, ya OTP validation ke liye best hai.

Cookies:

Purpose: Chote size ke data aur authentication details ko store karne ke liye use hota hai jo server ke sath communicate kartay hain.
Working: Har HTTP request ke sath browser automatically cookies ko server par bhejta hai.
Usage: User login tokens, session identification, aur tracking ke liye use hota hai.

   Comparison: Expiration & Size Limits:

Capacity (Size Limit):
Cookies:Boht kam capacity hoti hai (sirf **~4 KB** per cookie).
LocalStorage: Kafi bari space milti hai (lagbhag **~5 MB** per domain).
SessionStorage:Is mein bhi **~5 MB** tak ka storage milta hai.


Expiration (Data Kab Tak Rehta Hai?):
Cookies: Iski expiration date code se manually set ki jati hai (`max-age` ya `expires`).
LocalStorage:Expiration nahi hoti; data **permanent** rehta hai jab tak user ya script isay delete na kar de.
SessionStorage: Specific browser **tab close hote hi automatic expire** ho jata hai.

   Challenge: LocalStorage vs SessionStorage Behavior Difference

Jab aap `localStorage` ki jagah `sessionStorage` apply karti hain, toh behavior mein 2 main changes aate hain:

Tab Close Life-Cycle:
 `localStorage` ka data browser close karke agle din dobara open karne par bhi available rehta hai.
 `sessionStorage` ka data jaise hi woh browser tab band hoga, usi waqt completely erase ho jaye ga.


Multi-Tab Isolation:
 `localStorage` ka data same domain par khuli hui tamam tabs mein shared hota hai.
 `sessionStorage` ka data sirf usi specific tab tak limited hota hai jahan woh create hua tha; doosri tab mein accessible nahi hota.

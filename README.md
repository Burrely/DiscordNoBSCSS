# DiscordNoBSCSS
Custom CSS snippets to make Discord have a more tolerable experience.
Examples of features and fixes are, but are not limited to:
- Hiding Nitro, shop and library buttons on the contacts list.
- Startup promotion prevention.
- Camera mirror fix.

> [!TIP]
> Using a third-party client or extension that can load in custom css for Discord is recommended.<br>
> Interested in third party clients? Consider checking out [**Vencord**](https://vencord.dev/) or [**BetterDiscord**](https://betterdiscord.app/)!

## Example
Before                     |  After
:-------------------------:|:-------------------------:
![Before](https://github.com/user-attachments/assets/b2ec4252-0508-49b7-8e80-09e98649accb) |  ![After](https://github.com/user-attachments/assets/cebe10c4-6fa2-4881-a2e2-847f549f7bd3)

## Snippets
The snippets are sorted based on their functionality. Pick and choose as you like! Enjoy!

<details>
  <summary>
    <h3>Full Snippet</h3>
  </summary>

```css
/* DIRECT MESSAGES */

/* Promotional */
[href="/library"] { /* Hide the library button. */
  display: none;
}
[href="/store"] { /* Hide the Nitro button */
  display: none;
}
[href="/shop"] { /* Hide the shop */
  display: none;
}
[class*="upsell"] { /* Hide content that promotes advertising content */
  display: none;
}
div > div > div > div:has([src*="promotions/premium-marketing"]) { /* Hide promotions (specifically on start-up) */
  display: none;
}

/* Activities */
div:has(> div > div[aria-label="Start An Activity"]), div:has(> h2 > div[aria-label="Start An Activity"]) { /* Hide activities from friends list */
  display: none;
}
ul[aria-label="Direct Messages"] div:nth-child(2 of div[class*="sectionDivider"]) { /* Hide Activities divider */
  display: none;
}

div[aria-label="Members"] :nth-child(1 of h3[class*="membersGroup"]:has(span[role="button"])) {
    /* Hide Activities popout */
    display: none;
}

div[aria-label="Members"] > div:has(> div[data-list-item-id*="members"]) { /* Hide server Activites */
  display: none;
}



/* UTILITY */

/* Voice Chats */
div > video[class*="mirror"] { /* Webcam flip fix */
  transform: scaleX(1);
}



/* MISCELLANEOUS STYLING */

/* Title Bar */
.visual-refresh { /* Thinner Title Bar */
  --custom-app-top-bar-height: calc(14px + var(--space-sm));
}

/* Hide user "flair" */
ul[aria-label="Direct Messages"] li[class*="channel"] div > div:has(> div[class*="videoContainer"]),
div[role="list"] div > div > div:has(> div[class*="videoContainer"]){
  display: none;
}

/* Hide Title Text*/
div[class*="title"] > div[class*="title"]:has(> svg),
div[class*="title"] > div[class*="title"]:has(> div[class*="icon"]) {
    display: none;
}

/* Hide Help Button */
a:has(> div[aria-label="Help"]) {
    display: none;
}

/* Hide Inbox Button */
div:has(> div[aria-label="Inbox"]) {
    display: none;
}

/* Hide Animated Profile */
div[class*="profileEffects"] {
    display: none;
}

/* Hide Animated Avatar */
svg[class*="avatarDecoration"] {
    display: none;
}
```
</details>

<details>
  <summary>
    <h3>Promotions / Ads only Snippet</h3>
  </summary>

  ```css
/* DIRECT MESSAGES */

/* Promotional */
[href="/library"] { /* Hide the library button. */
  display: none;
}
[href="/store"] { /* Hide the Nitro button */
  display: none;
}
[href="/shop"] { /* Hide the shop */
  display: none;
}
[class*="upsell"] { /* Hide content that promotes advertising content */
  display: none;
}
div > div > div > div:has([src*="promotions/premium-marketing"]) { /* Hide promotions (specifically on start-up) */
  display: none;
}

/* Activities */
div:has(> div > div[aria-label="Start An Activity"]), div:has(> h2 > div[aria-label="Start An Activity"]) { /* Hide activities from friends list */
  display: none;
}
ul[aria-label="Direct Messages"] div:nth-child(2 of div[class*="sectionDivider"]) { /* Hide Activities divider */
  display: none;
}

div[aria-label="Members"] :nth-child(1 of h3[class*="membersGroup"]:has(span[role="button"])) {
    /* Hide Activities popout */
    display: none;
}

div[aria-label="Members"] > div:has(> div[data-list-item-id*="members"]) { /* Hide server Activites */
  display: none;
}
  ```
</details>

</details>

<details>
  <summary>
    <h3>Utility Snippet</h3>
  </summary>

  ```css
/* UTILITY */

/* Voice Chats */
div > video[class*="mirror"] { /* Webcam flip fix */
  transform: scaleX(1);
}
  ```
</details>

</details>

<details>
  <summary>
    <h3>Miscellaneous Snippet</h3>
  </summary>

  ```css
/* MISCELLANEOUS STYLING */

/* Title Bar */
.visual-refresh { /* Thinner Title Bar */
  --custom-app-top-bar-height: calc(14px + var(--space-sm));
}

/* Hide user "flair" */
ul[aria-label="Direct Messages"] li[class*="channel"] div > div:has(> div[class*="videoContainer"]),
div[role="list"] div > div > div:has(> div[class*="videoContainer"]){
  display: none;
}

/* Hide Title Text*/
div[class*="title"] > div[class*="title"]:has(> svg),
div[class*="title"] > div[class*="title"]:has(> div[class*="icon"]) {
    display: none;
}

/* Hide Help Button */
a:has(> div[aria-label="Help"]) {
    display: none;
}

/* Hide Inbox Button */
div:has(> div[aria-label="Inbox"]) {
    display: none;
}

/* Hide Animated Profile */
div[class*="profileEffects"] {
    display: none;
}

/* Hide Animated Avatar */
svg[class*="avatarDecoration"] {
    display: none;
}
  ```
</details>

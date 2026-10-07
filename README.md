# We need to cook Jesse

A small recipe book, weekly meal planner and shopping list. It is a single `index.html` file that runs in the browser: no server, no build step, no account.

## How it works

1. **Recipes**: add a recipe with a name, its ingredients (each with an amount such as `200 g` or `2`) and, if you like, a note and a link. Click a recipe's name to see everything at a glance.
2. **Calendar**: each day has Breakfast, Lunch and Dinner. Press **+ Add** to put a recipe on a meal; you can search by name or ingredient. Tick the ingredients you are missing and, if you like, enter how much to buy. Click a meal later to change the recipe or the ingredients. **+ Meal** adds an extra meal with a name you choose, and **×** removes a meal from that day.
3. **Shopping list**: the missing ingredients land here automatically, with the amounts to buy. Tick items as you buy them and use **Clear cart** to remove the bought ones. Changing or removing a meal updates the list.
4. **Excel**: **Export Excel** and **Import Excel** let you back up or move your data.

## Where your data lives

By default only in your own browser (localStorage): nothing is sent anywhere. To see the same data on every device, turn on sync.

## Sync between devices (optional)

Your data can be saved to a `data.json` file in a GitHub repository. Use a **separate private repository** for this, not the one that hosts the site.

1. Create a private repository (for example `meal-data`) with at least one commit, for example by ticking *Add a README*.
2. Create a fine-grained personal access token limited to that repository only, with **Contents: Read and write**.
3. Press **Sync**, then enter your username, the data repository name, the branch and the token.

The token is stored only in that device's browser. Repeat the last step on each device.

`data.json` is listed in `.gitignore` so personal data is never committed to this repository by accident.

## Host your own copy

1. Fork this repository (or use it as a template).
2. Go to **Settings → Pages**, choose **Deploy from a branch**, branch `main`, folder `/ (root)`.
3. After a minute the site is live at `https://<your-username>.github.io/<repository-name>/`.

## Credits

The original idea is by **Lorenzo Carbutti**, who developed it for Notion. I used Claude to turn it into this website.

Thanks to Miktaew for making "yet another idle rpg" :)
# Features added by this mod so far...
New Skills:
<details>
<summary>Cultivation</summary>

-all xp multiplied by 1 + (skills["Cultivation"].current_level * 0.1) + Math.floor(skills["Cultivation"].current_level / 5)

-max level is 30

-unlock: Sleeping 6 -> Cultivation

-Cultivate action in shack

</details>

<details>
<summary>Gather efficiency</summary>

-Gathering loot drops increase by a random value between 0 to (skills["Gather efficiency"].current_level + 1)

-this isn't mentioned in the tooltips for gathering activities, but it is displayed normally in the loot log lines

-max level is 3

-skill gains xp when it adds extra materials

</details>

<details>
<summary>Failure expert</summary>

-qol skill, that sends you back to combat after fully resting in bed

-max level is 1, effect only occurs at level 1

-unlock: Sleeping 1 -> Failure expert

-after unlocking the skill you get xp for it from dying (the more you die, the more xp you get, probably unbalanced by the time you get sleep to level 1...)

-<sub><sub>feels more like a perk than a skill...</sup></sup>

</details>

<details>
<summary>Lucky loot</summary>

-the loot drop chance from enemies is multiplied by 1.2 + (skills["Lucky loot"].current_level * 0.1)

-max level is 10

-skill gains xp when loot is dropped

</details>

UI:
-If you have more than 2 milestones on a skill, the tooltip for skills now displays a sum of all previous milestones and the current milestone.


# Original README
# yet another idle rpg
###### by Miktaew


### Still in development.

Official repo: https://github.com/miktaew/yet-another-idle-rpg  
Official release: https://miktaew.github.io/yet-another-idle-rpg/  
  
  
Dev repo: https://github.com/miktaew/yet-another-idle-rpg-dev  
Dev release: https://miktaew.github.io/yet-another-idle-rpg-dev/  


---
Be warned, the game balance remains a WIP
Using the "export" feature every now and then is highly recommended, even on main release, since there's always a risk of some gamebreaking bugs having made it through the testing undetected

---
##### Running
To run the project locally, you will need a server - even a most basic static server will be enough, as it's only about CORS policy. Npm module 'live-server' works perfectly for this purpose https://www.npmjs.com/package/live-server

##### Modifying/Modding and making standalone projects using this as an engine
Making actual changes in code will require either running the build script (`npm run build`) after installing esbuild, or simply changing script source in `index.html` from `dist/bundle.js` to `src/main.js`

When creating content or changing code logic, it's recommended to at the very least take a look at the dev repository, as there's always a possibility it already contains things you wanted to add, or has code changes that will make your work easier, or at least has a fix to a bug you found

Please keep in mind that the default branch you will see here is the `master` branch, while the one that's hosted is the `gh-pages` branch; on dev, the former might often have code that does yet not correspond to what you will see while playing

Consider also calling `Verify_Game_Objects()` in the console, which is a custom built-in tool that will go through most of the content, checking things like properties having acceptable values, or references to other objects being correct. While neither infallible nor covering *everything*, it might save you a lot of time and annoyance.

###### If you make an actual mod, it will be highly appreciated if you mention that it is a mod and not a completely original creation, as well as provide a link to the original. If you can, please also make make it as a fork of either repository, or at least let me know about its existence.
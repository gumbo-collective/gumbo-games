## gumbo-games

Repo that holds the list of games shown on the gumbo website: 
Be careful when modifying. Changes to games.json show up on the live site within a few minutes.

## Sections
 
`games.json` has three lists. Each game goes in one of them:
 
| List | Heading on the site |
| --- | --- |
| `announced` | Coming Soon |
| `demo` | Demo Available |
| `released` | Out Now |
 
## Fields
 
Every game has the same eight fields. Fields marked optional can be left as an empty string (`""`). Don't delete the field, just leave it empty.
 
| Field | Required? | What it does |
| --- | --- | --- |
| `title` | Required | The game's name, shown under the image. |
| `image` | Required | Link to the card image. It's cropped to 16:9, so use a Steam capsule or a similar wide image. It must be a direct link to an image file, not a web page. |
| `gameLink` | Required | Where the card goes when someone clicks the image. Usually the Steam page or the game's site. |
| `site` | Optional | Adds a **Site** button linking to the game's website. |
| `steam` | Optional | Adds a **Steam** button. |
| `itch` | Optional | Adds an **Itch.io** button. |
| `appStore` | Optional | Adds an **AppStore** button. |
| `playStore` | Optional | Adds a **Play** button for Google Play. |
 
A button only appears when its field has a link. If a field is `""`, that button is hidden.
 
## Example
 
```json
{
  "title": "Game Title",
  "image": "https://example.com/image.jpg",
  "gameLink": "https://store.steampowered.com/app/123456/Game_Title/",
  "site": "",
  "steam": "https://store.steampowered.com/app/123456/Game_Title/",
  "itch": "",
  "appStore": "",
  "playStore": ""
}
```
 
## Editing tips
 
- Games appear in a random order each time the page loads.
- One missing quote or comma breaks the whole list. Check your edit at [jsonlint.com](https://jsonlint.com) before committing.
 

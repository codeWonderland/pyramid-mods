# The Pyramid: Definitive Edition Mods
This is the official mod pack for [The Pyramid: Definitive Edition](https://www.github.com/codeWonderland/pyramid-definitive-edition)

## Image Standards
All images should be 350x500px to ensure that file sizes don't get too large. Images will be automatically resized if they don't meet these standards

## Pack Metadata
Each pack folder may include a `pack.json` describing the game alongside its card images. The game reads `tags` to power the draft screen's filters; the other fields describe the game for future screens and are preserved when a pack is edited in the mod manager.

```json
{
	"id": "a-to-z-trivia",
	"name": "A to Z Trivia",
	"tags": ["Miscellaneous", "Puzzle"],
	"is_free": true,
	"estimated_time": "15m",
	"objectives": {
		"primary_count": 22,
		"secondary_count": 7,
		"curse_count": 1,
		"has_curse": true,
		"versus_tertiary": "Compare words found to other players...",
		"co_op_rules": "Fill your lists together!"
	},
	"special_challenges": {
		"developer_available": false,
		"creator_available": false,
		"entries": []
	}
}
```

`tags` use the category names from the internal spreadsheet (Action, Deckbuilder, Bullet Hell, ...). Every field is optional, and a pack without a `pack.json` still loads normally, just without tags.

## Category Definitions
`categories.json` at the root lists every category a pack can be tagged with, with a short description the game shows when hovering that filter on the draft screen.

```json
{
	"categories": [
		{ "id": "deckbuilder", "name": "Deckbuilder", "description": "Games about building, modifying, and using a deck of cards" }
	]
}
```

A pack's `tags` should use these `name`s.

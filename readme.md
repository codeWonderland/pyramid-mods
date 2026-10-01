# The Pyramid: Definitive Edition Mods
This is the official mod pack for [The Pyramid: Definitive Edition](https://www.github.com/codeWonderland/pyramid-definitive-edition)

## Image Standards
All images should be 350x500px to ensure that file sizes don't get too large. Images will be automatically resized if they don't meet these standards

## Pack Metadata
Each pack folder may include a `pack.json` describing the game alongside its card images. The game reads `tags` for the draft screen's filters, and the rest for the Library.

**Edit it in the mod manager's pack editor** (in the game, or the [standalone mod manager](https://github.com/codeWonderland/official-pyramid-mods-manager)), which is where these records are maintained. Its Details section covers the game name, price, time per run, versus and co-op rules, and dev and creator challenges. Saving fills in the card counts, `developer_available` / `creator_available` and ids from the pack itself, so they never need typing. Fields the editor doesn't show are kept.

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

`tags` use the categories in `categories.json` (Action, Deckbuilder, Bullet Hell, ...). A challenge whose contributor's `role` is `Creator` counts as a creator challenge; any other role counts as the game's developers. Every field is optional, and a pack without a `pack.json` still loads normally, just without tags.

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

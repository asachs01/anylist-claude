# anylist-claude

AnyList grocery & shopping list integration for [Claude Code](https://docs.anthropic.com/en/docs/claude-code). Manage your AnyList lists using slash commands.

> **Note:** This uses the unofficial [anylist-js](https://github.com/bobby060/anylist-js) library. Not affiliated with AnyList.

## Setup

```bash
git clone <this-repo> anylist-claude
cd anylist-claude
npm install
node scripts/setup.mjs   # Enter your AnyList email & password
```

Credentials are stored at `~/.config/anylist/.env`.

## Slash Commands

| Command | Description | Example |
|---------|-------------|---------|
| `/grocery-add` | Add items to a list | `/grocery-add Milk, Eggs, Bread` |
| `/grocery-list` | Show items on a list | `/grocery-list Costco` |
| `/grocery-remove` | Check off items | `/grocery-remove Milk, Eggs` |
| `/grocery-delete` | Permanently delete items | `/grocery-delete Stale Item` |
| `/lists` | Show all lists | `/lists` |

Default list is **Groceries**. Specify a different list by name:

```
/grocery-add Costco Rotisserie Chicken, Paper Towels
```

## Scripts

All scripts live in `scripts/` and output JSON to stdout. Run directly:

```bash
node scripts/get-lists.mjs
node scripts/get-items.mjs "Groceries"
node scripts/add-item.mjs "Groceries" "Milk" --qty 2 --notes "whole milk"
node scripts/remove-item.mjs "Groceries" "Milk"
node scripts/delete-item.mjs "Groceries" "Milk"
```

## License

MIT

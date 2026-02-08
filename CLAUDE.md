# AnyList Integration

Manage AnyList grocery/shopping lists via CLI scripts. Credentials: `~/.config/anylist/.env` (run `node scripts/setup.mjs` to configure).

## Scripts (all in `scripts/`, output JSON to stdout)

```bash
node scripts/get-lists.mjs                          # All lists with item counts
node scripts/get-items.mjs "Groceries"               # Unchecked items on a list
node scripts/get-items.mjs "Groceries" --checked      # Include checked items
node scripts/add-item.mjs "Groceries" "Milk"          # Add item (re-adds if checked)
node scripts/add-item.mjs "Groceries" "Milk" --qty 2 --notes "whole milk"
node scripts/remove-item.mjs "Groceries" "Milk"       # Check off (mark complete)
node scripts/delete-item.mjs "Groceries" "Milk"       # Permanently delete
```

Each script call connects/disconnects (~3s). Run add-item once per item.

Known lists: Groceries, Costco, Walmart, Target, Pantry Inventory, Downstairs Freezer Inventory.

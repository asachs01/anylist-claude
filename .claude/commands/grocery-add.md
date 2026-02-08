Add items to an AnyList grocery list.

Usage: /grocery-add [list name] item1, item2, item3

Parse the arguments: if the first word matches a known list name (Groceries, Costco, Walmart, Target, "Pantry Inventory", "Downstairs Freezer Inventory"), use it as the list. Otherwise default to "Groceries" and treat all arguments as items.

Split items by commas. For each item, run:
```
node scripts/add-item.mjs "<list>" "<item>"
```

Report what was added.

$ARGUMENTS

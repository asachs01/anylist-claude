Permanently delete items from an AnyList list.

Usage: /grocery-delete [list name] item1, item2, item3

Parse the arguments: if the first word matches a known list name, use it. Otherwise default to "Groceries".

Split items by commas. For each item, run:
```
node scripts/delete-item.mjs "<list>" "<item>"
```

Report what was deleted.

$ARGUMENTS

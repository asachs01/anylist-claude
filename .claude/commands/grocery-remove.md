Check off (mark complete) items on an AnyList list.

Usage: /grocery-remove [list name] item1, item2, item3

Parse the arguments: if the first word matches a known list name, use it. Otherwise default to "Groceries".

Split items by commas. For each item, run:
```
node scripts/remove-item.mjs "<list>" "<item>"
```

Report what was checked off.

$ARGUMENTS

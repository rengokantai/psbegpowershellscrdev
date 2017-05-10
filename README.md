# psbegpowershellscrdev
## 3. Strings, Arrays and Hash Tables
### 1 Basic Strings
multiple line string:
```
$text = @"
a
b
"@

# @' '@ is also ok
```


### 2 String Interpolation
```
$items = (Get-ChildItem).Count
$loc = Get-Location
```

### 3 Formatting Strings
```
"{0} items {1}". -f $items, $loc
```
keep number after decimalpoint
```
"{0:N2}" -f 123.456   #123.45
"{0,8:N0}" -f 123.45   #     123  (8 placeholders)

others:
- C: currency
- P: percentage


#### 09:33
```
"PowerShell" -like "Power*"
```

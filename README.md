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
```
others:
- C: currency
- P: percentage


#### 09:33
```
"PowerShell" -like "Power*"
```

#### 10:53
```
"123-234-3454" -match "[0-9]{3}-[0-9]{3}-[0-9]{4}"
```

### 4 Arrays
```
$arr = "a", "b"
$arr[0]
$arr[1]
```

Formal syntax
```
$arr = @("a","b")
$arr.Count
```

```
$numbers =1,2,3
$numbers -contains 2
$numbers -notcontains 3
```

#### 05:30
```
$a = 1..3
$b = 6..10
$arr = $a,$b
```


### 5 Hashtables
```
$hash = @{"k1"="v1";"k2"="v2"}
$hash["k1"]
$hash."k1"
$hash.Remove("k1")
$hash.Contains("k1")
$hash.ContainsValue("v1")
$hash.Keys
$hash.Values
```

## 4. Program Flow
```
$var=2
if($var -eq 1){
}
else{
}
```

#### 03:01 switch
```
switch($var){
  1{"a";break}
  2{}
  default{}
}
```

#### 08:25
```
switch -caseinsensitive ("sHell")
{
  "shell"{}
  "sHell"{}
}
```
```
switch -Wildcard (""){
}
```


## 5. Reusing Code with Functions and Modules

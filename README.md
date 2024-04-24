---
runme:
  id: 01HW5HZ40BG01R0MME4CJG9VDP
  version: v3
---

## Setup Runme On MacOS

Die Installation über Homebrew ist die einfachste Möglichkeit auf einem Mac.

```sh {"id":"01HW5J64QWFHB727M5Y9MKMBWG","name":"setup via brew"}
brew install runme
```

## PING Example

Zum testen der Internetverbindung pingen wir nun Google an.

```sh {"id":"01HW5JVFEV6DBZN7QY2E4Z1A2C","name":"check internet connection - ping google"}
ping -c 5 8.8.8.8
```

## interactive - Setting

Beispiel für ein Interaktive code Zelle

```sh {"id":"01HW5Q48R89N4RENHZZZS89FF2","interactive":"true","name":"test","promptEnv":"auto"}
#!/bin/bash
echo "Do you want to see the file list of the current directory? (y/n)"
read answer

if [ "$answer" = "y" ]; then
  ls
else
  echo "Action canceled."
fi

```

## promptEnv - Setting

```sh {"id":"01HW5RNTENGKT5418M2S7Y2NCD","name":"testPromtEnv","promptEnv":"yes"}
export USER_NAME=""
echo $USER_NAME
```

## mime - Setting

```sh {"id":"01HW5TWJBW5EQ7JV6P5Y8HA033","name":"testTableWithoutMimeType"}
cat ./resources/table_example.csv
```

```sh {"cwd":"./resources/","id":"01HW5V1H3YMXPS90XPRVGQVNEB","mimeType":"text/csv","name":"testTableWithMimeType"}
cat table_example.csv
```

```sh {"id":"01HW885JG3N5DYHNGB80P035HS","mimeType":"image/svg+xml","name":"example_svg"}
curl https://api.dicebear.com/6.x/pixel-art/svg
```

## Shebang - Setting

```python {"id":"01HW8A0PN3X2WS2WAJQKNWFSJB","name":"shebang_python"}
print("hello from Python")
```

```javascript {"id":"01HW8A3681WEBT3WS95WP9NBV9","name":"shebang_js"}
console.log("hello from JavaScript")
```

## Piping

```sh {"id":"01HW8ASVBPNKZ1C50FEARY6K91","promptEnv":"yes"}
export URL
echo $URL
```

```sh {"id":"01HW8AWWVX7P360777V58523M6"}
ping -c 5 $__
```
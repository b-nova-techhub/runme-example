---
name: ricky
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

Zum testen der Internetverbindung pingen wir nun Google an!

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
export COMPANY=""
echo $COMPANY
```

## mime - Setting

```sh {"id":"01HW5TWJBW5EQ7JV6P5Y8HA033","interactive":"false","name":"testTableWithoutMimeType","terminalRows":"5"}
cat ./resources/table_example.csv
```

```sh {"cwd":"./resources/","id":"01HW5V1H3YMXPS90XPRVGQVNEB","interactive":"true","mimeType":"text/csv","name":"testTableWithMimeType","terminalRows":"2"}
cat table_example.csv
```

```sh {"id":"01HW885JG3N5DYHNGB80P035HS","mimeType":"image/svg+xml","name":"example_svg"}
curl https://api.dicebear.com/6.x/pixel-art/svg
```

## Rows

```sh {"id":"01HX50RVE48FJSZPP54XFRBXY6","interactive":"true","name":"example_numberOfRows","terminalRows":"5"}
for ((index=1; index<=10; index++)); do
    echo "Row $index"
    sleep 0.25
done
```

## Run by category

```sh {"category":"category_01","id":"01HX64SY5A0CWDKBEM0Y0TM6GY","mimeType":"text/plain","name":"example_cat1_01"}
echo "Hello From "
```

```sh {"category":"category_01","id":"01HX64V1JREVGPSBS2QBE5RAJH","name":"example_cat1_02"}
echo "category 01"
```

```sh {"category":"category_02","id":"01HX64YQ9A03233NSTXSPE25F2","name":"example_cat2_01"}
echo "Hello from category 02"
```

## Shebang - Setting

```python {"id":"01HW8A0PN3X2WS2WAJQKNWFSJB","name":"shebang_python"}
print("hello from Python")

```

```javascript {"id":"01HW8A3681WEBT3WS95WP9NBV9","name":"shebang_js"}
console.log("hello from JavaScript")
```

```java {"id":"01HX44PKHS2XJ91ZX63BPY6HYA","interpreter":"/Library/Java/JavaVirtualMachines/temurin-17.jdk/Contents/Home/bin/java --source 17","name":"shebang_java"}
import java.util.Locale;

class Hello {
    public static void main(String[] args) {
        String lang = Locale.getDefault().getLanguage();
        System.out.println(Greetings.getGreeting(lang) + " from the runme-Techup");
    }
}

class Greetings {
    static String getGreeting(String lang) {
        switch (lang) {
            case "fr": return "Bonjour";
            case "es": return "Hola";
            case "zh": return "Nǐn hǎo";
            case "de": return "Guten Tag";
            case "pl": return "Dzień dobry";
            case "el": return "Yassas";
            case "sv": return "God dag";
            default: return "Hi";
        }
    }
}
```

## Piping

```sh {"id":"01HW8ASVBPNKZ1C50FEARY6K91","promptEnv":"yes"}
export URL
echo $URL
```

```sh {"id":"01HW8AWWVX7P360777V58523M6"}
#ping -c 5 $__
echo $URL
echo $USER_NAME
```

## GitHub Action

```sh {"id":"01HW8CHV3KK1QFDTWWR8E44BNP","name":"example_github_action"}
https://github.com/b-nova-techhub/runme-example/blob/main/.github/workflows/b-nova-runme.yml
```
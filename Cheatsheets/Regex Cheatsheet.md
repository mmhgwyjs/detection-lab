# Regular Expressions (Regex) Reference

## Characters

| Character | Legend | Example | Sample Match |
|-----------|--------|---------|--------------|
| `\d` | Most engines: one digit from 0 to 9 | `file_\d\d` | `file_25` |
| `\d` | .NET, Python 3: one Unicode digit in any script | `file_\d\d` | `file_9੩` |
| `\w` | Most engines: "word character": ASCII letter, digit, or underscore | `\w-\w\w\w` | `A-b_1` |
| `\w` | Python 3: "word character": Unicode letter, ideogram, digit, or underscore | `\w-\w\w\w` | `字-ま_۳` |
| `\w` | .NET: "word character": Unicode letter, ideogram, digit, or connector | `\w-\w\w\w` | `字-ま‿۳` |
| `\s` | Most engines: "whitespace character": space, tab, newline, carriage return, vertical tab | `a\sb\sc` | `a b⏎c` |
| `\s` | .NET, Python 3, JavaScript: "whitespace character": any Unicode separator | `a\sb\sc` | `a b⏎c` |
| `\D` | One character that is not a digit as defined by your engine's `\d` | `\D\D\D` | `ABC` |
| `\W` | One character that is not a word character as defined by your engine's `\w` | `\W\W\W\W\W` | `*-+=)` |
| `\S` | One character that is not a whitespace character as defined by your engine's `\s` | `\S\S\S\S` | `Yoyo` |

## Quantifiers

| Quantifier | Legend | Example | Sample Match |
|------------|--------|---------|--------------|
| `+` | One or more | `Version \w-\w+` | `Version A-b1_1` |
| `{3}` | Exactly three times | `\D{3}` | `ABC` |
| `{2,4}` | Two to four times | `\d{2,4}` | `156` |
| `{3,}` | Three or more times | `\w{3,}` | `regex_tutorial` |
| `*` | Zero or more times | `A*B*C*` | `AAACC` |
| `?` | Once or none | `plurals?` | `plural` |

## More Characters

| Character | Legend | Example | Sample Match |
|-----------|--------|---------|--------------|
| `.` | Any character except line break | `a.c` | `abc` |
| `.*` | Any character except line break | `.*` | `whatever, man.` |
| `\.` | A period (special character: needs to be escaped by `\`) | `a\.c` | `a.c` |
| `\` | Escapes a special character | `\.\*\+\?` | `.*+?` |
| `\` | Escapes a special character | `\[\{\(\)\}\]` | `[{()}]` |

## Logic

| Logic | Legend | Example | Sample Match |
|--------|--------|---------|--------------|
| `|` | Alternation / OR operand | `22|33` | `33` |
| `( … )` | Capturing group | `A(nt|pple)` | `Apple` (captures `"pple"`) |
| `\1` | Contents of Group 1 | `r(\w)g\1x` | `regex` |
| `\2` | Contents of Group 2 | `(\d\d)\+(\d\d)=\2\+\1` | `12+65=65+12` |
| `(?: … )` | Non-capturing group | `A(?:nt|pple)` | `Apple` |

## More White-Space

| Character | Legend | Example | Sample Match |
|-----------|--------|---------|--------------|
| `\t` | Tab | `T\t\w{2}` | `T␣␣␣␣␣ab` |
| `\r` | Carriage return character | See below | |
| `\n` | Line feed character | See below | |
| `\r\n` | Line separator on Windows | `AB\r\nCD` | `AB⏎CD` |
| `\N` | Perl, PCRE (C, PHP, R…): one character that is not a line break | `\N+` | `ABC` |

## More Quantifiers

| Quantifier | Legend | Example | Sample Match |
|------------|--------|---------|--------------|
| `+` | The `+` (one or more) is "greedy" | `\d+` | `12345` |
| `?` | Makes quantifiers "lazy" | `\d+?` | `1` in `12345` |
| `*` | The `*` (zero or more) is "greedy" | `A*` | `AAA` |
| `?` | Makes quantifiers "lazy" | `A*?` | Empty in `AAA` |

## Anchors and Boundaries

| Anchor | Legend | Example | Sample Match |
|--------|--------|---------|--------------|
| `^` | Start of string or start of line | `^abc .*` | `abc` (line start) |
| `$` | End of string or end of line | `.*? the end$` | `this is the end` |
| `\A` | Beginning of string | `\Aabc[\d\D]*` | `abc` (string start) |
| `\z` | Very end of the string | `the end\z` | `this is...⏎the end` |

## Inline Modifiers  

| Modifier | Legend | Example | Sample Match |
|----------|--------|---------|--------------|
| `(?i)`  | Case-insensitive mode (except JavaScript) | `(?i)Monday` | `monDAY` |
| `(?s)`  | DOTALL mode (dot `.` matches newlines, except JS and Ruby) | `(?s)From A.*to Z` | `From A\n to Z` |
| `(?m)`  | Multiline mode (`^` and `$` match start and end of every line, except JS and Ruby) | `(?m)1\r\n^2$\r\n^3$` | `1\n2\n3` |
| `(?x)`  | Free-spacing mode (ignores unescaped whitespace and allows comments, except JavaScript) | `(?x) a \ b ` | `ab` |
| `(?n)`  | .NET, PCRE 10.30+: named capture only (turns all `()` into non-capture groups) | `(?n)(word)` | `word` |
| `(?d)`  | Java: Unix linebreaks only (`.` and anchors affected by `\n` only) |  |  |
| `(?^)`  | PCRE 10.32+: unset modifiers (unsets `ismnx` flags) |  |  |

## Lookarounds

| Lookaround | Legend | Example | Sample Match |
|------------|--------|---------|--------------|
| `(?=…)` | Positive lookahead | `(?=\d{10})\d{5}` | `01234` in `0123456789` |
| `(?<=…)` | Positive lookbehind | `(?<=\d)cat` | `cat` in `1cat` |
| `(?!…)` | Negative lookahead | `(?!theatre)the\w+` | `theme` |
| `(?<!…)` | Negative lookbehind | `\w{3}(?<!mon)ster` | `Munster` |


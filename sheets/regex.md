
Example Text
===============================================================================

```text
Dolorum quaerat animi consequatur labore. Rerum et qui et. Aliquam perferendis dicta libero et voluptatem deleniti. Doloremque cum est aut et et. Repudiandae ad debitis tempora harum. Qui enim est aut dolores consectetur est

Nesciunt porro deleniti ad voluptatem perspiciatis sed. Vel saepe nisi animi sapiente ut nostrum. Iusto est optio commodi suscipit illo minima sint saepe. Vitae magnam quam eos quisquam minima
```

Anchors
===============================================================================

| Syntax    | Description                                   | Example Reg | 1st match | 2nd Match |
| --------- | --------------------------------------------- | ----------- | --------- | --------- |
| ^         | Start of string or start of line (if m flag)  | ^\w{3}      | Dol       | Nes       |
| $         | End of string or start of line (if m flag)    | \w{3}$      | est       | ima       |
| \b        | Word Boundary                                 | \b..        | Do        | _q        |
| \B        | Not Word Boundary                             | \B...       | olo       | rum       |
| \Z        | End of string                                 | \w{3}\Z     | ima       |           |
| \z        | Absolute end of string                        | \w{3}\z     | ima       |           |

Character Classes
===============================================================================

| Syntax    | Description                           | Example Reg | Matches |
| --------- | ------------------------------------- | ----------- | ------- |
| [abd]     | Character Set                         | |
| [^abc]    | Negated Character Set                 | |
| .         | Any single character except newline   | |
| \w        | Word (a-z, A-Z, 0-9, also underscore) | |
| \W        | Not Word                              | |
| \d        | Digit                                 | |
| \D        | Not Digit                             | |
| \s        | Whitespace (space, tab, newline)      | |
| \S        | Not Whitespace                        | |
| \n        | Newline                               | |
| \r        | Carriage Return                       | |
| \t        | Tab                                   | |
| \0        | Null Character                        | |
| \xZZ      | Matches Unicode Hex character ZZ      | |
| \x{0025}  | Matches Unicode Hex character ZZZZ    | |
| [:upper:] | Upper case letters                    | |
| [:lower:] | Lower case letters                    | |
| [:alpha:] | All letters                           | |
| [:alnum:] | Digits and letters                    | |
| [:digit:] | Digits                                | |
| [:punct:] | Punctuation                           | |
| [:print:] | Printed characters and spaces         | |
| [:cntrl:] | Control Characters                    | |

Quantifiers
===============================================================================

| Syntax    | Description                                            | Example Reg | Matches |
| --------- | ------------------------------------------------------ | ----------- | ------- |
| *         | 0 or more                                              | |
| +         | 1 or more                                              | |
| ?         | 0 or 1                                                 | |
| a{3}      | Exactly 3 a's                                          | |
| a{3,}     | 3 or more a's                                          | |
| a{3,5}    | 3, 4, or 5 a's                                         | |
| a+?       | Makes + "lazy", matching as few characters as possible | |

Groups and Ranges
===============================================================================

| Syntax    | Description                                                 | Example Reg | Matches |
| --------- | ----------------------------------------------------------- | ----------- | ------- |
| (a|b)     | Match expression before or after \|                         | |
| (ab)      | Group multiple tokens together                              | |
| (?=ABC)   | Match things BEFORE given value (don't include given value) | \w{3}(?=\senim) | Qui |
| (?<=ABC)  | Match things AFTER given value (don't include given value)  | (?<=\senim\s)\w{3} | est |
| a{3,}     | 3 or more a's                                               | |
| a{3,5}    | 3, 4, or 5 a's                                              | |
| (abc)\4   | Match 4th subpattern                                        | (o.)\1 | would match olol, but not not present |

Pattern Modifiers
===============================================================================

| Syntax    | Description                                | Example Reg | Matches |
| --------- | ------------------------------------------ | ----------- | ------- |
| /g        | Global (keep matching as much as possible) | |
| /i        | Case Insensitive match                     | |
| /s        | Let . match newlines                       | |

Helpful Regex's
===============================================================================

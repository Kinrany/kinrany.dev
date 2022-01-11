# CSV replacement

CSV is a common human-readable plain text format for storing tabular data.

There is unfortunately no common standard for it. There is [RFC 4180], but
it's missing four common cases:
* using a different separator
* using more than one separator between two fields
* using more than one character as a separator
* using a single CR or LF instead of CRLF for line endings

I propose SSSV: a Space or Something-Separated Values format. There are two
changes compared to [RFC 4180]:

1. All empty fields MUST be quoted.
2. All fields of the first record MUST be quoted.

The first rule allows using multiple separators between two fields.

The second rule is introduced to allow any separator and any line ending
character combination to be used.

The first CR, LF or CRLF characters after the first record are chosen as the
line ending. All other records MUST end with this chosen line ending,
except for the last record.

The set of characters between the fields of the first row is chosen as
the separator. Any separator between any two fields MAY use any number of
characters from the chosen set. However, each separator MUST include
every character from the chosen set.

## Example

The following file has three columns and uses spaces and pipes as separators.

```
"one" | "two" | "three"
four  | five  | six
```

Note that using multiple separators allows for the file to be formatted
for better readability in a way similar to Markdown tables.

[RFC 4180]: https://datatracker.ietf.org/doc/html/rfc4180

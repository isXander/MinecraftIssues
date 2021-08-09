# MinecraftIssues
A repository of Minecraft errors and solutions/recommendations.

### Schema
```json5
{
  "info": "This is the text that is shown to the user when triggered",
  "and": [ // all checks must be true
    {
      "method": "contains", // checks if the text contains the value
      "value": "the text must contain this value",
      "not": true, // inverts the check
      "ic": true, // ignore case
      "leniency": 0.5 // half the string can be different to the value
    },
    {
      "method": "regex", // if a single occurance is found. it is triggered
      "value": "regex goes here",
      "not": true // inverts the check
    },
    {
      "method": "modloaded", // checks if the text contains evidence of a mod being loaded
      "value": "the mod id goes here",
      "not": true // invers the check
    }
  ],
  "or": [ // one or more of the checks must be true
    {
      "method": "contains", // checks if the text contains the value
      "value": "the text must contain this value",
      "not": true, // inverts the check
      "ic": true, // ignore case
      "leniency": 0.5 // half the string can be different to the value
    },
    {
      "method": "regex", // if a single occurance is found. it is triggered
      "value": "regex goes here",
      "not": true // inverts the check
    },
    {
      "method": "modloaded", // checks if the text contains evidence of a mod being loaded
      "value": "the mod id goes here",
      "not": true // invers the check
    }
  ]
}
```

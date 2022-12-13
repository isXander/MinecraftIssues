# MinecraftIssues
A repository of Minecraft errors and solutions/recommendations.

### Schema
```json5
{
  "schema_version": 1,
  "categories": [
    {
      "name": "Solutions",
      "checks": [
        {
          "message": "You encountered a first-time crash using CEM mod. Just launch again to resolve the issue.",
          // methods can either be terminating or conditioning
          // terminating are actual checks, for example: 'regex', 'contains' or 'mod_loaded'
          // conditioning take more methods such as: 'and', 'or', 'not'
          "method": "and",
          "conditions": [ // conditions take more methods, can be another 'and', etc
            {
              "method": "contains",
              "query": "java.lang.RuntimeException: Could not execute entrypoint stage 'client' due to errors, provided by 'cem'!"
            },
            {
              "method": "contains",
              "query": "Caused by: java.lang.ClassNotFoundException: me.lortseam.completeconfig.gui.cloth.ClothConfigScreenBuilder"
            }
          ]
        }
      ]
    }
  ]
}
```

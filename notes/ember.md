Update version of ember:

1. `npm uninstall -g ember-cli` # Remove old global ember-cli
2. `npm cache clean` # Clear NPM cache
3. `bower cache clean` # Clear Bower cache
4. `npm install -g ember-cli@2.9.0-beta.2` # Install new global ember-cli

ember-cli@latest is an option

https://github.com/ember-cli/ember-cli/releases


 Links:
Two types of link-to helper. Block and In-line.
```
{{#link-to ‘routename’}}

Using block like this gives more flexibility. You can put a button here, for example.

{{/link-to}}
```
In-line is more simple: 
```
{{link-to ‘Text of link’ ‘routename’}}
```


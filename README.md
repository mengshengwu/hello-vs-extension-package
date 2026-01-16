# Demo vscode extension for package to vsix
```bash
# Install dependencies
npm install
# Package the extension
npx vsce package
```

example output:
```bash
F:\workspace\personal\js_ts\helloworld [main +12 ~0 -0 !]> npx vsce package
Executing prepublish script 'npm run vscode:prepublish'...

> helloworld@0.0.1 vscode:prepublish
> npm run compile


> helloworld@0.0.1 compile
> tsc -p ./

 WARNING  A 'repository' field is missing from the 'package.json' manifest file.
Use --allow-missing-repository to bypass.
Do you want to continue? [y/N] y
 WARNING  LICENSE, LICENSE.md, or LICENSE.txt not found
Do you want to continue? [y/N] y
 INFO  Files included in the VSIX:
helloworld-0.0.1.vsix
├─ [Content_Types].xml
├─ extension.vsixmanifest
└─ extension/
   ├─ changelog.md [0.23 KB]
   ├─ package.json [0.9 KB]
   ├─ readme.md [0.13 KB]
   └─ out/
      ├─ extension.js [2.73 KB]
      └─ test/
         └─ extension.test.js [1.94 KB]

 DONE  Packaged: F:\workspace\personal\js_ts\helloworld\helloworld-0.0.1.vsix (7 files, 4.24 KB)
```

# Install the VSIX extension

-  In VSCode, Ctrl+Shift+P (or Cmd+Shift+P on Mac) to open the Command Palette

-  Input and select "Extensions: Install from VSIX..."

-  Choose the generated .vsix file (e.g., F:\workspace\personal\js_ts\helloworld\helloworld-0.0.1.vsix )

-  Ctrl+Shift+P (or Cmd+Shift+P on Mac) to open the Command Palette again ,type "Hello World"  will see the output message provided by the installed extension.
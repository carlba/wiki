# Node.js

## Usage

### Updating the Reqs For a Project to Latest Version

This will install the latest version of all dependencies in `packages.json`

```bash
npm install -g npm-check-updates
$ ncu -u
$ npm install
```

### Read a markdown file and log it as HTML

```typescript
import * as path from 'path';

const fsp = require('fs').promises;
const showdown  = require('showdown');
const converter = new showdown.Converter();

const readmePath = path.join(__dirname, '..', '..', 'README.md');

fsp.readFile(readmePath, 'utf8').then((data: string) => {
  const html = converter.makeHtml(data);
  console.log(html);
})
```

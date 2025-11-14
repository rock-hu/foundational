# gluestack-ui-cli  

[gluestack-ui/src/commands/init.ts](https://github.com/gluestack/gluestack-ui/blob/main/packages/gluestack-ui/src/commands/init.ts) 

```typescript
import { Command } from 'commander';
import { z } from 'zod';
import { handleError } from '../util/handle-error';
import { log } from '@clack/prompts';
import { InitializeGlueStack } from '../util/init';
import { config } from '../config';
import {
  checkWritablePath,
  detectProjectType,
  getPackageMangerFlag,
  isValidPath,
} from '../util';
import path from 'path';
import fs from 'fs';

export const init = new Command()
  .name('init')
  .description('Initialize gluestack into your project')
  .option('--use-npm ,useNpm', 'use npm to install dependencies', false)
  .option('--use-yarn, useYarn', 'use yarn to install dependencies', false)
  .option('--use-pnpm, usePnpm', 'use pnpm to install dependencies', false)
  .option('--use-bun, useBun', 'use bun to install dependencies', false)
  .option(
    '--path <path>',
    'path to the components directory. defaults to components/ui'
  )
  .option(
    '--template-only templateOnly',
    'Only install the template without installing dependencies',
    false
  )
  .option(
    '--projectType <projectType>',
    'Type of project to initialize',
    'library'
  ).action(async (opts) => {
    ...
  });    
```


[gluestack-ui/network/dependents](https://github.com/gluestack/gluestack-ui/network/dependents) 



## `npx gluestack-ui add --all`
```
npx gluestack-ui add --all
│
●  
│  Welcome to gluestack-ui v3!
│  
│
◇  Repository already cloned.
│
◇  Git pull successful.

Adding new component...

│
◇  Adding 53 components:
⏳ accordion, actionsheet, alert, alert-dialog, all-components, avatar, badge, bottomsheet, box, button, card, center, checkbox, divider, drawer, fab, flat-list, form-control, grid, heading, hstack, icon, image, image-background, input, input-accessory-view, keyboard-avoiding-view, link, menu, modal, popover, portal, pressable, progress, radio, refresh-control, safe-area-view, scroll-view, section-list, select, skeleton, slider, spinner, status-bar, switch, table, text, textarea, toast, tooltip, view, virtualized-list, vstack
│
○  ⏳ Installing dependencies. This might take a couple of minutes

added 1 package, and changed 1 package in 3s

◆  Done! Added 53 components to the project.
```
## Dummy-Meteor

This is a dummy meteor app created to reproduce https://youtrack.jetbrains.com/issue/WEB-60356.

### Installation

1. Clone the repository.
2. Follow steps from https://docs.meteor.com/install.html to install meteor.
3. Run `meteor npm install` to install dependencies.
4. Run `meteor lint` to install typescript definitions.

### Reproduction steps

1. Open, say, `imports/api/links.ts`. Note that WebStorm highlights `LinksCollection` as "not used".
2. Open `imports/ui/Info.tsx`. Note that `LinksCollection` is imported there.
3. Changing `import { LinksCollection } from '/imports/api/links';` to `import { LinksCollection } from 'imports/api/links';` in `Info.tsx` fixes the issue. 

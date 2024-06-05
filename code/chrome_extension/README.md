# ArguSure Chrome Extension Source Code

## 1. Setup

### i. Project Setup

Start by installing your dependencies as usual.

```bash
npm install
```

## Building, Bundling and Shipping 🚢

To get your extension running on Chrome, you'll need to do a couple (easy) steps. Firstly, run the build command, which uses vite to build and output to the `dist` folder.

```bash
npm run build
```

From here, open Chrome and go to `chrome://extensions`, then hit `Load Unpacked` and choose the newly made `dist` directory. Assuming no errors, voila! You're in.

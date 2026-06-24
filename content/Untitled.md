bash

```
npx quartz build --serve
```

Use code with caution.

Once the text stops moving, open your internet browser and go to `http://localhost:8080` to see your notes live on your computer.

Did your website successfully open up in your **browser** after running this, or did it give you another **error**?

You said: node:internal/modules/package_json_reader:301 throw new ERR_MODULE_NOT_FOUND(packageName, fileURLToPath(base), null); ^ Error [ERR_MODULE_NOT_FOUND]: Cannot find package 'yargs' imported from /Users/kevinoneil/my-quartz-site/quartz/bootstrap-cli.mjs at Object.getPackageJSONURL (node:internal/modules/package_json_reader:301:9) at packageResolve (node:internal/modules/esm/resolve:768:81) at moduleResolve (node:internal/modules/esm/resolve:859:18) at defaultResolve (node:internal/modules/esm/resolve:992:11) at #cachedDefaultResolve (node:internal/modules/esm/loader:701:20) at #resolveAndMaybeBlockOnLoaderThread (node:internal/modules/esm/loader:721:38) at ModuleLoader.resolveSync (node:internal/modules/esm/loader:759:56) at #resolve (node:internal/modules/esm/loader:683:17) at ModuleLoader.getOrCreateModuleJob (node:internal/modules/esm/loader:603:35) at ModuleJob.syncLink (node:internal/modules/esm/module_job:163:33) { code: 'ERR_MODULE_NOT_FOUND' } Node.js v24.18.0

This `ERR_MODULE_NOT_FOUND` error means the Quartz packages didn't finish downloading correctly earlier, so your computer is missing a piece called `yargs`.

Don't worry, this is very common and easy to fix. We just need to force the computer to download the missing pieces again.

Make sure you are still inside your `my-quartz-site` folder in the terminal, and run these two commands **one by one**:

Step 1: Repair the missing pieces

Copy this, paste it into your terminal, and press **Enter**:

bash

```
npm install
```

Use code with caution.

_(Wait a minute for the text to finish moving. This installs all the missing files.)_

Step 2: Try the website preview again

Once that finishes, copy this, paste it, and press **Enter**:

bash

```
npx quartz build --serve
```

Use code with caution.

Did the text change to show `http://localhost:8080` this time, or did the **npm install** command give you a different **error message**?
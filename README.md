# vitest-dev-vscode-issue
**error:There was an error during Vitest startup. Check the output for more details**



After `pnpm i` open the vscode editor



I have reviewed the historical issues, and issue #329 appears to be similar. I have provided the minimal reproducible code for reference.



In my case, when `Inspect` is configured in `vite.config.ts`, `vitest vscode` fails to run and start properly. The error message in the bottom right corner states, "There was an error during Vitest startup. Check the output for more details."

However, when `Inspect` is commented out, `vitest vscode` works fine.

I have also tried adding content to the exclude directories, but it was unsuccessful.



**the vitest oupput**

```
[INFO 19:59:01] [v1.8.5] Vitest extension is activated because Vitest is installed or there is a Vite/Vitest config file in the workspace.
[INFO 19:59:01] [API] Running Vitest v2.1.8 (vitest-dev-vscode-issue/vitest.config.ts) with Node.js@: C:\ToolPortable\Nodejs\nodejs\node.EXE 
[Error 19:59:03] [Error Error] Vitest failed to start: 
TypeError: Cannot convert undefined or null to object
    at Function.values (<anonymous>)
    at configureServer (file:///C:/Desktop/vitest-dev-vscode-issue/node_modules/.pnpm/vite-plugin-inspect@0.10.6_rollup@4.29.1_vite@6.0.6_@types+node@22.10.3_/node_modules/vite-plugin-inspect/dist/shared/vite-plugin-inspect.UaceC5Dq.mjs:1408:12)
    at configureServer (file:///C:/Desktop/vitest-dev-vscode-issue/node_modules/.pnpm/vite-plugin-inspect@0.10.6_rollup@4.29.1_vite@6.0.6_@types+node@22.10.3_/node_modules/vite-plugin-inspect/dist/shared/vite-plugin-inspect.UaceC5Dq.mjs:1494:19)
    at _createServer (file:///C:/Desktop/vitest-dev-vscode-issue/node_modules/.pnpm/vite@5.4.11_@types+node@22.10.3/node_modules/vite/dist/node/chunks/dep-CB_7IfJ-.js:63080:26)
    at async createViteServer (file:///C:/Desktop/vitest-dev-vscode-issue/node_modules/.pnpm/vitest@2.1.8_@types+node@22.10.3_jsdom@25.0.1/node_modules/vitest/dist/chunks/cli-api.C2yC_ESk.js:9822:18)
    at async Module.createVitest (file:///C:/Desktop/vitest-dev-vscode-issue/node_modules/.pnpm/vitest@2.1.8_@types+node@22.10.3_jsdom@25.0.1/node_modules/vitest/dist/chunks/cli-api.C2yC_ESk.js:11441:18)
    at async Po (C:\Users\test\.vscode\extensions\vitest.explorer-1.8.5\dist\worker.js:21:8420)
    at async process.e (C:\Users\test\.vscode\extensions\vitest.explorer-1.8.5\dist\worker.js:21:9978)
Error: Vitest failed to start: 
TypeError: Cannot convert undefined or null to object
    at Function.values (<anonymous>)
    at configureServer (file:///C:/Desktop/vitest-dev-vscode-issue/node_modules/.pnpm/vite-plugin-inspect@0.10.6_rollup@4.29.1_vite@6.0.6_@types+node@22.10.3_/node_modules/vite-plugin-inspect/dist/shared/vite-plugin-inspect.UaceC5Dq.mjs:1408:12)
    at configureServer (file:///C:/Desktop/vitest-dev-vscode-issue/node_modules/.pnpm/vite-plugin-inspect@0.10.6_rollup@4.29.1_vite@6.0.6_@types+node@22.10.3_/node_modules/vite-plugin-inspect/dist/shared/vite-plugin-inspect.UaceC5Dq.mjs:1494:19)
    at _createServer (file:///C:/Desktop/vitest-dev-vscode-issue/node_modules/.pnpm/vite@5.4.11_@types+node@22.10.3/node_modules/vite/dist/node/chunks/dep-CB_7IfJ-.js:63080:26)
    at async createViteServer (file:///C:/Desktop/vitest-dev-vscode-issue/node_modules/.pnpm/vitest@2.1.8_@types+node@22.10.3_jsdom@25.0.1/node_modules/vitest/dist/chunks/cli-api.C2yC_ESk.js:9822:18)
    at async Module.createVitest (file:///C:/Desktop/vitest-dev-vscode-issue/node_modules/.pnpm/vitest@2.1.8_@types+node@22.10.3_jsdom@25.0.1/node_modules/vitest/dist/chunks/cli-api.C2yC_ESk.js:11441:18)
    at async Po (C:\Users\test\.vscode\extensions\vitest.explorer-1.8.5\dist\worker.js:21:8420)
    at async process.e (C:\Users\test\.vscode\extensions\vitest.explorer-1.8.5\dist\worker.js:21:9978)
    at ChildProcess.p (C:\Users\test\.vscode\extensions\vitest.explorer-1.8.5\dist\extension.js:20:3607)
    at ChildProcess.emit (node:events:518:28)
    at emit (node:internal/child_process:950:14)
    at processTicksAndRejections (node:internal/process/task_queues:83:21)

```



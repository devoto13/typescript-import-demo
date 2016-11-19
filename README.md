# Demo for TypeScript not reporting error when importing non-existing module

That's it. On attempt to import non-existing module using `import "module-name"` syntax, no error is reported. But it correctly reports error on attempt to import any members from that module.

To reproduce run following commands:

    $ npm install
    $ ./node_modules/.bin/tsc --noEmit

My output is below:

    src/main.ts(1,31): error TS2307: Cannot find module '@angular/platform-browser'.

It should report error for both imports, but error is reported only for one of them.

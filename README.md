# Serverless Clojurescript Workshop

This is the starting template for the serverless workshop.

## Getting started

- Install lein
- Install node via NVM
- Install serverless `npm install serverless -g`

Note: initial template generated using

    serverless create --template aws-nodejs

You can delete, edit or create a new one if you know what you're doing.    

## Quickstart

Are you an EMACS user? Great, I got you.

```bash
npm install serverless -g
npm install
npm run offline
```

Open `core.cljs` in emacs, make a change and save the file.

In a new terminal tab:

```bash
npm run node-watcher
```

In a new terminal tab:

```bash
lein repl
```

In emacs:

    M-x cider-connect

In the REPL:

    user> (go!)

Boom! You've now got figwheel, auto prod builds and serverless offline ready for cURL-ing.

### REPL usage

These are the auto-generated docs for using the REPL.

#### Standalone Usage

1. `lein figwheel`
2. (In another window) `node target\js\compiled\cljs_serverless_workshop.js ...`


#### Production Builds

1. `lein cljsbuild once prod`
2. `node server.js ...`


#### REPL Usage (Vim)

You can now connect to Figwheel's REPL through
[Piggieback](https://github.com/cemerick/piggieback) using
[vim-fireplace](https://github.com/tpope/vim-fireplace):

1. `lein repl`
2. `(fig-start)`
3. `(cljs-repl)`
4. (In another window) `node target\js\compiled\cljs_serverless_workshop.js ...`
5. (In Vim) `:Piggieback (figwheel-sidecar.repl-api/repl-env)`

Standard `vim-fireplace` commands will now work in the context of the
Figwheel process:

- `cqp` to send a command from Vim to the REPL
- `cpa...` to evaluate a form without saving or reloading the file
- etc.

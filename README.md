c<h1 align='center'>OBAOLG</h1>

<p align='center'>
  Myriad is a Decentralized Ecosystem, built upon a backbone of interconnected "Central Nodes". OBAOLG is one such node within that Decentralized Ecosystem.
</p>

<br>

<p align='center'>
<a href="https://obaolg.netlify.app/">Live MCN</a> (Myriad Central Node)
</p>

<br>

## Try it!

> OBAOLG requires Node >=14.18

### Clone to local

If you prefer to do it manually with the cleaner git history

```bash
npx degit BBuchholz/obaolg my-baolg
cd my-baolg
pnpm i # If you don't have pnpm installed, run: npm install -g pnpm
```


## Usage

### Development

Just run and visit http://localhost:3333

```bash
pnpm dev
```

### Build

To build the App, run

```bash
pnpm build
```

And you will see the generated file in `dist` that ready to be served.

### Deploy on Netlify

First, initialize as a Netlify site

```
ntl init
```

Then just build and deploy

```
ntl build
ntl deploy
```

Then, after review, deploy to production with

```
ntl deploy --prod
```


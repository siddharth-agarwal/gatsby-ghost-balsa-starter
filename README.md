# gatsby-ghost-balsa-starter 

[![Netlify Status](https://api.netlify.com/api/v1/badges/e48f3803-8b13-4625-87df-bac480bc4944/deploy-status)](https://app.netlify.com/sites/elated-tesla-fddc20/deploys)

## Ghost Content API keys

All content is sourced from a Ghost CMS. If you don't customize the file `.ghost.json` content is fetched from the demo location at `https://cms.gotsby.org`. Surely you want to source your own content. Change the keys to match your own Ghost CMS Content API keys:

```bash

    {
        "development": {
            "apiUrl": "http://localhost:2368",
            "contentApiKey": "9fccdb0e4ea5b572e2e5b92942"
        },
        "production": {
            "apiUrl": "http://localhost:2368",
            "contentApiKey": "9fccdb0e4ea5b572e2e5b92942"
        }
    }
```

## Deploy

```bash
    gatsby build
```

After completion of the build process your static site can be found in the `public/` folder. Copy those files over to your webserver.


## Optimizing

You can disable the default Ghost Handlebars theme front-end by enabling the `Make this site private` flag within your Ghost settings. This enables password protection in front of the Ghost install and sets `<meta name="robots" content="noindex" />` so your Gatsby front-end becomes the source of truth for SEO.

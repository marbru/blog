# Bardic inspiration blog

This is my personal blog, built with eleventy and based on the [eleventy-base-blog v9](https://github.com/11ty/eleventy-base-blog) starter template.

## Development

Install deps:

```
npm install
```

Generate a production-ready build to the `_site` folder:

```
npx @11ty/eleventy
```

Or build and host on a local development server:

```
npx @11ty/eleventy --serve
```

Or you can run [debug mode](https://www.11ty.dev/docs/debugging/) to see all the internals.


## Writing

Posts go on [content/blog/](content/blog/), each in their own directory. Directory name will become the url segment for that post. Content should go on a `.md` file matching the same name as the directory. Assets particular to that post (like images or any downloads) should go in the folder as well, and linked relatively from the post content.  

## Notes

- Blog base url lives on [](_data/metadata.js). Other settings are in [eleventy.config.js](eleventy.config.js).
- The content on `./public` will be copied to `./_site` at build time. Eg: `./public/css/*` will live at `./_site/css/*`.
- URLs get `/content/` prepended automatically by the `HtmlBasePlugin`. Use `eleventy:ignore` to override (eg, done in [_includes/layouts/base.njk](_includes/layouts/base.njk))

## Blog Comments

The repository for comments on my blog, [mojimoon.github.io](https://mojimoon.github.io).

See [Issues](https://github.com/mojimoon/blog-comments/issues) for comments.

## How to comment

Scroll to the end of any blog post on [mojimoon.github.io](https://mojimoon.github.io) to find the comment section. Leave your comments there.

## Build

This blog uses [Beaudar](https://beaudar.lipk.org/) as the comment system. This is a static and lightweight solution that does not require a backend, making it easy to use and deploy.

Beaudar is optimized for Chinese users. For international users, consider using [Utterances](https://utteranc.es/).

To configure Beaudar for the [Stellar theme](https://github.com/xaoxuu/hexo-theme-stellar), follow these steps:

1. Create a new public repository for comments, e.g., `{username}/blog-comments`.
2. Add a file named `beaudar.json` to the root directory of the comment repository:
    ```json
    {
      "origins": [
        "https://{username}.github.io"
      ]
    }
    ```
    For repository GitHub Pages (e.g. `{username}.github.io/{repo}`), **stick to the above format**. For custom domains, append your custom domain URL to the `origins` array.
3. Append the following configuration to your blog theme's `_config.stellar.yml` file:
    ```yaml
    comments:
      service: beaudar
      beaudar:
        repo: {username}/blog-comments
    ```
4. Install the [Beaudar GitHub App](https://github.com/apps/beaudar) in your comment repository.

Here are the default configurations used by the Stellar theme:

- Theme: GitHub Light/Dark (follows system settings)
- Issue Title: Page Relative Path
- Issue Body: 
```markdown
# {{title}}

{{excerpt}}

{{url}}
```

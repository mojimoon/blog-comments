## Blog Comments

This is the repository for comments on my blog, [cryovit.github.io](https://cryovit.github.io).

All the comments are stored in `Discussions` of this repository.

## How to comment

Go to the blog and at the end of every page, you will find a comment section. Just comment there.

## Build

I choose [Beaudar](https://beaudar.lipk.org/) as the comment system. The static system does not require any backend. It is easy to use and deploy, and very lightweight.

It is specialized for Chinese users. For international users, you can use [Utterances](https://utteranc.es/).

Here is how to configure in [Stellar theme](https://github.com/xaoxuu/hexo-theme-stellar) hexo blog.

For other blogs it is also simple, just refer to [official documentation](https://beaudar.lipk.org/).

1. Create a new repository for comments, for example, `{username}/blog-comments`.
2. Add a file named `beaudar.json` to the root directory of comment repo. Its content:
    ```json
    {
    "origins": [
        "https://{username}.github.io"
    ]
    }
    ```
3. Append the following content to your blog theme config file `_config.stellar.yml`:
    ```yaml
    comments:
    service: beaudar
    beaudar:
        repo: {username}/blog-comments
    ```
4. Install [Github App of Beaudar](https://github.com/apps/beaudar) in your comment repo.

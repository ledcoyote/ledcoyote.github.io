# my homepage

[go there](https://ledcoyote.com)

## managing drafts

you should have the following remotes defined:

```bash
$ git remote -v
draft   git@github.com:ledcoyote/ledcoyote.github.io-draft.git (fetch)
draft   git@github.com:ledcoyote/ledcoyote.github.io-draft.git (push)
origin  git@github.com:ledcoyote/ledcoyote.github.io.git (fetch)
origin  git@github.com:ledcoyote/ledcoyote.github.io.git (push)
```

the convention shall be to maintain a `drafts` branch which is solely pushed to
the `draft` remote, which is private, and a `main` branch pushed to the `origin`
remote, which is public (`main` can also be pushed to `draft`, who cares).

write and commit files in `_drafts` to the `drafts` branch, and push these to
the `draft` remote.

when ready to publish,

```bash
git checkout drafts
mv _drafts/name-of-post.md _posts/YYYY-MM-DD-name-of-post.md
git add _drafts/name-of-post.md _posts/YYYY-MM-DD-name-of-post.md
git commit -m 'publish name-of-post'
git checkout main
git checkout drafts _posts/YYYY-MM-DD-name-of-post.md
git commit -m 'publish name-of-post'
git push origin main
git checkout drafts
git merge main
git push draft drafts
```

to un-publish a post

```bash
git checkout main
rm _posts/YYYY-MM-DD-name-of-post.md
git add _posts/YYYY-MM-DD-name-of-post.md
git commit -m 'unpublish name-of-post'
git push origin main
git checkout drafts
git merge main
git push draft drafts
```

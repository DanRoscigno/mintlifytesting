# Testing mintlify

1. Add `Mintlify` to the spell checker everywhere so you stop ending up with `Minify` :)
2. Acknowledge that the mintlify Starter Kit deployment pops the MDX files into the root dir of the GitHub repo it creates, and that is probably not what you want.
3. To configure mintlify to read from a different dir open [app.mintlify.com](https://app.mintlify.com/) and expand the left side menu (you might not see it, look for a small cube in the top left corner, or set the width of your browser wider). Open settings -> Git
4. In the  Git settings switch on `docs.json is in a subdirectory` and specify the path to the directory used. For me this is `/content`. You can save the change, as the mintlify site will not rebuild on a config change, it waits for a commit to `main` in your repo.
5. Move your content into the directory that you configured as the location for docs.json. In my case I moved docs.json, the MDX file from the starter kit, and images into `content/`:
   ```sh
   git mv docs.json favicon.svg index.mdx logo quickstart.mdx content
   ```
6. Modify the file `content/index.mdx` so that you can verify the changes in the preview that mintlify builds when you submit a PR with the docs.json and content move.
7. Open a PR with the changes and wait for a mintlify preview. Verify the change.
   > Tip
   >
   > you can see previews in [app.mintlify.com](https://app.mintlify.com) under Publishes -> Previews
8. Merge the PR if you like, and verify the change at the production URL


